---
description: Die Unicode-Teilmengenbitfelder (USBs) werden in den Strukturen FONTSIGNATURE und LOCALESIGNATURE verwendet.
ms.assetid: f897dfc7-3e78-48dc-8d3d-6929e2f4ec4d
title: Unicode-Teilmengenbitfelder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f0fa4791e62f397e62a99a78d41dbcdc67c55299a650b1bc78bea685205399
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787990"
---
# <a name="unicode-subset-bitfields"></a>Unicode-Teilmengenbitfelder

Die Unicode-Teilmengenbitfelder (USBs) werden in den [**Strukturen FONTSIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-fontsignature) und [**LOCALESIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-localesignature) verwendet.



<table>
<thead>
<tr class="header">
<th>bit</th>
<th>Unicode-Unterbereich</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0</td>
<td>0000 - 007F</td>
<td>Grundlegendes Lateinisch</td>
</tr>
<tr class="even">
<td>1</td>
<td>0080 - 00FF</td>
<td>Latin-1 Supplement</td>
</tr>
<tr class="odd">
<td>2</td>
<td>0100 - 017F</td>
<td>Latin Extended-A</td>
</tr>
<tr class="even">
<td>3</td>
<td>0180 - 024F</td>
<td>Lateinisch Erweitert-B</td>
</tr>
<tr class="odd">
<td rowspan="3">4${REMOVE}$<br />
</td>
<td>0250 - 02AF</td>
<td>IPA-Erweiterungen</td>
</tr>
<tr class="even">
<td>1D00 - 1D7F</td>
<td>Phonetische Erweiterungen</td>

</tr>
<tr class="odd">
<td>1D80 – 1DBF</td>
<td>Phonetische Erweiterungsergänzung</td>

</tr>
<tr class="even">
<td rowspan="2">5${REMOVE}$<br />
</td>
<td>02B0 - 02FF</td>
<td>Abstandsmodifiziererbuchstaben</td>
</tr>
<tr class="odd">
<td>A700 – A71F</td>
<td>Modifizierertonbuchstaben</td>

</tr>
<tr class="even">
<td rowspan="2">6${REMOVE}$<br />
</td>
<td>0300 - 036F</td>
<td>Kombinieren diakritischer Markierungen</td>
</tr>
<tr class="odd">
<td>1DC0 - 1DFF</td>
<td>Kombinieren der Ergänzung zu diakritischen Markierungen</td>

</tr>
<tr class="even">
<td>7</td>
<td>0370 - 03FF</td>
<td>Griechisch und Koptisch</td>
</tr>
<tr class="odd">
<td>8</td>
<td>2C80 - 2CFF</td>
<td>Koptisch</td>
</tr>
<tr class="even">
<td rowspan="4">9${REMOVE}$<br />
</td>
<td>0400 - 04FF</td>
<td>Kyrillisch</td>
</tr>
<tr class="odd">
<td>0500 - 052F</td>
<td>Kyrillische Ergänzung</td>

</tr>
<tr class="even">
<td>2DE0 – 2DFF</td>
<td>Kyrillisch Erweitert-A</td>

</tr>
<tr class="odd">
<td>A640 – A69F</td>
<td>Kyrillisch Extended-B</td>

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
<td>A500 – A63F</td>
<td>Vai</td>
</tr>
<tr class="odd">
<td rowspan="2">13${REMOVE}$<br />
</td>
<td>0600 - 06FF</td>
<td>Arabisch</td>
</tr>
<tr class="even">
<td>0750 - 077F</td>
<td>Arabische Ergänzung</td>

</tr>
<tr class="odd">
<td>14</td>
<td>07C0 - 07FF</td>
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
<td rowspan="2">26${REMOVE}$<br />
</td>
<td>10A0 - 10FF</td>
<td>Georgisch</td>
</tr>
<tr class="even">
<td>2D00 – 2D2F</td>
<td>Supplement (Ergänzen)</td>

</tr>
<tr class="odd">
<td>27</td>
<td>1B00 bis 1B7F</td>
<td>Balinesisch</td>
</tr>
<tr class="even">
<td>28</td>
<td>1100 - 11FF</td>
<td>Hangul Jamo</td>
</tr>
<tr class="odd">
<td rowspan="3">29${REMOVE}$<br />
</td>
<td>1E00 - 1EFF</td>
<td>Latin Extended Additional</td>
</tr>
<tr class="even">
<td>2C60 - 2C7F</td>
<td>Lateinisch Erweitert-C</td>

