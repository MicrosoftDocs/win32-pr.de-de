---
description: Die Unicode-Teilmenge Bitfeldern (USA) werden in der fontSignature-und der LOCALESIGNATURE-Struktur verwendet.
ms.assetid: f897dfc7-3e78-48dc-8d3d-6929e2f4ec4d
title: Unicode-Teilmenge Bitfields
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fced251b1bf8e04dd4c0d7d7cb0dca15c8bdfa6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364070"
---
# <a name="unicode-subset-bitfields"></a>Unicode-Teilmenge Bitfields

Die Unicode-Teilmenge Bitfeldern (USA) werden in der [**fontSignature**](/windows/win32/api/wingdi/ns-wingdi-fontsignature) -und der [**LOCALESIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-localesignature) -Struktur verwendet.



<table>
<thead>
<tr class="header">
<th>bit</th>
<th>Unicode-Unterbereich</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0</td>
<td>0000 - 007F</td>
<td>Basis-lateinisch</td>
</tr>
<tr class="even">
<td>1</td>
<td>0080 - 00FF</td>
<td>Lateinisch-1 Ergänzung</td>
</tr>
<tr class="odd">
<td>2</td>
<td>0100 - 017F</td>
<td>Lateinisch, erweitert-A</td>
</tr>
<tr class="even">
<td>3</td>
<td>0180 - 024F</td>
<td>Lateinisch, erweitert-B</td>
</tr>
<tr class="odd">
<td rowspan="3">4 $ {Remove} $<br />
</td>
<td>0250 - 02AF</td>
<td>IPA-Erweiterungen</td>
</tr>
<tr class="even">
<td>1D00 - 1D7F</td>
<td>Phonetische Erweiterungen</td>

</tr>
<tr class="odd">
<td>1D80-1dbf</td>
<td>Ergänzung zu phonetischen Erweiterungen</td>

</tr>
<tr class="even">
<td rowspan="2">5 $ {Remove} $<br />
</td>
<td>02B0 - 02FF</td>
<td>Abstands-modifiziererbuch staben</td>
</tr>
<tr class="odd">
<td>A700-A71F</td>
<td>Modifizierertonbuch staben</td>

</tr>
<tr class="even">
<td rowspan="2">6 $ {Remove} $<br />
</td>
<td>0300 - 036F</td>
<td>Kombinieren von diakritischen Markierungen</td>
</tr>
<tr class="odd">
<td>1dc0-1 DFF</td>
<td>Ergänzen der Ergänzung von diakritischen Markierungen</td>

</tr>
<tr class="even">
<td>7</td>
<td>0370 - 03FF</td>
<td>Griechisch und Koptisch</td>
</tr>
<tr class="odd">
<td>8</td>
<td>2c80-2CFF</td>
<td>Koptisch</td>
</tr>
<tr class="even">
<td rowspan="4">9 $ {Remove} $<br />
</td>
<td>0400 - 04FF</td>
<td>Kyrillisch</td>
</tr>
<tr class="odd">
<td>0500 - 052F</td>
<td>Cyrillic-Ergänzung</td>

</tr>
<tr class="even">
<td>2de 0-2dff</td>
<td>Kyrillisch erweitert-A</td>

</tr>
<tr class="odd">
<td>A640 - A69F</td>
<td>Kyrillisch erweitert-B</td>

</tr>
<tr class="even">
<td>10</td>
<td>0530 - 058F</td>
<td>Armenisch</td>
</tr>
<tr class="odd">
<td>11</td>
<td>0590 - 05FF</td>
<td>Hebräisch</td>
</tr>
<tr class="even">
<td>12</td>
<td>A500-A63F</td>
<td>Vai</td>
</tr>
<tr class="odd">
<td rowspan="2">13 $ {Remove} $<br />
</td>
<td>0600 - 06FF</td>
<td>Arabisch</td>
</tr>
<tr class="even">
<td>0750-077f</td>
<td>Arabische Ergänzung</td>

