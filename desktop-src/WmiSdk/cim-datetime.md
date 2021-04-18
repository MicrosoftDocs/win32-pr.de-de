---
description: Sie können auf alle Common Information Model (CIM)-Datums-und Uhrzeitwerte in WMI zugreifen, indem Sie eines der zwei für WMI und CIM spezifischen Formate mit fester Länge verwenden. Verwenden Sie bei der Skripterstellung das Objekt "Swap DateTime", um diese in reguläre Datumsangaben und Uhrzeiten zu konvertieren.
ms.assetid: 15126802-82f9-4ab4-98d8-0a15184302e9
ms.tgt_platform: multiple
title: CIM_DATETIME
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fee4356050ee340cbf9d1b066f012d32c7185dd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352506"
---
# <a name="cim_datetime"></a>CIM- \_ DateTime

Sie können auf alle [*Common Information Model (CIM)*](gloss-c.md) -Datums-und Uhrzeitwerte in WMI zugreifen, indem Sie eines der zwei für WMI und CIM spezifischen Formate mit fester Länge verwenden. Verwenden Sie bei der Skripterstellung das Objekt " [**Swap DateTime**](swbemdatetime.md) ", um diese in reguläre Datumsangaben und Uhrzeiten zu konvertieren.

In den folgenden Abschnitten wird beschrieben, wie die Datums-und Uhrzeit Formate von WMI verwendet werden.

## <a name="format"></a>Format

In der folgenden Tabelle werden die beiden Datums-und Uhrzeit Formate aufgelistet, die von WMI verwendet werden.



| Format                                                                                                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DateTime](datetime.md)<br/> *YYYYMMDDHHMMSS. mmmmmmsUUU*<br/>                             | Das Format, in dem CIM- [**DateTime**](datetime.md) -Werte gespeichert werden. Dieses Format ist Gebiets Schema unabhängig, sodass Sie ein Skript schreiben können, das auf einem beliebigen Computer ausgeführt wird. Sie müssen dieses Format verwenden, um ein Datum und eine Uhrzeit in [*Managed Object Format (MOF)*](gloss-m.md)oder beim Schreiben in eine Instanz mithilfe der [com-API für WMI](com-api-for-wmi.md) oder der [Skript-API für WMI](scripting-api-for-wmi.md)zu definieren. Weitere Informationen finden Sie unter [Ändern einer Instanzeigenschaft](modifying-an-instance-property.md). |
| Das Format ist nur in WMI Query Language (WQL)-Abfragen gültig.<br/> *yyyy-mm-dd hh: mm: SS: mmm*<br/> | Dieses Format kann in Skripts verwendet werden, die die Methode " [**Swap DateTime**](swbemdatetime.md) " verwenden. Weitere Informationen finden Sie unter [Abfragen von WMI](querying-wmi.md) oder [Abfragen mit WQL](querying-with-wql.md). Dieses Format ist nicht unabhängig vom Gebiets Schema. Die Reihenfolge von Jahr, Monat und Tag hängt von der Regional-und sprach Formateinstellung der Benutzersitzung ab. Wenn z. b. die Standardeinstellung für USA English "mm-dd-yyyy HH: mm: SS: MMM" lautet, ist das Format für die meisten anderen Länder oder Regionen "yyyy-mm-dd hh: mm: SS: MMM".       |



 

In der folgenden Tabelle werden die Felder in den Formaten aufgelistet.



