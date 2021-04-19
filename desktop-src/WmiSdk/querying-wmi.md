---
description: Eines der wichtigsten Tools von Windows-Verwaltungsinstrumentation (WMI) ist die Möglichkeit, das WMI-Repository nach Klassen-und Instanzinformationen abzufragen.
ms.assetid: 0cceda42-fba0-4a08-90dd-43f022d0be41
ms.tgt_platform: multiple
title: WMI-Abfrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdae44d4c40e1127bfc4d3436d6230eafd52146a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354607"
---
# <a name="querying-wmi"></a>WMI-Abfrage

Eines der wichtigsten Tools von Windows-Verwaltungsinstrumentation (WMI) ist die Möglichkeit, das WMI-Repository nach Klassen-und Instanzinformationen abzufragen. Beispielsweise können Sie anfordern, dass WMI alle Objekte zurückgibt, die das Herunterfahren von Ereignissen des Desktop Systems darstellen. Sie können auch Klassen-, Instanz-oder Schema Daten abrufen. In der folgenden Tabelle sind die verschiedenen Typen von Abfragen aufgelistet, die Sie vornehmen können.



| Thema                                                                | BESCHREIBUNG                                                                                                                                                                                      |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Aufrufen einer synchronen Abfrage](invoking-a-synchronous-query.md)     | Hier wird beschrieben, wie im gesamten Abfrageprozess eine Verknüpfung mit WMI beibehalten wird. Synchrone Abfragen eignen sich gut für kleine Abfragen oder Abfragen an ein lokales System.<br/>                                  |
| [Aufrufen einer asynchronen Abfrage](invoking-an-asynchronous-query.md) | Beschreibt das Einrichten eines separaten Prozesses zum Empfangen von Abfragen. Asynchrone Abfragen sind komplexer und bieten ein niedrigeres Maß an Sicherheit, verbessern jedoch im Allgemeinen die Systemleistung.<br/> |



 

Zusätzlich zum Abfragen des WMI-Repository können Sie auch den [*WMI Query Language (WQL)*](gloss-w.md) verwenden, um Benachrichtigungs Ereignisse an die Anwendung weiterzuleiten. Weitere Informationen finden Sie unter [empfangen eines WMI-Ereignisses](receiving-a-wmi-event.md).

> [!Note]
>
> Zum ordnungsgemäßen Abfragen von WMI müssen Sie über ein gutes Verständnis der WQL verfügen. Eine Abfrage, die falsch, zu komplex oder ungeeignet ist, kann dazu führen, dass der Abfrage Prozessor einen Fehler oder unerwartete Ergebnisse zurückgibt. Eine umfassende Anleitung zu WQL finden Sie unter [Querying with WQL (Abfragen mit WQL](querying-with-wql.md)).
>
> Es gibt Einschränkungen für die Anzahl von **-** und- **oder** -Schlüsselwörtern, die in WQL-Abfragen verwendet werden können. Eine große Anzahl von WQL-Schlüsselwörtern, die in einer komplexen Abfrage verwendet werden, kann bewirken, dass WMI den Fehlercode der **WBEM \_ E- \_ Kontingent \_ Verletzung** als **HRESULT** -Wert zurückgibt Das Limit von WQL-Schlüsselwörtern hängt von der Komplexität der Abfrage ab.
>
> Beim Abfragen von Eigenschafts Werten mit einem **UInt64** -oder **sint64** -Datentyp in einer Skriptsprache wie VBScript gibt WMI Zeichen folgen Werte zurück. Beim Vergleichen dieser Werte können unerwartete Ergebnisse auftreten, da das Vergleichen von Zeichen folgen andere Ergebnisse als das Vergleichen von Zahlen zurückgibt. Beispielsweise ist "10 Milliarden" kleiner als "9" beim Vergleichen von Zeichen folgen, und 9 ist kleiner als 10 Milliarden beim Vergleich von Zahlen. Um Verwirrung zu vermeiden, sollten Sie die [CDbl](/previous-versions//ftekwwt0(v=vs.85)) -Methode in VBScript verwenden, wenn Eigenschaften vom Typ **UInt64** oder **sint64** aus WMI abgerufen werden.

 

> [!Note]  

 

Weitere Informationen finden Sie unter Bearbeiten von [Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md).

 

