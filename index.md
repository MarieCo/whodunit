# Researcher Directory


```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Researcher Directory</title>
    <style>
        body { font-family: Arial, sans-serif; margin: 20px; }
        .researcher { border: 1px solid #ddd; padding: 15px; margin-bottom: 10px; border-radius: 5px; display: flex; align-items: center; }
        .info { margin-left: 15px; }
        .name { font-size: 1.5em; font-weight: bold; }
        .location, .time, .interest, .agenda { margin-top: 5px; }
        img { width: 100px; height: 100px; border-radius: 50%; }
    </style>
</head>
<body>
    <h1>Researcher Directory</h1>
    <div id="researchers"></div>

    <script>
        const researchers = [
            {
                name: "Dr. Jane Smith",
                bio: "Expert in quantum computing with a focus on secure communications.",
                interest: "Quantum cryptography, secure communication protocols",
                agenda: "Working on post-quantum security applications.",
                locations: [
                    { building: "Building A", time: "Mon 9AM-12PM" },
                    { building: "Building B", time: "Wed 2PM-5PM" }
                ],
                picture: "placeholder.jpg",
                collaborators: [{ name: "Dr. Alice Brown", link: "#" }, { name: "Dr. Bob White", link: "#" }]
            },
            {
                name: "Dr. John Doe",
                bio: "AI researcher exploring deep learning models for healthcare.",
                interest: "Neural networks, AI for medical diagnostics",
                agenda: "Developing AI-powered diagnostic tools.",
                locations: [
                    { building: "Building C", time: "Tue 10AM-1PM" },
                    { building: "Building D", time: "Fri 3PM-6PM" }
                ],
                picture: "placeholder.jpg",
                collaborators: [{ name: "Dr. Charlie Green", link: "#" }]
            }
        ];

        const container = document.getElementById("researchers");

        researchers.forEach(res => {
            const div = document.createElement("div");
            div.className = "researcher";
            div.innerHTML = `
                <img src="${res.picture}" alt="${res.name}">
                <div class="info">
                    <div class="name">${res.name}</div>
                    <div class="bio">${res.bio}</div>
                    <div class="interest"><strong>Research Interest:</strong> ${res.interest}</div>
                    <div class="agenda"><strong>Agenda:</strong> ${res.agenda}</div>
                    <div class="locations">
                        <strong>Locations & Availability:</strong>
                        <ul>
                            ${res.locations.map(loc => `<li>${loc.building}: ${loc.time}</li>`).join('')}
                        </ul>
                    </div>
                    <div class="collaborators">
                        <strong>Collaborators:</strong>
                        <ul>
                            ${res.collaborators.map(collab => `<li><a href="${collab.link}">${collab.name}</a></li>`).join('')}
                        </ul>
                    </div>
                </div>
            `;
            container.appendChild(div);
        });
    </script>
</body>
</html>
```