</tr>
<tr class="odd">
<td>14</td>
<td>07c0-07FF</td>
<td>Nko</td>
</tr>
<tr class="even">
<td>15</td>
<td>0900 - 097F</td>
<td>Devanagari</td>
</tr>
<tr class="odd">
<td>16</td>
<td>0980 - 09FF</td>
<td>Bengalisch</td>
</tr>
<tr class="even">
<td>17</td>
<td>0A00 - 0A7F</td>
<td>Gurmukhi</td>
</tr>
<tr class="odd">
<td>18</td>
<td>0A80 - 0AFF</td>
<td>Gujarati</td>
</tr>
<tr class="even">
<td>19</td>
<td>0B00 - 0B7F</td>
<td>Odia</td>
</tr>
<tr class="odd">
<td>20</td>
<td>0B80 - 0BFF</td>
<td>Tamilisch</td>
</tr>
<tr class="even">
<td>21</td>
<td>0C00 - 0C7F</td>
<td>Telugu</td>
</tr>
<tr class="odd">
<td>22</td>
<td>0C80 - 0CFF</td>
<td>Kannada</td>
</tr>
<tr class="even">
<td>23</td>
<td>0D00 - 0D7F</td>
<td>Malayalam</td>
</tr>
<tr class="odd">
<td>24</td>
<td>0E00 - 0E7F</td>
<td>Thailändisch</td>
</tr>
<tr class="even">
<td>25</td>
<td>0E80 - 0EFF</td>
<td>Laotisch</td>
</tr>
<tr class="odd">
<td rowspan="2">26 $ {Remove} $<br />
</td>
<td>10A0 - 10FF</td>
<td>Georgisch</td>
</tr>
<tr class="even">
<td>2d00-2d2f</td>
<td>Georgische Ergänzung</td>

</tr>
<tr class="odd">
<td>27</td>
<td>1b00-1b7f</td>
<td>Balinesisch</td>
</tr>
<tr class="even">
<td>28</td>
<td>1100 - 11FF</td>
<td>Hangul Jamo</td>
</tr>
<tr class="odd">
<td rowspan="3">29 $ {Remove} $<br />
</td>
<td>1E00 - 1EFF</td>
<td>Lateinisch erweitert zusätzlich</td>
</tr>
<tr class="even">
<td>2c60-2c7f</td>
<td>Lateinisch erweitert-C</td>

</tr>
<tr class="odd">
<td>A720 - A7FF</td>
<td>Lateinisch, erweitert-D</td>

</tr>
<tr class="even">
<td>30</td>
<td>1F00 - 1FFF</td>
<td>Griechisch (erweitert)</td>
</tr>
<tr class="odd">
<td rowspan="2">31 $ {Remove} $<br />
</td>
<td>2000 - 206F</td>
<td>Allgemeine Interpunktions Zeichen</td>
</tr>
<tr class="even">
<td>2e00-2e7f</td>
<td>Zusätzliches Interpunktions Zeichen</td>

</tr>
<tr class="odd">
<td>32</td>
<td>2070 - 209F</td>
<td>Hoch-und tief gestellte Skripts</td>
</tr>
<tr class="even">
<td>33</td>
<td>20A0 - 20CF</td>
<td>Währungssymbole</td>
</tr>
<tr class="odd">
<td>34</td>
<td>20D0 - 20FF</td>
<td>Kombinieren von diakritischen Markierungen für Symbole</td>
</tr>
<tr class="even">
<td>35</td>
<td>2100 - 214F</td>
<td>Letterlike-Symbole</td>
</tr>
<tr class="odd">
<td>36</td>
<td>2150 - 218F</td>
<td>Zahlen Formulare</td>
</tr>
<tr class="even">
<td rowspan="4">37 $ {Remove} $<br />
</td>
<td>2190 - 21FF</td>
<td>Pfeile</td>
</tr>
<tr class="odd">
<td>27F0 - 27FF</td>
<td>Ergänzende Pfeile-A</td>

</tr>
<tr class="even">
<td>2900 - 297F</td>
<td>Ergänzende Pfeile-B</td>

</tr>
<tr class="odd">
<td>2B00 - 2BFF</td>
<td>Verschiedene Symbole und Pfeile</td>

