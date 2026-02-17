You are a naming assistant. Given a list of file paths and minimal context from a static website, suggest a new filename (basename only, same extension) for each file. Rules:
- Lowercase, kebab-case, no spaces. SEO-friendly and human-readable.
- For HTML: use page purpose (e.g. about-us.html, contact.html). Keep index.html as index.html.
- For CSS/JS: use purpose (e.g. main-styles.css, analytics.js).
- For images: use content (e.g. logo-infygate.webp, hero-banner.webp). Use alt/title when provided.
- Return a JSON object: keys = exact original path strings, values = new basename only (e.g. "main.css"). Preserve extension.
- Do not change path prefix (e.g. css/ stays css/ by returning "name.css" not "css/name.css").

Files and context:
[
  {
    "path": "404.html",
    "context": {
      "title": "",
      "first_heading": "404"
    }
  },
  {
    "path": "admission.html",
    "context": {
      "title": "Admissions | Online Registrations | OES",
      "first_heading": "ADMISSIONS"
    }
  },
  {
    "path": "careers.html",
    "context": {
      "title": "Oxford School Careers | OES",
      "first_heading": "CAREERS"
    }
  },
  {
    "path": "certificates.html",
    "context": {
      "title": "Certificates | OES | Devanahalli",
      "first_heading": "CERTIFICATES"
    }
  },
  {
    "path": "contact_us.html",
    "context": {
      "title": "Contact Oxford | OES Devanahalli",
      "first_heading": "CONTACT US"
    }
  },
  {
    "path": "coscholastic_programmes.html",
    "context": {
      "title": "Co-scholastic Programmes | OES Devanahalli",
      "first_heading": "CO-SCHOLASTIC PROGRAMMES"
    }
  },
  {
    "path": "css/4ba1f7eeea678c518b19a8a229705620.css",
    "context": {
      "path": "css/4ba1f7eeea678c518b19a8a229705620.css"
    }
  },
  {
    "path": "css/559e64bf161e61fa0aca6e864c78191d.css",
    "context": {
      "path": "css/559e64bf161e61fa0aca6e864c78191d.css"
    }
  },
  {
    "path": "css/7cd3c01f553780097ebe1c4668033bfe.css",
    "context": {
      "path": "css/7cd3c01f553780097ebe1c4668033bfe.css"
    }
  },
  {
    "path": "css/7e610f95a2d26c26bc901487cdcd9a1c.css",
    "context": {
      "path": "css/7e610f95a2d26c26bc901487cdcd9a1c.css"
    }
  },
  {
    "path": "css/84d4a0216f16f715d9b301db3a8da352.css",
    "context": {
      "path": "css/84d4a0216f16f715d9b301db3a8da352.css"
    }
  },
  {
    "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css",
    "context": {
      "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css"
    }
  },
  {
    "path": "css/d09d646f062b67daeff66ff1410b63fc.css",
    "context": {
      "path": "css/d09d646f062b67daeff66ff1410b63fc.css"
    }
  },
  {
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "facilities.html",
    "context": {
      "title": "Facilities | Oxford English School Devanahalli",
      "first_heading": "FACILITIES"
    }
  },
  {
    "path": "imgs/01c068e11a5b7623e14ec801c77e805a.webp",
    "context": {
      "refs": [
        {
          "alt": "Karate Classes, Oxford English School, Extra Activities",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/02f64de11787f5e97d2abf45318365fe.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/052d40a1bcbeca3364d2ca5ca8a0a907.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/06c5c5901dccfc45d711b011094e6055.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/09c2831fd67fda77bb04078c3ce8f771.webp",
    "context": {
      "refs": [
        {
          "alt": "School Admissions Online, Online Registrations",
          "title": ""
        },
        {
          "alt": "Online Registration, Online Admission, Pay Fee Online, School Admissions Online.",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0e9568764d92ba83bbeb21b0c86b7cd6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0f5b2bfaaa923e028b8b687790df429f.webp",
    "context": {
      "refs": [
        {
          "alt": "Yoga Classes in School, Yoga day, best yoga training school",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/11a43d98820f9cc8fb423857b456cfa7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/18c4365cb3da348b614073cfe16c17cc.webp",
    "context": {
      "refs": [
        {
          "alt": "Vijaya Bharathi Education Society",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1ccd128f2d9b32b46e1e3a20bcd0da61.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1d6a5318af36417a4a48b5246afecd84.webp",
    "context": {
      "refs": [
        {
          "alt": "Schools with big playgrounds, Schools with extra curriculum activities, Sports School",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1fe97bbbc1c9ef4d51f20f827ed5f12d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/20a665f6fba4ae55ede13428f682eef9.webp",
    "context": {
      "refs": [
        {
          "alt": "Self Declaration",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/22525d8ed63b97a4adc4c7bb890b7f2a.webp",
    "context": {
      "refs": [
        {
          "alt": "The Art Room",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/231223f049096d0888fb6dae3a1ba457.webp",
    "context": {
      "refs": [
        {
          "alt": "Token of appreciation, appreciate students",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/25679944ec540cf3e5b58100964ad77a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/25820959cd518a652ffb3a074fb8cbbd.webp",
    "context": {
      "refs": [
        {
          "alt": "Vijaya Bharati Educational Society Certificate, Educational Certificate",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/25e95a2c7af380ca1dc0546d4236daf5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2781d9a53a9ff6e832919a41ff27e27f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/28892a0a3d85c0f2264f8f4da96fb242.webp",
    "context": {
      "refs": [
        {
          "alt": "INFRASTRUCTURE DETAILS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2d6963a8a911afff3cb4ea04de66d3b3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3087657ffa25d8737635e433ae940a73.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3315be3fbc98fc442f2f49f31280501f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/365572a59ff9723fba1f91ce19f62e60.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3c481d2085930c5471ec88b8dd7be3a2.webp",
    "context": {
      "refs": [
        {
          "alt": "MANDATORYDISCLOSUREpage0002",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/40e7ff89b27870160fd04b33653e4d7e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "Best Educational Institute in Bangalore, Pre Schools Devanahalli, Nursery Schools, High Schools",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/447b29bc0f07b16551e65ba00875d38a.webp",
    "context": {
      "refs": [
        {
          "alt": "Annaul day Inauguration Function",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4518eef139c1249072136d8949d4da43.webp",
    "context": {
      "refs": [
        {
          "alt": "Schools with big playgrounds, Schools with extra curriculum activities, Sports School",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/451cd82b14bbe754c6e5123d18722f6b.webp",
    "context": {
      "refs": [
        {
          "alt": "Schools with big playgrounds, Schools with extra curriculum activities, Sports School",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/48e081c49d65ea2407fdf1412e4c301c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4ce8901476ebb2b6caf55ea8e567ab6b.webp",
    "context": {
      "refs": [
        {
          "alt": "Fire Safety Certified, Schools with Safety Certified",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4cf9ddb60c2d5394fefe818c5bcc5c1a.webp",
    "context": {
      "refs": [
        {
          "alt": "Schools with big playgrounds, Schools with extra curriculum activities, Sports School",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4e206272285a01f2be5b2250053fe2cc.webp",
    "context": {
      "refs": [
        {
          "alt": "Academic Calendar",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/50d9760bd494a0f50942364274c2d796.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/52ea9c3931fea70954c9aa96e9daf834.webp",
    "context": {
      "refs": [
        {
          "alt": "VIDYA BHARATHI EDUCATIONAL SOCIETY - AFFIDAVIT",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/53feddeece6ade8878c5d060e20391d3.webp",
    "context": {
      "refs": [
        {
          "alt": "School Day Dance, Schools at Devanahalli",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/544ae6d80b167905e1b243164c7b1593.webp",
    "context": {
      "refs": [
        {
          "alt": "Prayer Assembly, Pray for Education, Educational Institute, Best School for life",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5529e1c36c80badb6073eabd855fae77.webp",
    "context": {
      "refs": [
        {
          "alt": "TMC Drinking Water And Sanitary",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/56884472103a6a30147ee85149d38b96.webp",
    "context": {
      "refs": [
        {
          "alt": "Library, Books for Life",
          "title": ""
        },
        {
          "alt": "Oxford English School, Libraries in school",
          "title": ""
        },
        {
          "alt": "Encourage Education, Independing Reading and Research",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/59a76b71fac77f3b40ce9168f355abae.webp",
    "context": {
      "refs": [
        {
          "alt": "PWD Building Safety Certificate, Government Adied School, Government Certified Schools",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5b4767bf48a221c229cb15abbef02287.webp",
    "context": {
      "refs": [
        {
          "alt": "Play Ground",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5e25c9767b053d81b348d21e83b36975.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/61234f078c52ff887ac81595c6dae135.webp",
    "context": {
      "refs": [
        {
          "alt": "Fashion day in schools",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/618478ed2e50b11e75716c122d840c5f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/62a9e2b26e1e946d2fc2dad2e2d9377a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/67a4a8e4789191c4a7cb157f97c4f6d5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/67fb18aa0f7c8c4f0798bc9c6c459168.webp",
    "context": {
      "refs": [
        {
          "alt": "Washroom, Swacha Barath, Clean Toilets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6a7d5dd27a55355efd4195a70bebdd24.webp",
    "context": {
      "refs": [
        {
          "alt": "MANDATORYDISCLOSUREpage000101",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6aa4e018eca23e1a480a082966e821fe.webp",
    "context": {
      "refs": [
        {
          "alt": "Oxford English School, Registration Desk, Office Desk",
          "title": ""
        },
        {
          "alt": "Co-Educational School, Devanahalli",
          "title": ""
        },
        {
          "alt": "Innovative Learning, Intellectual Learning, Physical and Creative Potentials, School For life",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/72294492d90e58041292ab6b7c6ba86b.webp",
    "context": {
      "refs": [
        {
          "alt": "Library",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/724bfd5701c3c3db19cca2f151da51fd.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/73b7fd84b9314285fff03b4bc0d49a17.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/746f57dad9261d706212d75e99249c23.webp",
    "context": {
      "refs": [
        {
          "alt": "Oxford Englsih School Classroom, School Infrastracture",
          "title": ""
        },
        {
          "alt": "School with Best Infrastructure near devanahalli, Schools with Best Classrooms",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/767521ae42f5acef3c1e8a68cf629e47.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7b90e7a56f7beec907ff313d49f727ba.webp",
    "context": {
      "refs": [
        {
          "alt": "Oxford Chairman, Ramachandra Gowda",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/80e43ab75e3cf34870372af8b49398d1.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/82705474693ec2b57797ec84306e982e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/874bf442c3a29d41c06cfa32aa188050.webp",
    "context": {
      "refs": [
        {
          "alt": "PWD Building Safety Certificate",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8bb4ba095e834c22797c183d2b4364e0.webp",
    "context": {
      "refs": [
        {
          "alt": "Professional Development, Best School Near Devanahalli",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8c9c8119e76041aefa9b838402fdbbfc.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/93e76c2d6bf01250d39d4ce6c6dcf62b.webp",
    "context": {
      "refs": [
        {
          "alt": "Fire Certificate",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/942b9f28399bfc37d2f2906fa71b190e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/944e3360fd9845e402f16ef30daae8d6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9555e0fa53f81075ae52fcad81426e98.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9ad5e7561d1fbf73a822f9aa968c19b2.webp",
    "context": {
      "refs": [
        {
          "alt": "Computer Lab, Best Computer lab with good faculties",
          "title": ""
        },
        {
          "alt": "Computer Education, Computer Lab, School with Computer Labs.",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9e7cd4d506c5fe618b2a52b809ee5eae.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a564e3979d34ef4548c859e7f759c99e.webp",
    "context": {
      "refs": [
        {
          "alt": "Recognition Certificate, Schools Near Devanahalli",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a5bee7090d810849f861d6965edf82ed.webp",
    "context": {
      "refs": [
        {
          "alt": "Schools with big playgrounds, Schools with extra curriculum activities, Sports School",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a5f732d965df377cb4d274b548d8a44e.webp",
    "context": {
      "refs": [
        {
          "alt": "Drawing classes, artist life, painting classes near me",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a6aaf2dec5d808aca6efc64dca58a6e7.webp",
    "context": {
      "refs": [
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/aa39a5d9d02f1b53fa2e0e41cbbcc7f5.webp",
    "context": {
      "refs": [
        {
          "alt": "NOC Certificate, Oxford English School",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/aa74aeedcdcfe34d6e51fe5131fce88f.webp",
    "context": {
      "refs": [
        {
          "alt": "Certificate Of Land",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ad25c7020f34a42bc626f2ae1fb096a8.webp",
    "context": {
      "refs": [
        {
          "alt": "Drawing classes, artist life, painting classes near me",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b0d8a52af9705875479716cc31092feb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b5028f40a6cf7fd9c8bba52b5197be88.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b5ced7f974cf9d2d9999d5ee65abafbe.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b81e0c01a49a7b0e2e08a7dd83e80572.webp",
    "context": {
      "refs": [
        {
          "alt": "Recognition Under RTE",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b8aefe467494d08d279fcf15b3c24f10.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bedb0235d561222604b56c8348fe0b03.webp",
    "context": {
      "refs": [
        {
          "alt": "No Objection (NOC)",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c0ff58a889b35f92ff07b13bf36a2675.webp",
    "context": {
      "refs": [
        {
          "alt": "School day functions, Oxford English School, Fashion day in schools",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c304b1364ea885b08f14747123e2be7c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c69db0711e5afa810d8bdeb1bb6462e6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c721a18bc04ae00d5bd751f3d044ad5e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c7aea1748a0b121570f3f12a560e66b8.webp",
    "context": {
      "refs": [
        {
          "alt": "Schools with big playgrounds, Schools with extra curriculum activities, Sports School",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c8e737b15e786d3d921859cb70ac1aa2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cac20e629c160cdf2d46bcd21e968c6e.webp",
    "context": {
      "refs": [
        {
          "alt": "Government Certified Schools",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d06d5fbc335a87f71b78f0940c3566ce.webp",
    "context": {
      "refs": [
        {
          "alt": "Government Affiliated School, Convents Near Devanahalli",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d0b6d2d2f4314625047bc4db21494c61.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d0d4ca84e1d1a74d317368a0844d715a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d4163da47962f8b7ced6c89a87e69a10.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d78916e7208dbba2acca9a9d72c3a52c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/dabf04311007296e54120b51370c4e8a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/db27e64fa6a88f5a850f27f318f51590.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/dc0e1bba5edb4bf2a6ef02be6b59d77d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/dc2adea37804cb49cddf386407530346.webp",
    "context": {
      "refs": [
        {
          "alt": "Certified to students",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/dcb94c93f80ca8e66b49953b39a8ec66.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/dd7c6b30a634baa65a5918572922e651.webp",
    "context": {
      "refs": [
        {
          "alt": "Nurssery ClassRoom, Best Pre-School",
          "title": ""
        },
        {
          "alt": "Scholastic Programmes, Play and Learn, Kids Zone, Children Care Center",
          "title": ""
        },
        {
          "alt": "Best Schools for Kids in North Bangalore, Schools at North Bangalore, CBSC Schools Near Devanahalli",
          "title": ""
        },
        {
          "alt": "Drawing classes, artist life, painting classes near me",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e113adf006d049617bfd8f83ea6d1d0e.webp",
    "context": {
      "refs": [
        {
          "alt": "Schools with big playgrounds, Schools with extra curriculum activities, Sports School",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e1436d8911cc94bece8bd1c56c8994ae.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e289bba629afbe8d2b7a52482650a6f4.webp",
    "context": {
      "refs": [
        {
          "alt": "Fee Structure",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/eb1874c6537a821a5d6056ae23a83f43.webp",
    "context": {
      "refs": [
        {
          "alt": "School with best transportation Facility",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ee7641367a1302a7d66e9cabe394b00e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f53fd60dd49e170ee6a7ebb9feff244d.webp",
    "context": {
      "refs": [
        {
          "alt": "Classrooms",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f642321ae0e0a94ac4d33d2e1f046365.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fc98bdf6bf64d8282a91f7616cf24a64.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fe5033d2815de7920d1723e3f88aecbf.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "Oxford English School | Devanahalli",
      "first_heading": "Oxford English School"
    }
  },
  {
    "path": "infrastructure.html",
    "context": {
      "title": "Infrastructure | OES | Devanahalli",
      "first_heading": ""
    }
  },
  {
    "path": "js/03b2eaae6007054a68c38e495f894dba.js",
    "context": {
      "path": "js/03b2eaae6007054a68c38e495f894dba.js"
    }
  },
  {
    "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js",
    "context": {
      "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js"
    }
  },
  {
    "path": "js/0c46896987137b0016246f6bc2243099.js",
    "context": {
      "path": "js/0c46896987137b0016246f6bc2243099.js"
    }
  },
  {
    "path": "js/165d7b0ddfa33362140feea997351b77.js",
    "context": {
      "path": "js/165d7b0ddfa33362140feea997351b77.js"
    }
  },
  {
    "path": "js/16df9ef05001a1741857bf99f5a5738f.js",
    "context": {
      "path": "js/16df9ef05001a1741857bf99f5a5738f.js"
    }
  },
  {
    "path": "js/2a85c11e395a8380b5915443e926b569.js",
    "context": {
      "path": "js/2a85c11e395a8380b5915443e926b569.js"
    }
  },
  {
    "path": "js/34be5330971fdbd18985525bd994b0aa.js",
    "context": {
      "path": "js/34be5330971fdbd18985525bd994b0aa.js"
    }
  },
  {
    "path": "js/35c5f9e096d4da33d2a62031daf14248.js",
    "context": {
      "path": "js/35c5f9e096d4da33d2a62031daf14248.js"
    }
  },
  {
    "path": "js/3d70953a848219e749fedc2cdb906675.js",
    "context": {
      "path": "js/3d70953a848219e749fedc2cdb906675.js"
    }
  },
  {
    "path": "js/3e940a33e44b65c1c0af8bb80a893530.js",
    "context": {
      "path": "js/3e940a33e44b65c1c0af8bb80a893530.js"
    }
  },
  {
    "path": "js/544d012df7acf9c3f0920f67c9e322b9.js",
    "context": {
      "path": "js/544d012df7acf9c3f0920f67c9e322b9.js"
    }
  },
  {
    "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js",
    "context": {
      "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js"
    }
  },
  {
    "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js",
    "context": {
      "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js"
    }
  },
  {
    "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js",
    "context": {
      "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js"
    }
  },
  {
    "path": "js/7260bab328b0ad74815a5efb377bcc67.js",
    "context": {
      "path": "js/7260bab328b0ad74815a5efb377bcc67.js"
    }
  },
  {
    "path": "js/893de96f1b6da546bd7c814964723eca.js",
    "context": {
      "path": "js/893de96f1b6da546bd7c814964723eca.js"
    }
  },
  {
    "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js",
    "context": {
      "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js"
    }
  },
  {
    "path": "js/9455859483e31e4da0e28f10d0742c2a.js",
    "context": {
      "path": "js/9455859483e31e4da0e28f10d0742c2a.js"
    }
  },
  {
    "path": "js/9db10375d298678e53777a2347b87073.js",
    "context": {
      "path": "js/9db10375d298678e53777a2347b87073.js"
    }
  },
  {
    "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js",
    "context": {
      "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js"
    }
  },
  {
    "path": "js/a2261649751fa61b606222c9b2ea3b80.js",
    "context": {
      "path": "js/a2261649751fa61b606222c9b2ea3b80.js"
    }
  },
  {
    "path": "js/b0bade6d42c2702ca85774296cc507c4.js",
    "context": {
      "path": "js/b0bade6d42c2702ca85774296cc507c4.js"
    }
  },
  {
    "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js",
    "context": {
      "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js"
    }
  },
  {
    "path": "js/cecb447a04bbe3e8982190dd6e697120.js",
    "context": {
      "path": "js/cecb447a04bbe3e8982190dd6e697120.js"
    }
  },
  {
    "path": "js/d80b370d82680fc786dcc943a327b9f2.js",
    "context": {
      "path": "js/d80b370d82680fc786dcc943a327b9f2.js"
    }
  },
  {
    "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js",
    "context": {
      "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js"
    }
  },
  {
    "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js",
    "context": {
      "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js"
    }
  },
  {
    "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js",
    "context": {
      "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js"
    }
  },
  {
    "path": "js/f8b57e3e8f415a27a60eb651df50e801.js",
    "context": {
      "path": "js/f8b57e3e8f415a27a60eb651df50e801.js"
    }
  },
  {
    "path": "mandatory-disclosure.html",
    "context": {
      "title": "Mandatory Disclosure | OES | Devanahalli | OES | Devanahalli",
      "first_heading": "MANDATORY DISCLOSURE"
    }
  },
  {
    "path": "parents_as_partners.html",
    "context": {
      "title": "Parents As Partners | Oxford English School Devanahalli",
      "first_heading": "PARENTS AS PARTNERS"
    }
  },
  {
    "path": "public-disclosure.html",
    "context": {
      "title": "Public Disclosure | OES | Devanahalli",
      "first_heading": "PUBLIC DISCLOSURE"
    }
  },
  {
    "path": "scholastic_programmes.html",
    "context": {
      "title": "Scholastic Programmes | Oxford English School Devanahalli",
      "first_heading": "SCHOLASTIC PROGRAMMES"
    }
  },
  {
    "path": "who_we_are.html",
    "context": {
      "title": "About Oxford English School Devanahalli | OES",
      "first_heading": "ABOUT US"
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.