| Feld    | BESCHREIBUNG                                                                                                                                                                                                                                     |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *yyyy*   | Vierstellige Jahres Angabe (0000 bis 9999). Die Implementierung kann den unterstützten Bereich einschränken. Eine-Implementierung kann z. b. nur die Jahre 1980 bis 2099 unterstützen.                                                                         |
| *mm*     | Zweistellige Monats Angabe (01 bis 12).                                                                                                                                                                                                                |
| *dd*     | Zweistellige Tages Angabe des Monats (01 bis 31). Dieser Wert muss für den Monat geeignet sein. Beispielsweise ist der 31. Februar ungültig. Ihre Implementierung muss jedoch keine Überprüfung auf gültige Daten durchsuchen.                                            |
| *HH*     | Zweistellige Stunden Angabe im 24-Stunden-Format (00 bis 23).                                                                                                                                                                              |
| *MM*     | Zweistellige Minuten Angabe in der Stunde (00 bis 59).                                                                                                                                                                                                   |
| *SS*     | Zweistellige Anzahl von Sekunden in der Minute (00 bis 59).                                                                                                                                                                                      |
| *mmmmmm* | Sechsstellige Anzahl von Mikrosekunden im zweiten Wert (000000 bis 999999). Die-Implementierung muss die Auswertung mit diesem Feld nicht unterstützen. Dieses Feld muss jedoch immer vorhanden sein, um die Art der Zeichenfolge mit fester Länge beizubehalten. |
| *mmm*    | Dreistellige Anzahl von Millisekunden in der Minute (000 bis 999).                                                                                                                                                                             |
| *s*      | Plus Zeichen (+) oder Minuszeichen (-), um einen positiven oder negativen Offset von der koordinierten Weltzeit (UTC) anzugeben.                                                                                                                               |
| *Uuu*    | Ein dreistelliger Offset, der die Anzahl der Minuten angibt, die die ursprüngliche Zeitzone von UTC abweicht. Für WMI wird es empfohlen, aber nicht erforderlich, Zeiten in GMT zu konvertieren (ein UTC-Offset von null).                                              |



 

Sie müssen alle Felder mit der angezeigten Länge eingeben, wobei die für den Typ erforderlichen führenden Nullen verwendet werden. Verwenden Sie jedoch Sternchen, um nicht verwendete Felder oder einen Platzhalter Wert anzugeben. Sie können ein Sternchen ( \* ) überall außer der **Where** -Klausel einer Abfrage verwenden. Beispielsweise können ein Datum und eine Uhrzeit mit einem nicht angegebenen Jahr in einem beliebigen Jahr auftreten. Wenn Sie ein Feld nicht angeben möchten, müssen Sie das gesamte Feld durch Sternchen ersetzen.

In den folgenden Beispielen werden gültige und ungültige Verwendungen von Sternchen beschrieben:

-   19980416 \* \* \* \* \* \* .000000 + \* \* \* (legal)
-   1998-04-16 \* \* \* \* \* \* : \* \* \* (unzulässig)
-   199 \* 0416 \* \* \* \* \* \* .000000 + \* \* \* (unzulässig)
-   199 \* -04-16 \* \* \* \* \* \* : \* \* \* (unzulässig)

Wenn ein DateTime-Wert verwendet wird, um einen bestimmten Zeitpunkt darzustellen, sollten alle Felder Daten enthalten. Wenn Sie zur Darstellung eines Zeit Bereichs verwendet wird, sollten nur die Felder, die zum übermitteln der Dauer erforderlich sind, Daten einschließen.

Im folgenden Beispiel wird "April First" beschrieben: ein Datum in Bezug auf ein nicht angegebenes Jahr, aber immer noch ein definierter Punkt, wenn die Maßeinheit ein Tag ist.

-   \*\*\*\*0401 \* \* \* \* \* \* . 000000 +\*\*\*
-   \*\*\*\*-04-01 \* \* \* \* \* \* : \* \* \* (unzulässig)

## <a name="setting-utc-offset-and-gmt"></a>Festlegen von UTC-Offset und GMT

In den folgenden Beispielen wird beschrieben, wie Sie eine Zeit ohne Zeitzone definieren können, indem Sie Sternchen im uuu-Feld nach dem Plus-oder Minuszeichen platzieren:

-   19980401135809.000000 +\*\*\*
-   19980401135809,000000-\*\*\*
-   1998-04-01 13:58:09: \* \* \* (unzulässig)

