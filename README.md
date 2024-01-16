<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
        }

        .tab-container {
            overflow: hidden;
            white-space: nowrap;
        }

        .tabs {
            transition: transform 0.3s;
        }

        .tab {
            display: inline-block;
            padding: 10px 20px;
            background-color: #ddd;
            cursor: pointer;
            transition: background-color 0.3s;
        }

        .tab:hover {
            background-color: #bbb;
        }

        .tab-content {
            display: none;
        }

        .scroll-button {
            cursor: pointer;
            padding: 10px;
            background-color: #ddd;
            border: none;
            outline: none;
        }
    </style>
</head>

<body>

    <div class="tab-container">
        <button class="scroll-button" onclick="scrollTabs(-1)">❮</button>
        <div class="tabs">
            <div class="tab" onclick="openTab('tab1')">Tab 1</div>
            <div class="tab" onclick="openTab('tab2')">Tab 2</div>
            <div class="tab" onclick="openTab('tab3')">Tab 3</div>
            <div class="tab" onclick="openTab('tab1')">Tab 1</div>
            <div class="tab" onclick="openTab('tab2')">Tab 2</div>
            <div class="tab" onclick="openTab('tab3')">Tab 3</div>
            <div class="tab" onclick="openTab('tab1')">Tab 1</div>
            <div class="tab" onclick="openTab('tab2')">Tab 2</div>
            <div class="tab" onclick="openTab('tab3')">Tab 3</div>
            <div class="tab" onclick="openTab('tab1')">Tab 1</div>
            <div class="tab" onclick="openTab('tab2')">Tab 2</div>
            <div class="tab" onclick="openTab('tab3')">Tab 3</div>
            <div class="tab" onclick="openTab('tab1')">Tab 1</div>
            <div class="tab" onclick="openTab('tab2')">Tab 2</div>
            <div class="tab" onclick="openTab('tab3')">Tab 3</div>
            <div class="tab" onclick="openTab('tab1')">Tab 1</div>
            <div class="tab" onclick="openTab('tab2')">Tab 2</div>
            <div class="tab" onclick="openTab('tab3')">Tab 3</div>
            <div class="tab" onclick="openTab('tab1')">Tab 1</div>
            <div class="tab" onclick="openTab('tab2')">Tab 2</div>
            <div class="tab" onclick="openTab('tab3')">Tab 3</div>
            <div class="tab" onclick="openTab('tab1')">Tab 1</div>
            <div class="tab" onclick="openTab('tab2')">Tab 2</div>
            <div class="tab" onclick="openTab('tab3')">Tab 3</div>
            <div class="tab" onclick="openTab('tab1')">Tab 1</div>
            <div class="tab" onclick="openTab('tab2')">Tab 2</div>
            <div class="tab" onclick="openTab('tab3')">Tab 3</div>
            <div class="tab" onclick="openTab('tab1')">Tab 1</div>
            <div class="tab" onclick="openTab('tab2')">Tab 2</div>
            <div class="tab" onclick="openTab('tab3')">Tab 3</div>
            <div class="tab" onclick="openTab('tab1')">Tab 1</div>
            <div class="tab" onclick="openTab('tab2')">Tab 2</div>
            <div class="tab" onclick="openTab('tab3')">Tab 3</div>
            <div class="tab" onclick="openTab('tab1')">Tab 1</div>
            <div class="tab" onclick="openTab('tab2')">Tab 2</div>
            <div class="tab" onclick="openTab('tab3')">Tab 3</div>
            <div class="tab" onclick="openTab('tab1')">Tab 1</div>
            <div class="tab" onclick="openTab('tab2')">Tab 2</div>
            <div class="tab" onclick="openTab('tab3')">Tab 3</div>
            <!-- Add more tabs as needed -->
        </div>
        <button class="scroll-button" onclick="scrollTabs(1)">❯</button>
    </div>

    <div class="tab-content" id="tab1">
        <h2>Content for Tab 1</h2>
        <p>This is the content for Tab 1.</p>
    </div>

    <div class="tab-content" id="tab2">
        <h2>Content for Tab 2</h2>
        <p>This is the content for Tab 2.</p>
    </div>

    <div class="tab-content" id="tab3">
        <h2>Content for Tab 3</h2>
        <p>This is the content for Tab 3.</p>
    </div>

    <script>
        var currentIndex = 0;

        function openTab(tabId) {
            // Hide all tab content
            var tabContents = document.getElementsByClassName("tab-content");
            for (var i = 0; i < tabContents.length; i++) {
                tabContents[i].style.display = "none";
            }

            // Show the selected tab content
            document.getElementById(tabId).style.display = "block";
        }

        function scrollTabs(direction) {
            var tabsContainer = document.querySelector('.tabs');
            var tabs = document.querySelectorAll('.tab');
            var tabWidth = tabs[0].offsetWidth;
            var maxIndex = tabs.length - 1;
            var maxScroll = maxIndex * tabWidth;

            currentIndex = Math.min(maxIndex, Math.max(0, currentIndex + direction));
            var translateValue = -currentIndex * tabWidth;

            tabsContainer.style.transform = 'translateX(' + translateValue + 'px)';
        }
    </script>

</body>

</html>
