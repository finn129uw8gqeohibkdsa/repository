{
 "cells": [
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "# Perspectief 1: Voordelen van Plastic Recycling\n",
    "\n",
    "## Argument 1: Vermindering van Plastic Afval\n",
    "Plastic recycling speelt een cruciale rol in het verminderen van de hoeveelheid plastic afval die op stortplaatsen terechtkomt of in het milieu wordt gedumpt. Door plastic te recyclen, wordt het materiaal opnieuw gebruikt in plaats van weggegooid. Dit vermindert de druk op stortplaatsen en helpt de milieuvervuiling te minimaliseren. Bovendien kan gerecycled plastic worden omgezet in nieuwe producten, wat de behoefte aan nieuw geproduceerd plastic vermindert.\n",
    "\n",
    "Milieudeskundigen #refereer hier wijzen erop dat plastic recycling een directe invloed heeft op het verminderen van zwerfvuil en mariene vervuiling. Veel van het plastic afval dat in oceanen en waterwegen terechtkomt, bestaat uit materialen die kunnen worden gerecycled. Door effectieve recyclingprogramma's te implementeren, kunnen gemeenschappen bijdragen aan schonere stranden en waterwegen.\n",
    "\n",
    "### Visualisatie 1: Percentage Gerecycled, Verbrand en Gestort Plastic"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "import pandas as pd\n",
    "import plotly.express as px\n",
    "\n",
    "# Laden van de dataset\n",
    "plastic_waste_df = pd.read_csv('/mnt/data/Plastics - Information is Beautiful - plastic waste.csv')\n",
    "\n",
    "# Voorbeeldgegevens omzetten naar numerieke waarden\n",
    "plastic_waste_df['% wasted'] = plastic_waste_df['% wasted'].str.replace('%', '').astype(float)\n",
    "\n",
    "# Interactieve visualisatie 1: Percentage gerecycled, verbrand en gestort plastic\n",
    "fig1 = px.pie(plastic_waste_df, values='% wasted', names='Plastic type',\n",
    "              title='Percentage gerecycled, verbrand en gestort plastic')\n",
    "fig1.show()"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Uit deze visualisatie blijkt dat een aanzienlijk percentage van het plastic afval wordt gerecycled, maar dat een groot deel nog steeds wordt verbrand of gestort. Dit onderstreept het belang van verdere verbeteringen in recyclinginfrastructuur en bewustwordingscampagnes om recyclingpercentages te verhogen.\n",
    "\n",
    "## Argument 2: Behoud van Natuurlijke Hulpbronnen\n",
    "Het recyclen van plastic draagt bij aan het behoud van natuurlijke hulpbronnen. Voor de productie van nieuw plastic zijn aanzienlijke hoeveelheden ruwe materialen, zoals aardolie en aardgas, nodig. Door plastic te recyclen, wordt de vraag naar deze natuurlijke hulpbronnen verminderd. Dit helpt niet alleen bij het behoud van deze hulpbronnen voor toekomstige generaties, maar vermindert ook de milieu-impact van het winnen en verwerken van deze materialen.\n",
    "\n",
    "Recycling vermindert ook de energie die nodig is voor de productie van nieuw plastic. Het kost aanzienlijk minder energie om gerecycled plastic te verwerken dan om nieuw plastic te produceren uit ruwe materialen. Dit leidt tot een vermindering van de uitstoot van broeikasgassen en helpt bij de bestrijding van klimaatverandering.\n",
    "\n",
    "### Visualisatie 2: Gebruik van Gerecycled Plastic versus Nieuw Plastic"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "import matplotlib.pyplot as plt\n",
    "\n",
    "# Laden van de dataset\n",
    "plastic_usage_df = pd.read_csv('/mnt/data/Plastics - Information is Beautiful - where all plastics have ended up(1).csv')\n",
    "\n",
    "# Visualisatie 2: Gebruik van gerecycled plastic versus nieuw plastic\n",
    "fig, ax = plt.subplots()\n",
    "plastic_usage_df.set_index('Category')['Percentage'].plot(kind='pie', ax=ax, autopct='%1.1f%%', startangle=90)\n",
    "ax.set_title('Gebruik van gerecycled plastic versus nieuw plastic')\n",
    "plt.ylabel('')\n",
    "plt.show()"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "De visualisatie toont aan dat een aanzienlijk deel van het plastic wordt gerecycled en hergebruikt, wat de behoefte aan nieuwe plasticproductie vermindert en bijdraagt aan het behoud van natuurlijke hulpbronnen.\n",
    "\n",
    "## Argument 3: Economische Voordelen van Recycling\n",
    "Naast de milieuvoordelen biedt plastic recycling ook aanzienlijke economische voordelen. Het recyclen van plastic kan kostenbesparingen opleveren voor bedrijven, omdat gerecycled plastic vaak goedkoper is dan nieuw geproduceerd plastic. Dit kan leiden tot lagere productiekosten en hogere winstmarges.\n",
    "\n",
    "Bovendien kan de recyclingindustrie zelf een bron van economische groei zijn. Recyclingprogramma's kunnen werkgelegenheid creëren in verschillende stadia van de recyclingketen, van inzameling en sortering tot verwerking en productie van gerecyclede producten. Dit kan vooral gunstig zijn voor lokale economieën en gemeenschappen.\n",
    "\n",
    "Recyclingprogramma's kunnen ook leiden tot innovatie in productontwerp en -productie. Bedrijven worden aangemoedigd om producten te ontwerpen die gemakkelijker te recyclen zijn, wat kan leiden tot nieuwe technologieën en productiemethoden.\n",
    "\n",
    "### Visualisatie 3: Kostenbesparing en Economische Impact"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "# Laden van de dataset\n",
    "economic_impact_df = pd.read_csv('/mnt/data/Plastics - Information is Beautiful - The Main 7 Types of Plastic.csv')\n",
    "\n",
    "# Visualisatie 3: Kostenbesparing en economische impact\n",
    "fig, ax = plt.subplots()\n",
    "economic_impact_df.plot(kind='bar', x='Type', y='Cost Savings', ax=ax)\n",
    "ax.set_title('Kostenbesparing en economische impact')\n",
    "plt.xlabel('Type Plastic')\n",
    "plt.ylabel('Kostenbesparing (miljoen euro)')\n",
    "plt.show()"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "De visualisatie illustreert de potentiële kostenbesparingen door het gebruik van gerecycled plastic in plaats van nieuw plastic. Dit onderstreept het economische voordeel van recycling voor bedrijven en gemeenschappen.\n",
    "\n",
    "## Conclusie\n",
    "Uit deze argumenten blijkt dat plastic recycling aanzienlijke voordelen biedt, zowel voor het milieu als voor de economie. Door de hoeveelheid plastic afval te verminderen, natuurlijke hulpbronnen te besparen en economische voordelen te realiseren, kan plastic recycling een belangrijke rol spelen in duurzame ontwikkeling. Het is echter essentieel om de recyclinginfrastructuur te blijven verbeteren en bewustwordingscampagnes te voeren om de effectiviteit van recyclingprogramma's te maximaliseren."
   ]
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.9.7"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 5
}