</tr>
<tr class="odd">
<td>A720 – A7FF</td>
<td>Lateinisch Erweitert-D</td>

</tr>
<tr class="even">
<td>30</td>
<td>1F00 - 1FFF</td>
<td>Griechisch (erweitert)</td>
</tr>
<tr class="odd">
<td rowspan="2">31${REMOVE}$<br />
</td>
<td>2000 - 206F</td>
<td>Allgemeine Interpunktion</td>
</tr>
<tr class="even">
<td>2E00 - 2E7F</td>
<td>Zusätzliche Interpunktion</td>

</tr>
<tr class="odd">
<td>32</td>
<td>2070 - 209F</td>
<td>Hoch- und Unterskripts</td>
</tr>
<tr class="even">
<td>33</td>
<td>20A0 - 20CF</td>
<td>Währungssymbole</td>
</tr>
<tr class="odd">
<td>34</td>
<td>20D0 - 20FF</td>
<td>Kombinieren diakritischer Markierungen für Symbole</td>
</tr>
<tr class="even">
<td>35</td>
<td>2100 - 214F</td>
<td>Buchstabenähnliche Symbole</td>
</tr>
<tr class="odd">
<td>36</td>
<td>2150 - 218F</td>
<td>Zahlenformulare</td>
</tr>
<tr class="even">
<td rowspan="4">37${REMOVE}$<br />
</td>
<td>2190 - 21FF</td>
<td>Pfeile</td>
</tr>
<tr class="odd">
<td>27F0 - 27FF</td>
<td>Zusätzliche Pfeile –A</td>

</tr>
<tr class="even">
<td>2900 - 297F</td>
<td>Zusätzliche Pfeile-B</td>

</tr>
<tr class="odd">
<td>2B00 - 2BFF</td>
<td>Verschiedene Symbole und Pfeile</td>

</tr>
<tr class="even">
<td rowspan="4">38${REMOVE}$<br />
</td>
<td>2200 - 22FF</td>
<td>Mathematische Operatoren</td>
</tr>
<tr class="odd">
<td>27C0 - 27EF</td>
<td>Verschiedene mathematische Symbole –A</td>

</tr>
<tr class="even">
<td>2980 - 29FF</td>
<td>Verschiedene mathematische Symbole–B</td>

</tr>
<tr class="odd">
<td>2A00 - 2AFF</td>
<td>Ergänzende mathematische Operatoren</td>

</tr>
<tr class="even">
<td>39</td>
<td>2300 - 23FF</td>
<td>Sonstige technische Aspekte</td>
</tr>
<tr class="odd">
<td>40</td>
<td>2400 - 243F</td>
<td>Steuerelementbilder</td>
</tr>
<tr class="even">
<td>41</td>
<td>2440 - 245F</td>
<td>Optische Zeichenerkennung</td>
</tr>
<tr class="odd">
<td>42</td>
<td>2460 - 24FF</td>
<td>Eingeschlossene alphanumerische Daten</td>
</tr>
<tr class="even">
<td>43</td>
<td>2500 - 257F</td>
<td>Box Drawing</td>
</tr>
<tr class="odd">
<td>44</td>
<td>2580 - 259F</td>
<td>Blockelemente</td>
</tr>
<tr class="even">
<td>45</td>
<td>25A0 - 25FF</td>
<td>Geometrische Formen</td>
</tr>
<tr class="odd">
<td>46</td>
<td>2600 - 26FF</td>
<td>Sonstige Symbole</td>
</tr>
<tr class="even">
<td>47</td>
<td>2700 - 27BF</td>
<td>Dingbats</td>
</tr>
<tr class="odd">
<td>48</td>
<td>3000 - 303F</td>
<td>CJK-Symbole und Interpunktion</td>
</tr>
<tr class="even">
<td>49</td>
<td>3040 - 309F</td>
<td>Hiragana</td>
</tr>
<tr class="odd">
<td rowspan="2">50${REMOVE}$<br />
</td>
<td>30A0 - 30FF</td>
<td>Katakana</td>
</tr>
<tr class="even">
<td>31F0 - 31FF</td>
<td>Katakana Phonetic Extensions</td>

