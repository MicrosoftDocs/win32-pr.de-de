---
description: In diesem Thema werden die Calendar Type-Informationen (caltype-Datentyp) beschrieben, die in den Funktionen enumcalendarinfo, enumcalendarinfoex, enumcalendarinfoexex, getcalendarinfo und getcalendarinfoex verwendet werden.
ms.assetid: 33361a97-0f27-477a-a0ee-3d4d3aaeaacf
title: Kalendertyp Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a8e334a1b05f372f51c81ab8158294d46eebfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867947"
---
# <a name="calendar-type-information"></a>Kalendertyp Informationen

In diesem Thema werden die Calendar Type-Informationen (caltype-Datentyp) beschrieben, die in den Funktionen [**enumcalendarinfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa), [**enumcalendarinfoex**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa), [**enumcalendarinfoexex**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex), [**getcalendarinfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa)und [**getcalendarinfoex**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex) verwendet werden. Einige dieser Werte werden auch von der [**setcalendarinfo**](/windows/desktop/api/Winnls/nf-winnls-setcalendarinfoa) -Funktion verwendet.

Die folgenden caltype-Konstanten können in Kombination mit allen anderen caltype-Konstanten verwendet werden.



| Konstante                     | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cal \_ nouseroverride          | **Windows Me/98, Windows 2000:** Verwenden Sie den Standardwert des Systems anstelle der Auswahl des Benutzers.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Cal- \_ Rückgabe \_ \_ Namen | **Windows 7 und höher:** Rufen Sie das Ergebnis von [**getcalendarinfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) in Form von Namen von Monaten ab, bei denen es sich um die Namen handelt, die verwendet werden, wenn die Monatsnamen mit anderen Elementen kombiniert werden. Beispielsweise wird in Ukrainisch die Entsprechung von Januar in den Namen "" geschrieben, wenn der Monat allein benannt wird. Wenn jedoch der Monats Name in Kombination verwendet wird, z. b. in einem Datum wie dem 5. Januar 2003, wird das Format des Namens verwendet. Im Beispiel "Ukrainisch" wird der Name des "Genitive Month" als "2003 5. Weitere Informationen finden Sie unter [locale \_ Return \_ Genitive \_ Names](locale-return-constants.md). |
| Cal- \_ Rückgabe \_ Nummer          | **Windows Me/98, Windows 2000:** Rufen Sie das Ergebnis von [**getcalendarinfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) als Zahl anstelle einer Zeichenfolge ab. Dies gilt nur für Werte, die mit Cal \_ I beginnen.                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Cal \_ -Verwendung von \_ CP \_ ACP            | **Windows Me/98, Windows 2000:** Verwenden Sie die ANSI-Codepage (ACP) des Systems anstelle der Gebiets Schema-Codepage für die Zeichen folgen Übersetzung. Dies ist nur für ANSI-Versionen von Funktionen relevant, z. b. **enumcalendarinfoa**.                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

