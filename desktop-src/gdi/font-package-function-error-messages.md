---
description: Fehlermeldungen der Schriftartpaketfunktion
ms.assetid: 3cf7a8a1-66b2-45ca-b53d-29c80f95ff70
title: Fehlermeldungen der Schriftartpaketfunktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7008707675d9b2ef3eb31229535b07b1af6000e43d1122c2929fd12988fb4ea3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118761083"
---
# <a name="font-package-function-error-messages"></a>Fehlermeldungen der Schriftartpaketfunktion

Die folgenden LONG-Werte werden von den Schriftartpaketfunktionen ( [**CreateFontPackage**](/windows/desktop/api/FontSub/nf-fontsub-createfontpackage) und [**MergeFontPackage**](/windows/desktop/api/FontSub/nf-fontsub-mergefontpackage) ) zurückgegeben, wenn Fehler auftreten. Wenn Funktionen erfolgreich sind, wird der Wert NO \_ ERROR zurückgegeben.



| Rückgabewert                   | Wert | BESCHREIBUNG                                                                                                      |
|--------------------------------|-------|------------------------------------------------------------------------------------------------------------------|
| KEIN \_ FEHLER                      | 0     | Kein Fehler ist aufgetreten.                                                                                               |
| \_ERR-FORMAT                    | 1006  | Fehler beim Eingabedatenformat.                                                                             |
| ERR \_ GENERIC                   | 1000  | Fehler im generischen Code.                                                                               |
| ERR \_ MEM                       | 1005  | Während der Speicherbelegung ist ein Fehler aufgetreten.                                                                      |
| ERR \_ NO \_ GLYPHS                | 1009  | Es wurden keine Glyphen gefunden.                                                                                            |
| UNGÜLTIGE \_ \_ ERR-BASIS             | 1085  | Die Schriftart enthielt eine ungültige BASE-Tabelle (Baseline Data). Derzeit wird dieser Wert nicht verwendet.                      |
| UNGÜLTIGE \_ \_ ERR-CMAP             | 1030  | Die Schriftart enthielt eine ungültige CMAP-Tabelle (Character-to-Glyph Mapping).                                           |
| UNGÜLTIGES \_ \_ ERR-DELTAFORMAT \_    | 1013  | Beim Versuch, eine Teilmenge einer Schriftart im Format 1 oder 2 zu verwenden, wurde ein ungültiges Deltaformat erkannt.                                |
| ERR \_ INVALID \_ EBLC             | 1086  | Die Schriftart enthielt eine ungültige EBLC-Tabelle (Embedded Bitmap Location Data).                                        |
| ERR \_ INVALID \_ GLYF             | 1061  | Die Schriftart enthielt eine ungültige Glyf-Datentabelle (glyf).                                                           |
| ERR \_ INVALID \_ GDEF             | 1083  | Die Schriftart enthielt eine ungültige GDEF-Tabelle (GDEF). Derzeit wird dieser Wert nicht verwendet.              |
| ERR \_ INVALID \_ GPOS             | 1082  | Die Schriftart enthielt eine ungültige GPOS-Tabelle (GPOS). Derzeit wird dieser Wert nicht verwendet.             |
| UNGÜLTIGER \_ \_ ERR-GSUB             | 1081  | Die Schriftart enthielt eine ungültige GSUB-Tabelle (GSUB).                                              |
| ERR \_ INVALID \_ HDMX             | 1089  | Die Schriftart enthielt eine ungültige Tabelle mit horizontalen Gerätemetriken (HDMX).                                            |
| ERR \_ INVALID \_ HEAD             | 1062  | Die Schriftart enthielt eine ungültige Kopfzeilentabelle.                                                          |
| ERR \_ INVALID \_ HHEA             | 1063  | Die Schriftart enthielt eine ungültige Tabelle mit horizontaler Kopfzeile (hhea).                                                    |
| ERR \_ INVALID \_ HHEA \_ ODER \_ VHEA   | 1072  | Die Schriftart enthielt eine ungültige Tabelle mit horizontaler Kopfzeile (hhea) oder eine ungültige Tabelle mit vertikalem Metrikheader (vhea). |
| ERR \_ INVALID \_ HMTX             | 1064  | Die Schriftart enthielt eine ungültige Tabelle mit horizontalen Metriken (hmtx).                                                   |
| ERR \_ INVALID \_ HMTX \_ ODER \_ VMTX   | 1073  | Die Schriftart enthielt eine ungültige Tabelle mit horizontalen Metriken (hmtx) oder eine ungültige Tabelle mit vertikalen Metriken (vmtx).       |
| ERR \_ INVALID \_ JSTF             | 1084  | Die Schriftart enthielt eine TABELLE mit ungültigen Begründungsdaten (JSTF).                                                   |
| ERR \_ INVALID \_ LTSH             | 1087  | Die Schriftart enthielt eine ungültige LTSH-Tabelle (Linear Threshold Data).                                                |
| ERR \_ INVALID \_ TTO              | 1080  | Die Schriftart war eine ungültige TrueType Open-Schriftart.                                                                      |
| ERR \_ INVALID \_ VDMX             | 1088  | Die Schriftart enthielt eine ungültige VDMX-Tabelle (Vertical Device Metrics).                                              |
| ERR \_ INVALID \_ LOCA             | 1065  | Die Schriftart enthielt eine ungültige Index-to-Location-Tabelle (loca).                                                    |
| ERR \_ INVALID \_ MAXP             | 1066  | Die Schriftart enthielt eine ungültige Maxp-Tabelle (Maximum Profile).                                                      |
| ERR \_ INVALID \_ MERGE \_ CHECKSUMS | 1011  | Der Versuch, Prüfsummen für zwei Schriftarten aus einer anderen Schriftart zusammenzuführen, war nicht erfolgreich.                       |
| UNGÜLTIGE \_ \_ ERR-MERGEFORMATE \_   | 1010  | Der Versuch, Schriftarten mit den falschen dttf-Formaten zusammenzuführen, war nicht erfolgreich.                                          |
| ERR \_ INVALID \_ MERGE \_ NUMGLYPHS | 1012  | Der Versuch, die Anzahl der Glyphen für zwei Schriftarten aus einer anderen Schriftart zusammenzuführen, war nicht erfolgreich.            |
| UNGÜLTIGER \_ \_ ERR-NAME             | 1067  | Der Name des Schriftartpakets oder ein Schriftartname war ungültig.                                                                |
| ERR \_ INVALID \_ POST             | 1068  | Die Schriftart enthielt eine ungültige PostScript (Post)-Tabelle.                                               |
| ERR \_ INVALID \_ OS2              | 1069  | Die Schriftart enthielt eine ungültige OS/2- Windows Metrikentabelle (OS/2).                                    |
| ERR \_ INVALID \_ VHEA             | 1070  | Die Schriftart enthielt eine ungültige Tabelle mit einem vertikalen Metrikheader (vhea).                                              |
| ERR \_ INVALID \_ VMTX             | 1071  | Die Schriftart enthielt eine ungültige Tabelle mit vertikalen Metriken (vmtx).                                                     |
| UNGÜLTIGER \_ \_ TTC-INDEX \_       | 1015  | Ein ungültiger nullbasierter Index (TTC) in die Schriftartdatei wurde übergeben.                                                 |
| ERR \_ MISSING \_ CMAP             | 1030  | Die Schriftart enthält keine cmap-Tabelle.                                                                           |
| ERR \_ MISSING \_ EBDT             | 1044  | Die Schriftart enthält keine EBDT-Tabelle.                                                                          |
| ERR \_ MISSING \_ GLYF             | 1031  | Die Schriftart enthält keine glyf-Tabelle.                                                                           |
| ERR \_ MISSING \_ HEAD             | 1032  | Die Schriftart enthält keine Kopftabelle.                                                                           |
| ERR \_ MISSING \_ HHEA             | 1033  | Die Schriftart enthält keine Hhea-Tabelle.                                                                          |
| ERR \_ MISSING \_ HMTX             | 1034  | Die Schriftart enthält keine hmtx-Tabelle.                                                                          |
| ERR \_ MISSING \_ LOCA             | 1035  | Die Schriftart enthält keine Loca-Tabelle.                                                                           |
| ERR \_ MISSING \_ MAXP             | 1036  | Die Schriftart enthält keine maxp-Tabelle.                                                                           |
| ERR \_ \_ FEHLENDER NAME             | 1037  | Die Schriftart enthält keine Namenstabelle (Name).                                                                  |
| ERR \_ MISSING \_ POST             | 1038  | Die Schriftart enthält keine Post-Tabelle.                                                                           |
| ERR \_ MISSING \_ OS2              | 1039  | Die Schriftart enthält keine OS/2-Tabelle.                                                                          |
| ERR \_ MISSING \_ VHEA             | 1040  | Die Schriftart enthält keine vhea-Tabelle.                                                                           |
| ERR \_ MISSING \_ VMTX             | 1041  | Die Schriftart enthält keine vmtx-Tabelle.                                                                           |
| ERR \_ MISSING \_ HHEA \_ OR \_ VHEA   | 1042  | Die Schriftart enthält weder eine hhea-Tabelle noch eine vhea-Tabelle.                                                          |
| ERR \_ MISSING \_ HMTX \_ OR \_ VMTX   | 1043  | Die Schriftart enthält weder eine hmtx-Tabelle noch eine vmtx-Tabelle.                                                          |
| ERR \_ NOT \_ TTC                  | 1014  | Der bereitgestellte Wert war kein Index für eine TTC-Datei.                                                              |
| ERR \_ PARAMETER0                | 1100  | Der Aufruf des Funktionsparameters 0 war ungültig.                                                                        |
| ERR \_ PARAMETER1                | 1101  | Der Aufruf des Funktionsparameters 1 war ungültig.                                                                        |
| ERR \_ PARAMETER2                | 1102  | Der Aufruf des Funktionsparameters 2 war ungültig.                                                                        |
| ERR \_ PARAMETER3                | 1103  | Der Aufruf des Funktionsparameters 3 war ungültig.                                                                        |
| ERR \_ PARAMETER4                | 1104  | Der Aufruf des Funktionsparameters 4 war ungültig.                                                                        |
| ERR \_ PARAMETER5                | 1105  | Der Aufruf des Funktionsparameters 5 war ungültig.                                                                        |
| \_ERR-PARAMETER6                | 1106  | Der Aufruf des Funktionsparameters 6 war ungültig.                                                                        |
| ERR \_ PARAMETER7                | 1107  | Der Aufruf des Funktionsparameters 7 war ungültig.                                                                        |
| \_ERR-PARAMETER8                | 1108  | Der Aufruf des Funktionsparameters 8 war ungültig.                                                                        |
| ERR \_ PARAMETER9                | 1109  | Der Aufruf des Funktionsparameters 9 war ungültig.                                                                        |
| ERR \_ PARAMETER10               | 1110  | Der Aufruf des Funktionsparameters 10 war ungültig.                                                                       |
| ERR \_ PARAMETER11               | 1111  | Der Aufruf des Funktionsparameters 11 war ungültig.                                                                       |
| \_ERR-PARAMETER12               | 1112  | Der Aufruf des Funktionsparameters 12 war ungültig.                                                                       |
| ERR \_ PARAMETER13               | 1113  | Der Aufruf des Funktionsparameters 13 war ungültig.                                                                       |
| \_ERR-PARAMETER14               | 1114  | Der Aufruf des Funktionsparameters 14 war ungültig.                                                                       |
| \_ERR-PARAMETER15               | 1115  | Der Aufruf des Funktionsparameters 15 war ungültig.                                                                       |
| \_ERR-PARAMETER16               | 1116  | Der Aufruf des Funktionsparameters 16 war ungültig.                                                                       |
| ERR \_ READCONTROL               | 1003  | Die Struktur des Lesesteuersteuer steuerelements hat nicht mit Daten übereingelesen.                                                                   |
| ERR \_ READOUTOFBOUNDS           | 1001  | Ein Lesen aus dem Arbeitsspeicher war nicht zulässig, möglicherweise, weil Daten nicht über die Grenzen hinaus oder beschädigt waren.                          |
| \_ERR-VERSION                   | 1008  | Der Hauptwert dttf.version der Eingabedaten war größer als die Version, die die Funktion lesen kann.                   |
| ERR \_ WÜRDE \_ ZUNEHMEN               | 1007  | Die angeforderte Aktion hat dazu führte, dass die Daten anwachsen, und die Anwendung muss originale Daten verwenden.                             |
| ERR \_ WRITECONTROL              | 1004  | Die Struktur des Schreibsteuersteuersteuer steuerelements hat nicht mit Daten überein übereinstimmung.                                                                  |
| ERR \_ WRITEOUTOFBOUNDS          | 1002  | Ein Schreibzugriff auf den Arbeitsspeicher war nicht zulässig, möglicherweise, weil Daten nicht über die Grenzen hinaus waren.                                      |



 

 

 



