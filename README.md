# Évaluation GitHub

## Ihsane Montagné

### Étudiant Next-U

Ce projet est destiné a **une évaluation dans le cadre** de _l'obtention de ma première année_

## Some code




    contactForm.addEventListener('submit', (event) => {
        event.preventDefault();
        
        const name = document.getElementById('name').value;
        const phone = document.getElementById('phone').value;
        const email = document.getElementById('email').value;

        if (name && phone && email) {
            addContact(name, phone, email);
            contactForm.reset();
        }
    });

    function addContact(name, phone, email) {
        const li = document.createElement('li');

        li.innerHTML = `
            <span>${name} - ${phone} - ${email}</span>
            <button onclick="deleteContact(this)">Supprimer</button>
        `;

        contactList.appendChild(li);
    }