</tr>
<tr class="even">
<td rowspan="4">38 $ {Remove} $<br />
</td>
<td>2200 - 22FF</td>
<td>Mathematische Operatoren</td>
</tr>
<tr class="odd">
<td>27C0 - 27EF</td>
<td>Verschiedene mathematische Symbole-A</td>

</tr>
<tr class="even">
<td>2980 - 29FF</td>
<td>Verschiedene mathematische Symbole-B</td>

</tr>
<tr class="odd">
<td>2A00 - 2AFF</td>
<td>Ergänzende mathematische Operatoren</td>

</tr>
<tr class="even">
<td>39</td>
<td>2300 - 23FF</td>
<td>Sonstige technische</td>
</tr>
<tr class="odd">
<td>40</td>
<td>2400 - 243F</td>
<td>Steuerelement Bilder</td>
</tr>
<tr class="even">
<td>41</td>
<td>2440 - 245F</td>
<td>Optische Zeichenerkennung</td>
</tr>
<tr class="odd">
<td>42</td>
<td>2460 - 24FF</td>
<td>Eingeschlossene alphanumerische Zeichen</td>
</tr>
<tr class="even">
<td>43</td>
<td>2500 - 257F</td>
<td>Box-Zeichnung</td>
</tr>
<tr class="odd">
<td>44</td>
<td>2580 - 259F</td>
<td>Block Elemente</td>
</tr>
<tr class="even">
<td>45</td>
<td>25A0 - 25FF</td>
<td>Geometrische Formen</td>
</tr>
<tr class="odd">
<td>46</td>
<td>2600 - 26FF</td>
<td>Verschiedene Symbole</td>
</tr>
<tr class="even">
<td>47</td>
<td>2700 - 27BF</td>
<td>Dingbats</td>
</tr>
<tr class="odd">
<td>48</td>
<td>3000 - 303F</td>
<td>CJK-Symbole und-Interpunktions Zeichen</td>
</tr>
<tr class="even">
<td>49</td>
<td>3040 - 309F</td>
<td>Hiragana</td>
</tr>
<tr class="odd">
<td rowspan="2">50 $ {Remove} $<br />
</td>
<td>30A0 - 30FF</td>
<td>Katakana</td>
</tr>
<tr class="even">
<td>31F0 - 31FF</td>
<td>Katakana-phonetische Erweiterungen</td>

</tr>
<tr class="odd">
<td rowspan="2">51 $ {Remove} $<br />
</td>
<td>3100 - 312F</td>
<td>Bopomofo</td>
</tr>
<tr class="even">
<td>31A0 - 31BF</td>
<td>Bopomofo erweitert</td>

</tr>
<tr class="odd">
<td>52</td>
<td>3130 - 318F</td>
<td>Hangul Compatibility Jamo</td>
</tr>
<tr class="even">
<td>53</td>
<td>A840 - A87F</td>
<td>Phags-pa</td>
</tr>
<tr class="odd">
<td>54</td>
<td>3200 - 32FF</td>
<td>Eingeschlossene cjk-Buchstaben und Monate</td>
</tr>
<tr class="even">
<td>55</td>
<td>3300 - 33FF</td>
<td>CJK-Kompatibilität</td>
</tr>
<tr class="odd">
<td>56</td>
<td>AC00 - D7AF</td>
<td>Hangul-Silben</td>
</tr>
<tr class="even">
<td>57</td>
<td>D800 und-DFFF</td>
<td>Nicht-Ebene 0. Beachten Sie, dass das Festlegen dieses Bits impliziert, dass es mindestens einen ergänzenden Code Punkt gibt, der hinter der von dieser Schriftart unterstützten grundlegenden mehrdimensionalen Ebene (BMP) liegt. Weitere Informationen finden Sie unter <a href="surrogates-and-supplementary-characters.md">Surrogates und ergänzende Zeichen</a>.</td>
</tr>
<tr class="odd">
<td>58</td>
<td>10900-1091f</td>
<td>Phönizischen</td>
</tr>
<tr class="even">
<td rowspan="7">59 $ {Remove} $<br />
</td>
<td>2E80 - 2EFF</td>
<td>Ergänzung zu cjk-radikalen</td>
</tr>
<tr class="odd">
<td>2F00 - 2FDF</td>
<td>Kangxi-radikale</td>