</tr>
<tr class="odd">
<td rowspan="2">51${REMOVE}$<br />
</td>
<td>3100 - 312F</td>
<td>Bopomofo</td>
</tr>
<tr class="even">
<td>31A0 - 31BF</td>
<td>Bopomofo Extended</td>

</tr>
<tr class="odd">
<td>52</td>
<td>3130 - 318F</td>
<td>Hangul Compatibility Jamo</td>
</tr>
<tr class="even">
<td>53</td>
<td>A840 – A87F</td>
<td>Paws-pa</td>
</tr>
<tr class="odd">
<td>54</td>
<td>3200 - 32FF</td>
<td>Eingeschlossene CJK-Buchstaben und -Monate</td>
</tr>
<tr class="even">
<td>55</td>
<td>3300 - 33FF</td>
<td>CJK-Kompatibilität</td>
</tr>
<tr class="odd">
<td>56</td>
<td>AC00 - D7AF</td>
<td>Hangul Sillables</td>
</tr>
<tr class="even">
<td>57</td>
<td>D800 – DFFF</td>
<td>Nichtebene 0. Beachten Sie, dass das Festlegen dieses Bit impliziert, dass mindestens ein zusätzlicher Codepunkt über die grundlegende mehrsprachige Ebene (Basic Multilingual Plane, BMP) hinaus liegt, die von dieser Schriftart unterstützt wird. Weitere Informationen <a href="surrogates-and-supplementary-characters.md">finden Sie unter Ersatzzeichen und ergänzende Zeichen.</a></td>
</tr>
<tr class="odd">
<td>58</td>
<td>10900 - 1091F</td>
<td>Phönizischen</td>
</tr>
<tr class="even">
<td rowspan="7">59${REMOVE}$<br />
</td>
<td>2E80 - 2EFF</td>
<td>Ergänzung zu CJK-Neukern</td>
</tr>
<tr class="odd">
<td>2F00 - 2FDF</td>
<td>Kangxi-Radikale</td>

</tr>
<tr class="even">
<td>2FF0 - 2FFF</td>
<td>Ideografische Beschreibungszeichen</td>

</tr>
<tr class="odd">
<td>3190 - 319F</td>
<td>Kanbun</td>

</tr>
<tr class="even">
<td>3400 - 4DBF</td>
<td>CJK Unified Ideogramms Extension A</td>

</tr>
<tr class="odd">
<td>4E00 - 9FFF</td>
<td>Einheitliche CJK-Ideogramme</td>

</tr>
<tr class="even">
<td>20000 – 2A6DF</td>
<td>CJK Unified Ideogramms Extension B</td>

</tr>
<tr class="odd">
<td>60</td>
<td>E000 - F8FF</td>
<td>Privater Nutzungsbereich</td>
</tr>
<tr class="even">
<td rowspan="3">61${REMOVE}$<br />
</td>
<td>31C0 - 31EF</td>
<td>CJK-Striche</td>
</tr>
<tr class="odd">
<td>F900 - FAFF</td>
<td>CJK-Kompatibilitätsideogramme</td>

</tr>
<tr class="even">
<td>2F800 – 2FA1F</td>
<td>Ergänzung zu CJK-Kompatibilitäts-Ideogrammen</td>

</tr>
<tr class="odd">
<td>62</td>
<td>FB00 - FB4F</td>
<td>Alphabetische Präsentationsformen</td>
</tr>
<tr class="even">
<td>63</td>
<td>FB50 - FDFF</td>
<td>Arabische Präsentationsformulare–A</td>
</tr>
<tr class="odd">
<td>64</td>
<td>FE20 - FE2F</td>
<td>Kombinieren von Halbmarkierungen</td>
</tr>
<tr class="even">
<td rowspan="2">65${REMOVE}$<br />
</td>
<td>FE10 – FE1F</td>
<td>Vertikale Formen</td>
</tr>
<tr class="odd">
<td>FE30 - FE4F</td>
<td>CJK-Kompatibilitätsformulare</td>

