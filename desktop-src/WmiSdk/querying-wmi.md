---
description: Eines der wichtigsten Tools der Windows Management Instrumentation (WMI) ist die Möglichkeit, das WMI-Repository nach Klassen- und Instanzinformationen abfragt.
ms.assetid: 0cceda42-fba0-4a08-90dd-43f022d0be41
ms.tgt_platform: multiple
title: Abfragen von WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfc9cd51946bad1df482bb286c538e38bba8e2b3337776e3cd62e0a0da652574
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118817538"
---
# <a name="querying-wmi"></a>Abfragen von WMI

Eines der wichtigsten Tools der Windows Management Instrumentation (WMI) ist die Möglichkeit, das WMI-Repository nach Klassen- und Instanzinformationen abfragt. Beispielsweise können Sie anfordern, dass WMI alle Objekte zurücksinget, die Herunterfahrensereignisse von Ihrem Desktopsystem darstellen. Sie können auch Klassen-, Instanz- oder Schemadaten abrufen. In der folgenden Tabelle sind die verschiedenen Arten von Abfragen aufgeführt, die Sie ausführen können.



| Thema                                                                | Beschreibung                                                                                                                                                                                      |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Aufrufen einer synchronen Abfrage](invoking-a-synchronous-query.md)     | Beschreibt, wie ein Link mit WMI während des gesamten Abfrageprozesses verwaltet wird. Synchrone Abfragen sind für kleine Abfragen oder Abfragen an ein lokales System gut.<br/>                                  |
| [Aufrufen einer asynchronen Abfrage](invoking-an-asynchronous-query.md) | Beschreibt, wie ein separater Prozess zum Empfangen von Abfragen eingerichtet wird. Asynchrone Abfragen sind komplexer und bieten ein geringeres Maß an Sicherheit, verbessern aber im Allgemeinen die Systemleistung.<br/> |



 

Zusätzlich zum Abfragen des WMI-Repositorys können Sie auch den WMI Query Language [*(WQL)*](gloss-w.md) verwenden, um Benachrichtigungsereignisse an Ihre Anwendung weiter zu routen. Weitere Informationen finden Sie unter [Empfangen eines WMI-Ereignisses.](receiving-a-wmi-event.md)

> [!Note]
>
> Um WMI ordnungsgemäß abfragen zu können, müssen Sie WQL gut verstehen. Eine falsche, zu komplexe oder ungeeignete Abfrage kann dazu führen, dass der Abfrageprozessor einen Fehler oder unerwartete Ergebnisse zurücksendet. Eine umfassende Anleitung zu WQL finden Sie unter [Abfragen mit WQL.](querying-with-wql.md)
>
> Die Anzahl der SCHLÜSSELWÖRTER **AND** und **OR,** die in WQL-Abfragen verwendet werden können, ist begrenzt. Eine große Anzahl von WQL-Schlüsselwörtern, die in einer komplexen Abfrage verwendet werden, kann dazu führen, dass WMI den **WBEM \_ E \_ QUOTA \_ VIOLATION-Fehlercode** als **HRESULT-Wert** zurückgibt. Der Grenzwert für WQL-Schlüsselwörter hängt davon ab, wie komplex die Abfrage ist.
>
> Beim Abfragen von Eigenschaftswerten mit einem **uint64-** oder **sint64-Datentyp** in einer Skriptsprache wie VBScript gibt WMI Zeichenfolgenwerte zurück. Unerwartete Ergebnisse können beim Vergleichen dieser Werte auftreten, da das Vergleichen von Zeichenfolgen andere Ergebnisse als das Vergleichen von Zahlen zurückgibt. Beispielsweise ist "100000000000" beim Vergleichen von Zeichenfolgen kleiner als "9", und 9 ist kleiner als 10000000000 beim Vergleichen von Zahlen. Um Verwirrung zu vermeiden, sollten Sie die [CDbl-Methode](/previous-versions//ftekwwt0(v=vs.85)) in VBScript verwenden, wenn Eigenschaften vom Typ **uint64** oder **sint64** aus WMI abgerufen werden.

 

> [!Note]  

 

Weitere Informationen finden Sie unter [Bearbeiten von Klassen- und Instanzinformationen.](manipulating-class-and-instance-information.md)

 

