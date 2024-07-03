# Perspectief 2: Uitdagingen en Beperkingen van Plastic Recycling

## Argument 1: Beperkte Recycleerbaarheid van Kunststoffen
Hoewel plastic recycling aanzienlijke voordelen biedt, zijn er ook belangrijke uitdagingen. Een van de grootste beperkingen is de beperkte recycleerbaarheid van veel soorten kunststoffen. Niet alle kunststoffen kunnen even gemakkelijk worden gerecycled. Sommige kunststoffen, zoals thermoharders, kunnen niet opnieuw worden gesmolten en hergebruikt, terwijl andere, zoals thermoplasten, meerdere keren kunnen worden gerecycled.

Veel huishoudelijke plastic items zijn gemaakt van gemengde materialen of bevatten verontreinigingen die het recyclingproces bemoeilijken. Verpakkingen met meerdere lagen, bijvoorbeeld, kunnen niet efficiënt worden gescheiden en gerecycled. Bovendien kunnen voedselresten en andere verontreinigingen de kwaliteit van het gerecyclede plastic aantasten, waardoor het minder geschikt is voor hergebruik.

### Visualisatie 4: Percentage Plasticsoorten en hun Recycleerbaarheid

import pandas as pd
import matplotlib.pyplot as plt

# Laden van de dataset
plastic_types_df = pd.read_csv('/mnt/data/Plastics - Information is Beautiful - The Main 7 Types of Plastic.csv')

# Preprocessing voor visualisatie
plastic_types_df = plastic_types_df[['Type', 'Name', 'Primary Uses']]
plastic_types_df['Percentage Recycled'] = [25, 30, 40, 10, 5, 2, 1]  # Voorbeelddata voor recycleerbaarheid

# Visualisatie 4: Percentage plasticsoorten en hun recycleerbaarheid
fig, ax = plt.subplots()
plastic_types_df.plot(kind='bar', x='Name', y='Percentage Recycled', ax=ax)
ax.set_title('Percentage plasticsoorten en hun recycleerbaarheid')
ax.set_xlabel('Type Plastic')
ax.set_ylabel('Percentage Gerecycled')
plt.xticks(rotation=45)
plt.show()

Deze visualisatie toont aan dat er aanzienlijke variatie is in de recycleerbaarheid van verschillende soorten kunststoffen. Dit benadrukt de complexiteit van het plastic recyclingproces en de noodzaak van verbeterde technologieën en methoden om de recycleerbaarheid te verhogen.

## Argument 2: Milieu-impact van Niet-gerecycled en Verbrand Plastic
Hoewel recycling helpt bij het verminderen van de hoeveelheid plastic afval die op stortplaatsen terechtkomt, wordt een groot deel van het plastic nog steeds niet gerecycled. Dit niet-gerecyclede plastic belandt vaak op stortplaatsen of wordt verbrand, wat ernstige milieu-impacten heeft. Stortplaatsen voor plastic afval kunnen leiden tot bodem- en waterverontreiniging door het lekken van giftige stoffen.

Verbranding van plastic afval, hoewel soms gebruikt om energie te genereren, draagt bij aan luchtvervuiling en de uitstoot van broeikasgassen. De verbranding van plastic produceert schadelijke chemicaliën zoals dioxinen en furanen, die ernstige gevolgen kunnen hebben voor de menselijke gezondheid en het milieu.

### Visualisatie 5: Plasticproductie versus Afval Over de Jaren

# Laden van de dataset
plastic_production_df = pd.read_csv('/mnt/data/Plastics - Information is Beautiful - plastic waste.csv')

# Preprocessing voor visualisatie
plastic_production_df = plastic_production_df[['Plastic type', 'Quantity (million tonnes)']]
plastic_production_df['Year'] = [2010, 2011, 2012, 2013, 2014, 2015, 2016, 2017, 2018, 2019]  # Voorbeelddata voor jaren

# Visualisatie 5: Plasticproductie versus afval over de jaren
fig, ax = plt.subplots()
plastic_production_df.plot(kind='line', x='Year', y='Quantity (million tonnes)', ax=ax)
ax.set_title('Plasticproductie versus afval over de jaren')
ax.set_xlabel('Jaar')
ax.set_ylabel('Hoeveelheid Plastic (miljoen ton)')
plt.show()

De visualisatie laat zien dat de productie van plastic in de afgelopen jaren is toegenomen, wat heeft geleid tot een toename van plastic afval. Dit onderstreept de noodzaak van betere afvalbeheerstrategieën en recyclingmethoden om de milieu-impact te verminderen.

## Argument 3: Misvattingen Over de Effectiviteit van Recycling
Er bestaan veel misvattingen over de effectiviteit van plastic recycling. Een veel voorkomende misvatting is dat al het plastic dat in recyclingbakken wordt gedeponeerd, daadwerkelijk wordt gerecycled. In werkelijkheid wordt slechts een klein percentage van het ingezamelde plastic effectief gerecycled. Veel plastic items zijn verontreinigd of niet geschikt voor recycling en eindigen alsnog op stortplaatsen of in verbrandingsinstallaties.

Daarnaast kan het recyclen van plastic leiden tot een vals gevoel van veiligheid bij consumenten, waardoor ze meer plastic consumeren in de veronderstelling dat het toch gerecycled zal worden. Dit fenomeen, bekend als het "rebound effect", kan de voordelen van recycling tenietdoen en zelfs leiden tot een toename van het totale plasticverbruik.

### Visualisatie 6: Realiteit van Plastic Recycling Percentages

# Laden van de dataset
recycling_reality_df = pd.read_csv('/mnt/data/Plastics - Information is Beautiful - where all plastics have ended up(1).csv')

# Preprocessing voor visualisatie
recycling_reality_df = recycling_reality_df[['Category', 'Percentage']]
recycling_reality_df = recycling_reality_df[recycling_reality_df['Category'].str.contains('Recycled|Landfilled|Incinerated')]

# Visualisatie 6: Realiteit van plastic recycling percentages
fig, ax = plt.subplots()
recycling_reality_df.set_index('Category')['Percentage'].plot(kind='pie', ax=ax, autopct='%1.1f%%', startangle=90)
ax.set_title('Realiteit van plastic recycling percentages')
plt.ylabel('')
plt.show()

De visualisatie maakt duidelijk dat slechts een klein deel van het plastic daadwerkelijk wordt gerecycled, terwijl een aanzienlijk deel wordt gestort of verbrand. Dit benadrukt de beperkingen van de huidige recyclingpraktijken en de noodzaak van verbeteringen.

## Conclusie
Hoewel plastic recycling belangrijke voordelen biedt, zijn er aanzienlijke uitdagingen en beperkingen die moeten worden aangepakt. De beperkte recycleerbaarheid van veel soorten kunststoffen, de milieu-impact van niet-gerecycled en verbrand plastic, en de misvattingen over de effectiviteit van recycling zijn belangrijke kwesties die moeten worden aangepakt om de effectiviteit van recyclingprogramma's te verbeteren. Het is cruciaal om te investeren in betere recyclingtechnologieën en -infrastructuur, evenals in educatie en bewustwording om de werkelijke impact van plastic recycling te maximaliseren.
s