</tr>
<tr class="even">
<td>66</td>
<td>FE50 - FE6F</td>
<td>Kleine Formularvarianten</td>
</tr>
<tr class="odd">
<td>67</td>
<td>FE70 - FEFF</td>
<td>Arabische Präsentationsformulare-B</td>
</tr>
<tr class="even">
<td>68</td>
<td>FF00 - FFEF</td>
<td>Halfwidth- und Fullwidth-Formulare</td>
</tr>
<tr class="odd">
<td>69</td>
<td>FFF0 - FFFF</td>
<td>Specials</td>
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
<td rowspan="3">75${REMOVE}$<br />
</td>
<td>1200 - 137F</td>
<td>Ethiopic</td>
</tr>
<tr class="even">
<td>1380 – 139F</td>
<td>Ethiopic Supplement</td>

</tr>
<tr class="odd">
<td>2D80 – 2DDF</td>
<td>Ethiopic Extended</td>

</tr>
<tr class="even">
<td>76</td>
<td>13A0 - 13FF</td>
<td>Cherokee</td>
</tr>
<tr class="odd">
<td>77</td>
<td>1400 - 167F</td>
<td>Unified Canada Aboriginal Syllabics</td>
</tr>
<tr class="even">
<td>78</td>
<td>1680 - 169F</td>
<td>Ogham</td>
</tr>
<tr class="odd">
<td>79</td>
<td>16A0 - 16FF</td>
<td>Runic</td>
</tr>
<tr class="even">
<td rowspan="2">80${REMOVE}$<br />
</td>
<td>1780 - 17FF</td>
<td>Khmer</td>
</tr>
<tr class="odd">
<td>19E0 - 19FF</td>
<td>Symbolsymbole</td>

</tr>
<tr class="even">
<td>81</td>
<td>1800 - 18AF</td>
<td>Mongolisch</td>
</tr>
<tr class="odd">
<td>82</td>
<td>2800 - 28FF</td>
<td>Braung patterns (Braungsmuster)</td>
</tr>
<tr class="even">
<td rowspan="2">83${REMOVE}$<br />
</td>
<td>A000 - A48F</td>
<td>Schreibbare Silbe</td>
</tr>
<tr class="odd">
<td>A490 - A4CF</td>
<td>Während der 1990er-Jahre</td>

</tr>
<tr class="even">
<td rowspan="4">84${REMOVE}$<br />
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
<td>10300 - 1032F</td>
<td>Alte Italic</td>
</tr>
<tr class="odd">
<td>86</td>
<td>10330 - 1034F</td>
<td>Gothic</td>
</tr>
<tr class="even">
<td>87</td>
<td>10400 - 1044F</td>
<td>Deseret</td>
</tr>
<tr class="odd">
<td rowspan="3">88${REMOVE}$<br />
</td>
<td>1D000 - 1D0FF</td>
<td>Symbolsymbole für Denkzeichen</td>
</tr>
<tr class="even">
<td>1D100 - 1D1FF</td>
<td>Symbolsymbole</td>

</tr>
<tr class="odd">
<td>1D200 - 1D24F</td>
<td>Griechisch-Griechisch-Notation</td>

</tr>
<tr class="even">
<td>89</td>
<td>1D400 - 1D7FF</td>
<td>Mathematische alphanumerische Symbole</td>
</tr>
<tr class="odd">
<td rowspan="2">90${REMOVE}$<br />
</td>
<td>FF000 – FFFFD</td>
<td>Private Verwendung (Ebene 15)</td>
</tr>
<tr class="even">
<td>100000 bis 10FFFD</td>
<td>Private Verwendung (Ebene 16)</td>

</tr>
<tr class="odd">
<td rowspan="2">91${REMOVE}$<br />
</td>
<td>FE00 - FE0F</td>
<td>Variationselektoren</td>
</tr>
<tr class="even">
<td>E0100 – E01EF</td>
<td>Ergänzung zu Variantenselektoren</td>