Die folgenden caltype-Konstanten schließen sich gegenseitig aus und können in einem Funktions aufrufnicht in Kombination miteinander verwendet werden.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Konstante</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>CAL_ICALINTVALUE</td>
<td>Ein ganzzahliger Wert, der den Kalendertyp des alternativen Kalenders angibt.</td>
</tr>
<tr class="even">
<td>CAL_ITWODIGITYEARMAX</td>
<td><strong>Windows Me/98, Windows 2000:</strong> Ein ganzzahliger Wert, der die obere Grenze des zweistelligen Jahres Bereichs angibt.</td>
</tr>
<tr class="odd">
<td>CAL_IYEAROFFSETRANGE</td>
<td>Mindestens eine NULL-terminierte Zeichenfolge, die die Jahres Offsets für die einzelnen Zeitraum Bereiche angibt. Die letzte Zeichenfolge weist ein zusätzliches abschließendes NULL-Zeichen auf. Dieser Wert variiert je nach Typ des optionalen Kalenders im Format.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVDAYNAME1</td>
<td>Abgekürzte System eigener Name des ersten Tags der Woche.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVDAYNAME2</td>
<td>Abgekürzte System eigener Name des zweiten Tags der Woche.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVDAYNAME3</td>
<td>Abgekürzte System eigener Name des dritten wochentags.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVDAYNAME4</td>
<td>Abgekürzte Name des vierten Tags der Woche.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVDAYNAME5</td>
<td>Abgekürzte System eigener Name des fünften wochentags.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVDAYNAME6</td>
<td>Abgekürzte System eigener Name des sechsten wochentags.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVDAYNAME7</td>
<td>Abgekürzte System eigener Name des siebten wochentags.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVERASTRING</td>
<td><strong>Windows 7 und höher:</strong> Abgekürzte nativer Name eines Zeitraums. Der vollständige Zeitraum wird durch die CAL_SERASTRING Konstante dargestellt.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME1</td>
<td>Der systemeigene Name des ersten Monats des Jahres wurde abgekürzt.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVMONTHNAME2</td>
<td>Abgekürzte System eigener Name des zweiten Monats des Jahres.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME3</td>
<td>Der systemeigene Name des dritten Monats des Jahres wurde abgekürzt.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVMONTHNAME4</td>
<td>Abgekürzte nativer Name des vierten Monats des Jahres.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME5</td>
<td>Abgekürzte nativer Name des fünften Monats des Jahres.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVMONTHNAME6</td>
<td>Der systemeigene Name des sechsten Monats des Jahres wurde abgekürzt.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME7</td>
<td>Der systemeigene Name des siebten Monats des Jahres wurde abgekürzt.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVMONTHNAME8</td>
<td>Abgekürzte nativer Name des achten Monats des Jahres.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME9</td>
<td>Der systemeigene Name des neunten Monats des Jahres wurde abgekürzt.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVMONTHNAME10</td>
<td>Der systemeigene Name des zehnten Monats des Jahres wurde abgekürzt.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME11</td>
<td>Der systemeigene Name des elften Monats des Jahres wurde abgekürzt.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVMONTHNAME12</td>
<td>Der systemeigene Name des zwölften Monats des Jahres wurde abgekürzt.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME13</td>
<td>Der systemeigene Name des dreizehnten Monats des Jahres, sofern vorhanden.</td>
</tr>
<tr class="odd">
<td>CAL_SCALNAME</td>
<td>Der Native Name des alternativen Kalenders.</td>
</tr>
<tr class="even">
<td>CAL_SDAYNAME1</td>
<td>Der Native Name des ersten Tags der Woche.</td>
</tr>
<tr class="odd">
<td>CAL_SDAYNAME2</td>
<td>Der Native Name des zweiten Tags der Woche.</td>
</tr>
<tr class="even">
<td>CAL_SDAYNAME3</td>
<td>Der Native Name des dritten wochentags.</td>
</tr>
<tr class="odd">
<td>CAL_SDAYNAME4</td>
<td>Der Native Name des vierten Tags der Woche.</td>
</tr>
<tr class="even">
<td>CAL_SDAYNAME5</td>
<td>Der Native Name des fünften wochentags.</td>
</tr>
<tr class="odd">
<td>CAL_SDAYNAME6</td>
<td>Der systemeigene Name des sechsten wochentags.</td>
</tr>
<tr class="even">
<td>CAL_SDAYNAME7</td>
<td>Der Native Name des siebten wochentags.</td>
</tr>
<tr class="odd">
<td>CAL_SERASTRING</td>
<td>Mindestens eine NULL-terminierte Zeichenfolge, die jeden der Unicode-Code Punkte angibt, die den mit CAL_IYEAROFFSETRANGE verknüpften Zeitraum angeben. Die letzte Zeichenfolge weist ein zusätzliches abschließendes NULL-Zeichen auf. Dieser Wert variiert je nach Typ des optionalen Kalenders im Format.</td>
</tr>
<tr class="even">
<td>CAL_SLONGDATE</td>
<td>Lange Datumsformate für den Kalendertyp.</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHDAY</td>
<td><strong>Windows 7 und höher:</strong> Format von Monat und Tag für den Kalendertyp. Die Formatierung ähnelt der für CAL_SLONGDATE. Wenn z. b. das Muster Month/Day der vollständige Monats Name ist, gefolgt von der Tagesnummer mit führenden Nullen (z &quot; . b. September 03), &quot; ist das Format &quot; MMMM dd &quot; . Einfache Anführungszeichen können verwendet werden, um nicht formatierte Zeichen (z. b. "de") in Spanisch einzufügen.
<blockquote>
[!Note]<br />
Dieser Kalendertyp unterstützt nur ein Format.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME1</td>
<td>Der Native Name des ersten Monats des Jahres.</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHNAME2</td>
<td>Der Native Name des zweiten Monats des Jahres.</td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME3</td>
<td>Der Native Name des dritten Monats des Jahres.</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHNAME4</td>
<td>Der Native Name des vierten Monats des Jahres.</td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME5</td>
<td>Der Native Name des fünften Monats des Jahres.</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHNAME6</td>
<td>Der Native Name des sechsten Monats des Jahres.</td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME7</td>
<td>Der Native Name des siebten Monats des Jahres.</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHNAME8</td>
<td>Der Native Name des achten Monats des Jahres.</td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME9</td>
<td>Der Native Name des neunten Monats des Jahres.</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHNAME10</td>
<td>Der Native Name des zehnten Monats des Jahres.</td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME11</td>
<td>Der Native Name des elften Monats des Jahres.</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHNAME12</td>
<td>Der Native Name des zwölften Monats des Jahres.</td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME13</td>
<td>Der Native Name des dreizehnten Monats des Jahres, falls vorhanden.</td>
</tr>
<tr class="odd">
<td>CAL_SSHORTDATE</td>
<td>Kurze Datumsformate für den Kalendertyp.</td>
</tr>
<tr class="even">
<td>CAL_SSHORTESTDAYNAME1</td>
<td><strong>Windows Vista und höher:</strong> Kurzer nativer Name des ersten Tags der Woche.</td>
</tr>
<tr class="odd">
<td>CAL_SSHORTESTDAYNAME2</td>
<td><strong>Windows Vista und höher:</strong> Kurzer nativer Name des zweiten Tags der Woche.</td>
</tr>
<tr class="even">
<td>CAL_SSHORTESTDAYNAME3</td>
<td><strong>Windows Vista und höher:</strong> Kurzer nativer Name des dritten wochentags.</td>
</tr>
<tr class="odd">
<td>CAL_SSHORTESTDAYNAME4</td>
<td><strong>Windows Vista und höher:</strong> Kurzer nativer Name des vierten Tags der Woche.</td>
</tr>
<tr class="even">
<td>CAL_SSHORTESTDAYNAME5</td>
<td><strong>Windows Vista und höher:</strong> Kurzer nativer Name des fünften wochentags.</td>
</tr>
<tr class="odd">
<td>CAL_SSHORTESTDAYNAME6</td>
<td><strong>Windows Vista und höher:</strong> Kurzer nativer Name des sechsten wochentags.</td>
</tr>
<tr class="even">
<td>CAL_SSHORTESTDAYNAME7</td>
<td><strong>Windows Vista und höher:</strong> Kurzer nativer Name des siebten wochentags.</td>
</tr>
<tr class="odd">
<td>CAL_SYEARMONTH</td>
<td><strong>Windows Me/98, Windows 2000:</strong> Das Jahr/Monat-Format für die angegebenen Kalender.</td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Wenn der Native Name des Wochentags oder eines Monats eine leere Zeichenfolge ist, ist dieser Name mit dem in den entsprechenden Gebiets Schema Informationen angegebenen Namen identisch und wird daher hier nicht dupliziert.

 

 

 