</tr>
<tr class="even">
<td>2FF0 - 2FFF</td>
<td>Ideografische Beschreibungs Zeichen</td>

</tr>
<tr class="odd">
<td>3190 - 319F</td>
<td>Kanbun</td>

</tr>
<tr class="even">
<td>3400 - 4DBF</td>
<td>CJK Unified Ideographs Extension A</td>

</tr>
<tr class="odd">
<td>4E00 - 9FFF</td>
<td>Einheitliche cjk-Ideographen</td>

</tr>
<tr class="even">
<td>20000-2a6df</td>
<td>CJK Unified Ideographs Extension B</td>

</tr>
<tr class="odd">
<td>60</td>
<td>E000 - F8FF</td>
<td>Privater Verwendungsbereich</td>
</tr>
<tr class="even">
<td rowspan="3">61 $ {Remove} $<br />
</td>
<td>31c0 bis 31ef</td>
<td>CJK-Striche</td>
</tr>
<tr class="odd">
<td>F900 - FAFF</td>
<td>CJK-Kompatibilitäts Ideographs</td>

</tr>
<tr class="even">
<td>2F 800-2fa1f</td>
<td>Ergänzung der CJK-Kompatibilitäts Ideographs</td>

</tr>
<tr class="odd">
<td>62</td>
<td>FB00 - FB4F</td>
<td>Alphabetische Präsentations Formulare</td>
</tr>
<tr class="even">
<td>63</td>
<td>FB50 - FDFF</td>
<td>Arabische Präsentations Formulare-A</td>
</tr>
<tr class="odd">
<td>64</td>
<td>FE20 - FE2F</td>
<td>Kombinieren von halb Markierungen</td>
</tr>
<tr class="even">
<td rowspan="2">65 $ {Remove} $<br />
</td>
<td>FE10 - FE1F</td>
<td>Vertikale Formulare</td>
</tr>
<tr class="odd">
<td>FE30 - FE4F</td>
<td>CJK-Kompatibilitäts Formulare</td>

</tr>
<tr class="even">
<td>66</td>
<td>FE50 - FE6F</td>
<td>Kleine Formular Varianten</td>
</tr>
<tr class="odd">
<td>67</td>
<td>FE70 - FEFF</td>
<td>Arabische Präsentations Formulare-B</td>
</tr>
<tr class="even">
<td>68</td>
<td>FF00 - FFEF</td>
<td>Halfwidth-und Fullwidth-Formulare</td>
</tr>
<tr class="odd">
<td>69</td>
<td>FFF0 - FFFF</td>
<td>Spezi</td>
</tr>
<tr class="even">
<td>70</td>
<td>0F00 - 0FFF</td>
<td>Tibetisch</td>
</tr>
<tr class="odd">
<td>71</td>
<td>0700 - 074F</td>
<td>Syrisch</td>
</tr>
<tr class="even">
<td>72</td>
<td>0780 - 07BF</td>
<td>Thaana</td>
</tr>
<tr class="odd">
<td>73</td>
<td>0D80 - 0DFF</td>
<td>Singhalesisch</td>
</tr>
<tr class="even">
<td>74</td>
<td>1000 - 109F</td>
<td>Myanmar</td>
</tr>
<tr class="odd">
<td rowspan="3">75 $ {Remove} $<br />
</td>
<td>1200 - 137F</td>
<td>Ethiopic</td>
</tr>
<tr class="even">
<td>1380-139 f</td>
<td>Äthiopische Ergänzung</td>

</tr>
<tr class="odd">
<td>2d80-2ddf</td>
<td>Äthiopisch erweitert</td>

</tr>
<tr class="even">
<td>76</td>
<td>13A0 - 13FF</td>
<td>Cherokee</td>
</tr>
<tr class="odd">
<td>77</td>
<td>1400 - 167F</td>
<td>Einheitliche kanadische Aborigines-Silben</td>
</tr>
<tr class="even">
<td>78</td>
<td>1680 - 169F</td>
<td>Ogam</td>
</tr>
<tr class="odd">
<td>79</td>
<td>16A0 - 16FF</td>
<td>Runisch</td>
</tr>
<tr class="even">
<td rowspan="2">80 $ {Remove} $<br />
</td>
<td>1780 - 17FF</td>
<td>Khmer</td>
</tr>
<tr class="odd">
<td>19E0 - 19FF</td>
<td>Khmer-Symbole</td>