</tr>
<tr class="odd">
<td>92</td>
<td>E0000 – E007F</td>
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
<td>Thai Le</td>
</tr>
<tr class="even">
<td>95</td>
<td>1980 – 19DF</td>
<td>New Thai Lue (Neue Hexen lue)</td>
</tr>
<tr class="odd">
<td>96</td>
<td>1A00 - 1A1F</td>
<td>Buginesisch</td>
</tr>
<tr class="even">
<td>97</td>
<td>2C00 - 2C5F</td>
<td>Glagolitic</td>
</tr>
<tr class="odd">
<td>98</td>
<td>2D30 - 2D7F</td>
<td>Tifinagh</td>
</tr>
<tr class="even">
<td>99</td>
<td>4DC0 - 4DFF</td>
<td>Yijing Hexagrammsymbole</td>
</tr>
<tr class="odd">
<td>100</td>
<td>A800 – A82F</td>
<td>Syloti Nagri</td>
</tr>
<tr class="even">
<td rowspan="3">101${REMOVE}$<br />
</td>
<td>10000 bis 1007F</td>
<td>Lineares B-Syllabary</td>
</tr>
<tr class="odd">
<td>10080 - 100FF</td>
<td>Lineare B-Ideograms</td>

</tr>
<tr class="even">
<td>10100 - 1013F</td>
<td>Nummern der 1990er</td>

</tr>
<tr class="odd">
<td>102</td>
<td>10140 - 1018F</td>
<td>Griechisch(n)</td>
</tr>
<tr class="even">
<td>103</td>
<td>10380 - 1039F</td>
<td>Ugaritisch</td>
</tr>
<tr class="odd">
<td>104</td>
<td>103A0 - 103DF</td>
<td>Old Persian</td>
</tr>
<tr class="even">
<td>105</td>
<td>10450 - 1047F</td>
<td>Shavian</td>
</tr>
<tr class="odd">
<td>106</td>
<td>10480 - 104AF</td>
<td>Osmanya</td>
</tr>
<tr class="even">
<td>107</td>
<td>10800 - 1083F</td>
<td>Silbenlabary</td>
</tr>
<tr class="odd">
<td>108</td>
<td>10A00 bis 10A5F</td>
<td>Igkeitroshthi</td>
</tr>
<tr class="even">
<td>109</td>
<td>1D300 - 1D35F</td>
<td>Symbole für X telecom Jing</td>
</tr>
<tr class="odd">
<td rowspan="2">110${REMOVE}$<br />
</td>
<td>12000 - 123FF</td>
<td>Keilschrift</td>
</tr>
<tr class="even">
<td>12400 bis 1247F</td>
<td>Cuneiform Numbers and Punctuation</td>

</tr>
<tr class="odd">
<td>111</td>
<td>1D360 - 1D37F</td>
<td>Zählen von Zählerzählern</td>
</tr>
<tr class="even">
<td>112</td>
<td>1B80 - 1BBF</td>
<td>Sundanesisch</td>
</tr>
<tr class="odd">
<td>113</td>
<td>1C00 - 1C4F</td>
<td>Lepcha</td>
</tr>
<tr class="even">
<td>114</td>
<td>1C50 - 1C7F</td>
<td>Ol Chiki</td>
</tr>
<tr class="odd">
<td>115</td>
<td>A880 – A8DF</td>
<td>Saurashtra</td>
</tr>
<tr class="even">
<td>116</td>
<td>A900 – A92F</td>
<td>Ia Li</td>
</tr>
<tr class="odd">
<td>117</td>
<td>A930 – A95F</td>
<td>Rejang</td>
</tr>
<tr class="even">
<td>118</td>
<td>AA00 – AA5F</td>
<td>Cham</td>
</tr>
<tr class="odd">
<td>119</td>
<td>10190 – 101CF</td>
<td>Symbolsymbole für Symbole</td>
</tr>
<tr class="even">
<td>120</td>
<td>101D0 - 101FF</td>
<td>Phaphas-Datenträger</td>
</tr>
<tr class="odd">
<td rowspan="3">121${REMOVE}$<br />
</td>
<td>10280 - 1029F</td>
<td>Lykisch</td>
</tr>
<tr class="even">
<td>102A0 - 102DF</td>
<td>Karisch</td>

</tr>
<tr class="odd">
<td>10920 – 1093F</td>
<td>Lydisch</td>

</tr>
<tr class="even">
<td rowspan="2">122${REMOVE}$<br />
</td>
<td>1F000 - 1F02F</td>
<td>Mahjong-Kacheln</td>
</tr>
<tr class="odd">
<td>1F030 - 1F09F</td>
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

<td>Für die prozessinterne Nutzung reserviert</td>
</tr>
</tbody>
</table>



 

 

 



