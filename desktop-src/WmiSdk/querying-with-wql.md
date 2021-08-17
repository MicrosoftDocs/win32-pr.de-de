---
description: Die WMI Query Language (WQL) ist eine Teilmenge der standardmäßigen American National Standards Institute strukturierte Abfragesprache (ANSI SQL) mit geringfügigen semantischen Änderungen zur Unterstützung von WMI.
ms.assetid: 7e04ba37-c0e0-4304-b162-8b911f233f38
ms.tgt_platform: multiple
title: Abfragen mit WQL
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 737ae9505a0f775c26c5049eeb2f8500c9e3222d78181e18326ff53d39dfde01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118554831"
---
# <a name="querying-with-wql"></a>Abfragen mit WQL

Die WMI Query Language (WQL) ist eine Teilmenge der standardmäßigen American National Standards Institute strukturierte Abfragesprache (ANSI SQL) mit geringfügigen semantischen Änderungen zur Unterstützung von WMI.

Eine vollständige Liste der unterstützten WQL-Schlüsselwörter finden Sie unter [WQL (SQL für WMI).](wql-sql-for-wmi.md) Die Verwendung von SQL Schlüsselwörtern für Objekt- oder Eigenschaftsnamen kann die Analyse einer Abfrage einschränken. Die folgenden SQL Schlüsselwörter sind eingeschränkt: **NULL,** **TRUE** und **FALSE**.

> [!Note]  
> Die Anzahl von AND- und OR-Schlüsselwörtern, die in WQL-Abfragen verwendet werden können, ist begrenzt. Eine große Anzahl von WQL-Schlüsselwörtern, die in einer komplexen Abfrage verwendet werden, kann dazu führen, dass WMI den **WBEM \_ E \_ QUOTA \_ VIOLATION-Fehlercode** als **HRESULT-Wert** zurückgibt. Die Beschränkung der WQL-Schlüsselwörter hängt davon ab, wie komplex die Abfrage ist.

 

Abfragen können die **WHERE-Klausel** für Erweiterungen und Anpassungen verwenden, obwohl dies nicht erforderlich ist. Die **WHERE-Klausel** besteht aus einer Eigenschaft oder einem Schlüsselwort, einem Operator und einer Konstante. Alle **WHERE-Klauseln** müssen einen der vordefinierten Operatoren angeben, die in WQL enthalten sind. Weitere Informationen zur Syntax finden Sie unter [WHERE-Klausel.](where-clause.md) Weitere Informationen zu gültigen WQL-Operatoren finden Sie unter [WQL-Operatoren.](wql-operators.md)

Wie bei anderen SQL Abfragezeichenfolgen können Sie Ihre Abfragen mit Escapezeichen umgehen.

> [!Note]  
> WQL unterstützt keine namespaceübergreifenden Abfragen oder Zuordnungen. Sie können nicht alle Instanzen einer angegebenen Klasse abfragen, die sich in allen Namespaces auf dem Zielcomputer befinden.

 

WQL unterstützt die folgenden Abfragetypen:

-   Datenabfragen

    Datenabfragen werden verwendet, um Klasseninstanzen und Datenzuordnungen abzurufen. Sie sind der am häufigsten verwendete Abfragetyp in WMI-Skripts und -Anwendungen. Weitere Informationen zur Syntax von Datenabfragen finden Sie unter [Anfordern von Klasseninstanzdaten.](requesting-class-instance-data.md) Weitere Informationen zu Zuordnungen finden Sie unter [Deklarieren einer Zuordnungsklasse.](declaring-an-association-class.md)

    > [!Note]  
    > WQL unterstützt keine Abfragen von Arraydatentypen.

     

    Im folgenden Beispiel für eine Datenabfrage wird die Ereignisprotokolldatei mit dem Namen "Application" von allen Instanzen von [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent)angefordert.

    ```VB
    strComputer = "." 
    Set objWMIService = GetObject("winmgmts:\\" _
        & strComputer & "\root\CIMV2") 
    Set colItems = objWMIService.ExecQuery( _
        "SELECT * FROM Win32_NTLogEvent " _
        & "WHERE Logfile = 'Application'",,48)
    ```

    

-   Ereignisabfragen

    Consumer verwenden Ereignisabfragen, um sich zu registrieren, um Benachrichtigungen über Ereignisse zu erhalten. Ereignisanbieter verwenden Ereignisabfragen zur Registrierung, um ein oder mehrere Ereignisse zu unterstützen. Weitere Informationen zu Ereignisabfragen finden Sie unter [Empfangen von Ereignisbenachrichtigungen.](receiving-event-notifications.md)

    Die folgende Beispielereignisabfrage durch einen temporären Ereignisverbraucher fordert eine Benachrichtigung an, wenn eine neue Instanz einer von [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) abgeleiteten Klasse erstellt wird.

    ```VB
    strComputer = "." 
    Set objWMIService = GetObject("winmgmts:\\" _
        & strComputer & "\root\CIMV2") 
    Set objEvents = objWMIService.ExecNotificationQuery _
    ("SELECT * FROM __InstanceModificationEvent WITHIN 10 WHERE " & _
        "TargetInstance ISA 'Win32_Service'" & _
        " AND TargetInstance._Class = 'win32_TerminalService'")

    i = TRUE
    Do While i = TRUE
        Set strReceivedEvent = objEvents.NextEvent

        'report an event
        Wscript.Echo "An event has occurred."
    Loop
    ```

    

-   Schemaabfragen

    Schemaabfragen werden verwendet, um Klassendefinitionen (anstatt Klasseninstanzen) und Schemazuordnungen abzurufen. Klassenanbieter verwenden Schemaabfragen, um die Klassen anzugeben, die sie bei der Registrierung unterstützen. Weitere Informationen zu Schemaabfragen finden Sie unter [Abrufen von Klassendefinitionen.](retrieving-class-definitions.md)

    Die folgende Beispielschemaabfrage zeigt die spezielle Syntax.

    ```sql
    SELECT * FROM meta_class WHERE __this ISA "Win32_BaseService"
    ```

    

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Format für Datum und Uhrzeit](date-and-time-format.md)
</dt> </dl>

 

 