</tr>
<tr class="even">
<td>81</td>
<td>1800 - 18AF</td>
<td>Mongolisch</td>
</tr>
<tr class="odd">
<td>82</td>
<td>2800 - 28FF</td>
<td>Braillemuster</td>
</tr>
<tr class="even">
<td rowspan="2">83 $ {Remove} $<br />
</td>
<td>A000 - A48F</td>
<td>Yi-Silben</td>
</tr>
<tr class="odd">
<td>A490 - A4CF</td>
<td>Yi-Radikale</td>

</tr>
<tr class="even">
<td rowspan="4">84 $ {Remove} $<br />
</td>
<td>1700 - 171F</td>
<td>Tagalog</td>
</tr>
<tr class="odd">
<td>1720 - 173F</td>
<td>Hanunoo</td>

</tr>
<tr class="even">
<td>1740 - 175F</td>
<td>Buhid</td>

</tr>
<tr class="odd">
<td>1760 - 177F</td>
<td>Tagbanwa</td>

</tr>
<tr class="even">
<td>85</td>
<td>10300-1032f</td>
<td>Alte kursiv Formatierung</td>
</tr>
<tr class="odd">
<td>86</td>
<td>10330-1034F</td>
<td>Go</td>
</tr>
<tr class="even">
<td>87</td>
<td>10400-1044f</td>
<td>Deseret</td>
</tr>
<tr class="odd">
<td rowspan="3">88 $ {Remove} $<br />
</td>
<td>1 D000-1 D0FF</td>
<td>Byzantinische Musik Symbole</td>
</tr>
<tr class="even">
<td>1D100-1D1FF</td>
<td>Musik Symbole</td>

</tr>
<tr class="odd">
<td>1d200-1d24f</td>
<td>Alte griechische Musik Notation</td>

</tr>
<tr class="even">
<td>89</td>
<td>1d400-1d7ff</td>
<td>Mathematische alphanumerische Symbole</td>
</tr>
<tr class="odd">
<td rowspan="2">90 $ {Remove} $<br />
</td>
<td>FF000-ffffd</td>
<td>Private Verwendung (Ebene 15)</td>
</tr>
<tr class="even">
<td>100000-10fffd</td>
<td>Private Verwendung (Ebene 16)</td>

</tr>
<tr class="odd">
<td rowspan="2">91 $ {Remove} $<br />
</td>
<td>FE00 - FE0F</td>
<td>Variierungsselektoren</td>
</tr>
<tr class="even">
<td>E0100 - E01EF</td>
<td>Ergänzung der variabselectoren</td>

</tr>
<tr class="odd">
<td>92</td>
<td>E0000 - E007F</td>
<td>`Tags`</td>
</tr>
<tr class="even">
<td>93</td>
<td>1900 - 194F</td>
<td>Limbu</td>
</tr>
<tr class="odd">
<td>94</td>
<td>1950 - 197F</td>
<td>Tai-Le</td>
</tr>
<tr class="even">
<td>95</td>
<td>1980-19DF</td>
<td>Neue Tai-Lue</td>
</tr>
<tr class="odd">
<td>96</td>
<td>1a00-1A1F</td>
<td>Buginesisch</td>
</tr>
<tr class="even">
<td>97</td>
<td>2c00-2c5f</td>
<td>Glagolitisch</td>
</tr>
<tr class="odd">
<td>98</td>
<td>2D30-2d7f</td>
<td>Tifinagh</td>
</tr>
<tr class="even">
<td>99</td>
<td>4DC0 - 4DFF</td>
<td>Yijing-hexrammsymbole</td>
</tr>
<tr class="odd">
<td>100</td>
<td>A800 - A82F</td>
<td>Syloti Nagri</td>
</tr>
<tr class="even">
<td rowspan="3">101 $ {Remove} $<br />
</td>
<td>10000-1007f</td>
<td>Lineare B-Silben</td>
</tr>
<tr class="odd">
<td>10080-100 FF</td>
<td>Lineare B-Ideogramme</td>