Eine Anwendung interpretiert einen Datums-und uhrzeitverweis ohne Zonen auf einen lokalen, abstrakten Chronometer innerhalb des ausgeführten Betriebssystems. Tragbare Computer können z. b. über interne Uhren verfügen, deren Einstellungen der geografischen Zeitzone entsprechen. Sie können eine unzonenzeit interpretieren, indem Sie die Zeitzone der aktuellen abstrakten Zeit Quelle anstelle der lokalen Zeitzone ersetzen.

Sie sollten die Bedeutung des UTC-Offsets mit Datums-und Uhrzeitangaben in Abfragen besonders berücksichtigen. Im Allgemeinen funktionieren Äquivalenz, größer als oder kleiner als Vergleiche zwischen zwei Datums-und Uhrzeitangaben, wenn die Datums-und Uhrzeitangaben denselben UTC-Offset verwenden. Beim Umgang mit Datums-und Uhrzeitangaben mit unterschiedlichen Zeit Zonen Offsets sollten Sie zunächst die Datums-und Uhrzeitangaben in GMT konvertieren.

Abfragen, die relative Datumsangaben und Uhrzeiten mit Sternchen in einem oder mehreren unter Feldern einbeziehen, sind im Vergleich zu Äquivalenz nur für WMI sinnvoll. Außerdem lässt WMI keine Verwendung von Sternchen als Platzhalter zu. Stattdessen vergleicht WMI relative Datums-und Uhrzeitangaben auf Zeichenbasis.

In den folgenden Beispielen werden zwei Datumsangaben beschrieben, die eine WMI-Abfrage nicht als identisch betrachtet:

-   19980401135809.000000 +\*\*\*
-   19980401135809.000000 + 000

## <a name="converting-to-filetime-or-vt_date-format"></a>Wechseln in das FILETIME-oder VT \_ Date-Format

Das CIM- [**DateTime**](datetime.md) -Format wird nur innerhalb von WMI verwendet. Sie können in das und aus dem WMI-Format und entweder in das FILETIME-oder VT Date-Format konvertieren, \_ indem Sie die-Methoden des Skript Objekts " [**slibemdatetime**](swbemdatetime.md) " aufrufen. Eine [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) - **DateTime** -Struktur ist ein 64-Bit-Wert, der von den 32-Bit-Windows-Betriebssystemen verwendet wird. Das VT \_ Date-Format ist ein DateTime-Wert der Automatisierungs Variante, der von Visual Basic und ActiveX verwendet wird. In der folgenden Tabelle sind die Konvertierungs Methoden aufgeführt.



| Methode                                                         | BESCHREIBUNG                                                                                           |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**' Swap DateTime. GetFileTime '**](swbemdatetime-getfiletime.md) | Ruft einen [**DateTime**](datetime.md) -Wert im [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) -Format ab.                |
| [**"Slibemdatetime. getVarDate"**](swbemdatetime-getvardate.md)   | Ruft einen [**DateTime**](datetime.md) -Wert im VT- \_ Datumsformat ab.                                         |
| [**' Swap DateTime. SetFileTime '**](swbemdatetime-setvardate.md)  | Legt eine [**DateTime**](datetime.md) -Eigenschaft mithilfe eines [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) -Datums als Eingabe fest. |
| [**Slibemdatetime. SetVarDate**](swbemdatetime-setvardate.md)   | Legt eine [**DateTime**](datetime.md) -Eigenschaft mithilfe eines VT- \_ Datums Datums als Eingabe fest.                          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datums-und Uhrzeit Format](date-and-time-format.md)
</dt> <dt>

[Informationen zu WMI](about-wmi.md)
</dt> <dt>

[WMI-Tasks: Datumsangaben und Uhrzeiten](wmi-tasks--dates-and-times.md)
</dt> <dt>

[Intervall Format](interval-format.md)
</dt> <dt>

[**Swap-Datei\_**](swbemobject-put-.md)
</dt> <dt>

[**Swap Service Type. Put**](swbemservicesex-put.md)
</dt> <dt>

[**Swap-DateTime**](swbemdatetime.md)
</dt> <dt>

[**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)
</dt> <dt>

[**IWbemServices::P utclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass)
</dt> </dl>

 

