---
description: Fehlermeldungen der Schriftart Paket Funktion
ms.assetid: 3cf7a8a1-66b2-45ca-b53d-29c80f95ff70
title: Fehlermeldungen der Schriftart Paket Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06bcf84f92b60351e8375df682de0c3b01c2aa1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130769"
---
# <a name="font-package-function-error-messages"></a>Fehlermeldungen der Schriftart Paket Funktion

Die folgenden Long-Werte werden von den Schriftart Paketfunktionen (" [**kreatefontpackage**](/windows/desktop/api/FontSub/nf-fontsub-createfontpackage) " und " [**mergefontpackage**](/windows/desktop/api/FontSub/nf-fontsub-mergefontpackage) ") zurückgegeben, wenn Fehler auftreten. Wenn Funktionen erfolgreich sind, wird der Wert "kein \_ Fehler" zurückgegeben.



| Rückgabewert                   | Wert | BESCHREIBUNG                                                                                                      |
|--------------------------------|-------|------------------------------------------------------------------------------------------------------------------|
| kein \_ Fehler                      | 0     | Kein Fehler ist aufgetreten.                                                                                               |
| Err- \_ Format                    | 1006  | Ein Eingabedaten-Format Fehler ist aufgetreten.                                                                             |
| Err- \_ generisch                   | 1000  | Im generischen Code ist ein Fehler aufgetreten.                                                                               |
| Err-Arbeitsspeicher \_                       | 1005  | Fehler bei der Speicher Belegung.                                                                      |
| Err \_ keine \_ Symbole                | 1009  | Es wurden keine Symbole gefunden.                                                                                            |
| \_ungültige \_ Basis             | 1085  | Die Schriftart enthielt eine ungültige Baseline-Datentabelle (Basistabelle). Dieser Wert wird derzeit nicht verwendet.                      |
| \_ungültige \_ cmap             | 1030  | Die Schriftart enthielt eine ungültige Zeichen-zu-Glyphen-Zuordnungs Tabelle (cmap).                                           |
| Err \_ - \_ Delta Format ist ungültig. \_    | 1013  | Beim Versuch, eine Schriftart im Format 1 oder 2 zu unterteilen, wurde ein ungültiges Delta Format festgestellt.                                |
| Err \_ ungültige \_ EBLC             | 1086  | Die Schriftart enthielt eine ungültige EBLC-Tabelle (Bitmap Location Data).                                        |
| \_ungültige \_ glyf.             | 1061  | Die Schriftart enthielt eine ungültige glyf-Tabelle (Symbol).                                                           |
| Err- \_ ungültiger \_ GDEF             | 1083  | Die Schriftart enthielt eine ungültige GDEF-Tabelle (Symbol-Definitions Daten). Dieser Wert wird derzeit nicht verwendet.              |
| Ungültige Gruppenrichtlinien Objekte \_ \_             | 1082  | Die Schriftart enthielt eine ungültige Tabelle mit Glyphe-Positionierungsdaten (GPOs). Dieser Wert wird derzeit nicht verwendet.             |
| Err- \_ ungültige \_ GSUB             | 1081  | Die Schriftart enthielt eine ungültige GSUB (Symbol Substitution Data)-Tabelle.                                              |
| Err- \_ ungültige \_ hdmx.             | 1089  | Die Schriftart enthielt eine ungültige hdmx-Tabelle (horizontale gerätemetriken).                                            |
| \_ungültige \_ Kopfzeile             | 1062  | Die Schriftart enthielt eine ungültige Schriftart Header Tabelle (Head).                                                          |
| Err- \_ ungültige \_ hhea             | 1063  | Die Schriftart enthielt eine ungültige Tabelle mit horizontaler Kopfzeile (hhea).                                                    |
| Err \_ ungültige \_ hhea \_ oder \_ vhea   | 1072  | Die Schriftart enthielt eine ungültige hhea-Tabelle (horizontal Header) oder eine ungültige vhea-Tabelle (Vertical Metrics Header). |
| Err \_ ungültiges \_ HMTX             | 1064  | Die Schriftart enthielt eine ungültige Tabelle mit horizontaler Metriken (HMTX).                                                   |
| Err \_ ungültige \_ HMTX- \_ oder \_ VMTX-Datei   | 1073  | Die Schriftart enthielt eine ungültige Tabelle mit horizontaler Metriken (HMTX) oder eine ungültige Tabelle mit vertikalen Metriken (VMTX).       |
| \_ungültige \_ jstf-Datei             | 1084  | Die Schriftart enthielt eine ungültige jstf-Tabelle (Begründung).                                                   |
| Err- \_ ungültige \_ LTSH             | 1087  | Die Schriftart enthielt eine ungültige LTSH-Tabelle (linear Threshold Data).                                                |
| Err \_ ungültiges \_ tto              | 1080  | Die Schriftart war eine ungültige TrueType-öffnende Schriftart.                                                                      |
| Err- \_ ungültige \_ VDMX             | 1088  | Die Schriftart enthielt eine ungültige VDMX-Tabelle (Vertical Device Metrics).                                              |
| \_ungültige \_ Loca             | 1065  | Die Schriftart enthielt eine ungültige Index-to-Location-Tabelle (Loca).                                                    |
| \_ungültiges \_ MaxP.             | 1066  | Die Schriftart enthielt eine ungültige Tabelle "Maximum profile" (MaxP).                                                      |
| \_ungültige \_ Merge- \_ Prüfsummen | 1011  | Der Versuch, Prüfsummen für zwei Schriftarten aus einer anderen Mutter Schriftart zusammenzuführen, ist nicht erfolgreich.                       |
| Err- \_ ungültige \_ Zusammenschluss \_ Formate   | 1010  | Der Versuch, Schriftarten mit den falschen dttf-Formaten zusammenzuführen, war nicht erfolgreich.                                          |
| Err \_ ungültige \_ Merge- \_ numglyphen. | 1012  | Ein Versuch, die Anzahl der Symbole für zwei Schriftarten aus einer anderen Mutter Schriftart zusammenzuführen, war nicht erfolgreich.            |
| \_ungültiger \_ Name             | 1067  | Der Name des Schriftart Pakets oder der Schriftart ist ungültig.                                                                |
| \_ungültiger \_ Beitrag             | 1068  | Die Schriftart enthielt eine ungültige Tabelle mit PostScript-Informationen (Post).                                               |
| Err- \_ ungültige \_ OS2              | 1069  | Die Schriftart enthielt eine ungültige Tabelle mit Betriebssystem/2 und Windows-spezifischer Metriken (OS/2).                                    |
| Err- \_ ungültige \_ vhea             | 1070  | Die Schriftart enthielt eine ungültige vhea-Tabelle (Vertical Metrics Header).                                              |
| Err- \_ ungültige \_ VMTX             | 1071  | Die Schriftart enthielt eine ungültige Tabelle mit vertikalen Metriken (VMTX).                                                     |
| Err- \_ ungültiger \_ TTC- \_ Index       | 1015  | Es wurde ein ungültiger NULL basierter (TTC) Index in die Schriftart Datei übermittelt.                                                 |
| \_fehlende \_ cmap für Err             | 1030  | Die Schriftart enthielt keine cmap-Tabelle.                                                                           |
| Err \_ Missing \_ ebdt             | 1044  | Die Schriftart enthielt keine ebdt-Tabelle.                                                                          |
| Err \_ - \_ glyf fehlt             | 1031  | Die Schriftart enthielt keine glyf-Tabelle.                                                                           |
| Err \_ Missing \_ Head             | 1032  | Die Schriftart enthielt keine Haupttabelle.                                                                           |
| Err \_ - \_ hhea fehlt             | 1033  | Die Schriftart enthielt keine hhea-Tabelle.                                                                          |
| Err \_ fehlt \_ HMTX             | 1034  | Die Schriftart enthielt keine HMTX-Tabelle.                                                                          |
| Err \_ Missing \_ Loca             | 1035  | Die Schriftart enthielt keine Loca-Tabelle.                                                                           |
| Err \_ fehlt \_ MaxP             | 1036  | Die Schriftart enthielt keine MaxP-Tabelle.                                                                           |
| fehlender Err- \_ \_ Name             | 1037  | Die Schriftart enthielt keine Benennungs Tabelle (Name).                                                                  |
| Err \_ - \_ Post fehlt.             | 1038  | Die Schriftart enthielt keine Post-Tabelle.                                                                           |
| Err \_ Missing \_ OS2              | 1039  | Die Schriftart enthielt keine OS/2-Tabelle.                                                                          |
| Err \_ - \_ vhea fehlt             | 1040  | Die Schriftart enthielt keine vhea-Tabelle.                                                                           |
| Err \_ fehlt \_ VMTX             | 1041  | Die Schriftart enthielt keine VMTX-Tabelle.                                                                           |
| Err \_ fehlt \_ hhea \_ oder \_ vhea   | 1042  | Die Schriftart enthielt keine hhea-Tabelle oder vhea-Tabelle.                                                          |
| Err \_ fehlt \_ HMTX \_ oder \_ VMTX   | 1043  | Die Schriftart enthielt keine HMTX-Tabelle oder VMTX-Tabelle.                                                          |
| Err \_ Not \_ TTC                  | 1014  | Der angegebene Wert war kein Index für eine TTC-Datei.                                                              |
| Err- \_ PARAMETER0                | 1100  | Der Aufruf des Funktions Parameters 0 war ungültig.                                                                        |
| Err- \_ PARAMETER1                | 1101  | Der Aufruf von Funktionsparameter 1 war ungültig.                                                                        |
| Err- \_ PARAMETER2                | 1102  | Der Aufruf von Funktionsparameter 2 war ungültig.                                                                        |
| Err- \_ PARAMETER3                | 1103  | Der Aufruf von Funktionsparameter 3 war ungültig.                                                                        |
| Err- \_ PARAMETER4                | 1104  | Der Aufruf von Funktionsparameter 4 war ungültig.                                                                        |
| Err- \_ PARAMETER5                | 1105  | Der Aufruf des Funktions Parameters 5 war ungültig.                                                                        |
| Err- \_ PARAMETER6                | 1106  | Der Aufruf von Funktionsparameter 6 war ungültig.                                                                        |
| Err- \_ PARAMETER7                | 1107  | Der Aufruf von Funktionsparameter 7 war ungültig.                                                                        |
| Err- \_ PARAMETER8                | 1108  | Der Aufruf von Funktionsparameter 8 war ungültig.                                                                        |
| Err- \_ PARAMETER9                | 1109  | Der Aufruf von Funktionsparameter 9 war ungültig.                                                                        |
| Err- \_ PARAMETER10               | 1110  | Der Aufruf von Funktionsparameter 10 war ungültig.                                                                       |
| Err- \_ PARAMETER11               | 1111  | Der Aufruf von Funktionsparameter 11 war ungültig.                                                                       |
| Err- \_ PARAMETER12               | 1112  | Der Aufruf von Funktionsparameter 12 war ungültig.                                                                       |
| Err- \_ PARAMETER13               | 1113  | Der Aufruf des Funktions Parameters 13 war ungültig.                                                                       |
| Err- \_ PARAMETER14               | 1114  | Der Aufruf von Funktionsparameter 14 war ungültig.                                                                       |
| Err- \_ PARAMETER15               | 1115  | Der Aufruf von Funktionsparameter 15 war ungültig.                                                                       |
| Err- \_ PARAMETER16               | 1116  | Der Aufruf von Funktionsparameter 16 war ungültig.                                                                       |
| Err- \_ Steuerelement               | 1003  | Die Lese Steuerelement Struktur entsprach nicht den Daten.                                                                   |
| Err-Ausgabe \_ Grenzen           | 1001  | Ein Lesevorgang aus dem Arbeitsspeicher war nicht zulässig, möglicherweise weil Daten außerhalb des gültigen Bereichs liegen oder beschädigt waren.                          |
| Err- \_ Version                   | 1008  | Der wichtige dttf. Version-Wert der Eingabedaten war größer als die Version, die von der Funktion gelesen werden kann.                   |
| Err \_ \_ wächst               | 1007  | Die angeforderte Aktion hat bewirkt, dass Daten vergrößert werden, und die Anwendung muss die ursprünglichen Daten verwenden.                             |
| Err- \_ Schreib Steuerung              | 1004  | Die Schreib Steuerungsstruktur entsprach nicht den Daten.                                                                  |
| Err- \_ Schreibvorgänge          | 1002  | Ein Schreibzugriff auf den Arbeitsspeicher war nicht zulässig, möglicherweise weil Daten außerhalb des gültigen Bereichs liegen.                                      |



 

 

 