</tr>
<tr class="even">
<td>10100-1013f</td>
<td>Ägäis-Nummern</td>

</tr>
<tr class="odd">
<td>102</td>
<td>10140-1018f</td>
<td>Alte griechische Zahlen</td>
</tr>
<tr class="even">
<td>103</td>
<td>10380-1039f</td>
<td>Ugaritisch</td>
</tr>
<tr class="odd">
<td>104</td>
<td>103 a0-103 DF</td>
<td>Alte persische</td>
</tr>
<tr class="even">
<td>105</td>
<td>10450-1047f</td>
<td>Shavian</td>
</tr>
<tr class="odd">
<td>106</td>
<td>10480-104af</td>
<td>Osmanya</td>
</tr>
<tr class="even">
<td>107</td>
<td>10800-1083f</td>
<td>Zypriotische silabäre</td>
</tr>
<tr class="odd">
<td>108</td>
<td>10a00-10a5f</td>
<td>Kharoshthi</td>
</tr>
<tr class="even">
<td>109</td>
<td>1d300-1d35f</td>
<td>Tai Xuan Jing-Symbole</td>
</tr>
<tr class="odd">
<td rowspan="2">110 $ {Remove} $<br />
</td>
<td>12000-123FF</td>
<td>Cuneiform</td>
</tr>
<tr class="even">
<td>12400-1247f</td>
<td>Cuneiform-Zahlen und-Satzzeichen</td>

</tr>
<tr class="odd">
<td>111</td>
<td>1d360-1d37f</td>
<td>Zählen von Strich Ziffern</td>
</tr>
<tr class="even">
<td>112</td>
<td>1b80-1bbf</td>
<td>Sundanesisch</td>
</tr>
<tr class="odd">
<td>113</td>
<td>1c00-1c4f</td>
<td>Lepcha</td>
</tr>
<tr class="even">
<td>114</td>
<td>1c50-1c7f</td>
<td>Ol Chiki</td>
</tr>
<tr class="odd">
<td>115</td>
<td>A880 - A8DF</td>
<td>Saurashtra</td>
</tr>
<tr class="even">
<td>116</td>
<td>A900-A92F</td>
<td>Kayah Li</td>
</tr>
<tr class="odd">
<td>117</td>
<td>A930 - A95F</td>
<td>Rejang</td>
</tr>
<tr class="even">
<td>118</td>
<td>AA00 - AA5F</td>
<td>Gar</td>
</tr>
<tr class="odd">
<td>119</td>
<td>10190-101 CF</td>
<td>Alte Symbole</td>
</tr>
<tr class="even">
<td>120</td>
<td>101d0-101 ff</td>
<td>Phaistos-CD</td>
</tr>
<tr class="odd">
<td rowspan="3">121 $ {Remove} $<br />
</td>
<td>10280-1029f</td>
<td>Lykisch</td>
</tr>
<tr class="even">
<td>102a0-102df</td>
<td>Karisch</td>

</tr>
<tr class="odd">
<td>10920-1093f</td>
<td>Lydisch</td>

</tr>
<tr class="even">
<td rowspan="2">122 $ {Remove} $<br />
</td>
<td>1F-1F</td>
<td>Mahjong-Kacheln</td>
</tr>
<tr class="odd">
<td>1F 030-1F 09F</td>
<td>Domino-Kacheln</td>

</tr>
<tr class="even">
<td>123</td>

<td><strong>Windows 2000 und höher:</strong> Layoutfortschritt, horizontal von rechts nach links</td>
</tr>
<tr class="odd">
<td>124</td>

<td><strong>Windows 2000 und höher:</strong> Layoutfortschritt, vertikal vor horizontal</td>
</tr>
<tr class="even">
<td>125</td>

<td><strong>Windows 2000 und höher:</strong> Layoutfortschritt, vertikal von unten nach oben</td>
</tr>
<tr class="odd">
<td>126-127</td>

<td>Reserviert für Prozess interne Verwendung</td>
</tr>
</tbody>
</table>



 

 

 



