# Software-Engineering-Repository

This project is done by the following members:
- Jasper Rosales
- John Aaron Caay
- Mar Franklin Caraig
- Nino Joseph Agquiz


<script>
        const chapters = ['ChapterOne', 'ChapterTwo', 'ChapterThree', 'ChapterFour'];

        chapters.forEach(chapter => {
            fetch(`${chapter}.html`)
                .then(response => {
                    if (!response.ok) {
                        throw new Error(`HTTP error! status: ${response.status}`);
                    }
                    return response.text();
                })
                .then(htmlContent => {
                    document.getElementById(chapter).innerHTML = htmlContent;
                })
                .catch(error => {
                    console.error(`Error loading ${chapter}:`, error);
                    document.getElementById(chapter).innerHTML = 'Failed to load ' + chapter;
                });
        });
</script>