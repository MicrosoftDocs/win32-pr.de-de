---
description: Der WMI Query Language (WQL) ist eine Teilmenge der Standard American National Standards Institute Structured Query Language (ANSI SQL) mit geringfügigen Semantik Änderungen, um WMI zu unterstützen.
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
ms.openlocfilehash: 8e2d3f68f4d7384781110958070b33b67a78405f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347071"
---
# <a name="querying-with-wql"></a>Abfragen mit WQL

Der WMI Query Language (WQL) ist eine Teilmenge der Standard American National Standards Institute Structured Query Language (ANSI SQL) mit geringfügigen Semantik Änderungen, um WMI zu unterstützen.

Eine umfassende Liste der unterstützten WQL-Schlüsselwörter finden Sie unter [WQL (SQL für WMI)](wql-sql-for-wmi.md). Durch die Verwendung von SQL-Schlüsselwörtern für Objekt-oder Eigenschaftsnamen kann eine Abfrage möglicherweise nicht analysiert werden. Die folgenden SQL-Schlüsselwörter sind eingeschränkt: **null**, **true** und **false**.

> [!Note]  
> Es gibt Einschränkungen für die Anzahl von-und-oder-Schlüsselwörtern, die in WQL-Abfragen verwendet werden können. Eine große Anzahl von WQL-Schlüsselwörtern, die in einer komplexen Abfrage verwendet werden, kann bewirken, dass WMI den Fehlercode der **WBEM \_ E- \_ Kontingent \_ Verletzung** als **HRESULT** -Wert zurückgibt Das Limit von WQL-Schlüsselwörtern hängt von der Komplexität der Abfrage ab.

 

Abfragen können die **Where** -Klausel für Erweiterung und Anpassung verwenden, obwohl Sie nicht erforderlich ist. Die **Where** -Klausel besteht aus einer Eigenschaft oder einem Schlüsselwort, einem Operator und einer Konstante. Alle **Where** -Klauseln müssen einen der vordefinierten Operatoren angeben, die in WQL enthalten sind. Weitere Informationen zur Syntax finden Sie unter [WHERE-Klausel](where-clause.md). Weitere Informationen zu gültigen WQL-Operatoren finden Sie unter [WQL-Operatoren](wql-operators.md).

Wie bei anderen SQL-Abfrage Zeichenfolgen können Sie Ihre Abfragen mit Escapezeichen versehen.

> [!Note]  
> WQL unterstützt keine Namespace übergreifende Abfragen oder Zuordnungen. Es ist nicht möglich, alle Instanzen einer bestimmten Klasse abzufragen, die sich in allen Namespaces auf dem Bereitstellungs Zielcomputer befinden.

 

WQL unterstützt die folgenden Typen von Abfragen:

-   Daten Abfragen

    Daten Abfragen werden verwendet, um Klassen Instanzen und Daten Zuordnungen abzurufen. Dabei handelt es sich um den am häufigsten verwendeten Abfragetyp in WMI-Skripts und-Anwendungen. Weitere Informationen zur Syntax von Daten Abfragen finden Sie unter [anfordern von klasseninstanzdaten](requesting-class-instance-data.md). Weitere Informationen zu Zuordnungen finden Sie unter [Deklarieren einer Association-Klasse](declaring-an-association-class.md).

    > [!Note]  
    > WQL unterstützt keine Abfragen von Array Datatypes.

     

    Im folgenden Beispiel für eine Datenabfrage wird die Ereignisprotokoll Datei "Application" aus allen Instanzen von [**Win32 \_ ntlogevent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent)angefordert.

    ```VB
    strComputer = "." 
    Set objWMIService = GetObject("winmgmts:\\" _
        & strComputer & "\root\CIMV2") 
    Set colItems = objWMIService.ExecQuery( _
        "SELECT * FROM Win32_NTLogEvent " _
        & "WHERE Logfile = 'Application'",,48)
    ```

    

-   Ereignis Abfragen

    Consumer verwenden Ereignis Abfragen, um sich für den Empfang von Benachrichtigungen über Ereignisse zu registrieren. Ereignis Anbieter verwenden Ereignis Abfragen zur Registrierung, um ein oder mehrere Ereignisse zu unterstützen. Weitere Informationen zu Ereignis Abfragen finden Sie unter [empfangen von Ereignis Benachrichtigungen](receiving-event-notifications.md).

    Die folgende Beispiel Ereignis Abfrage durch einen temporären Ereignisconsumer fordert eine Benachrichtigung an, wenn eine neue Instanz einer Klasse erstellt wird, die von [**Win32 \_ ntlogevent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) abgeleitet wurde.

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

    

-   Schema Abfragen

    Schema Abfragen werden verwendet, um Klassendefinitionen (anstelle von Klassen Instanzen) und Schema Zuordnungen abzurufen. Klassen Anbieter verwenden Schema Abfragen, um die Klassen anzugeben, die Sie bei der Registrierung unterstützen. Weitere Informationen zu Schema Abfragen finden Sie unter [Abrufen von Klassendefinitionen](retrieving-class-definitions.md).

    Die folgende Beispiel Schema Abfrage zeigt die spezielle Syntax.

    ```sql
    SELECT * FROM meta_class WHERE __this ISA "Win32_BaseService"
    ```

    

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Format für Datum und Uhrzeit](date-and-time-format.md)
</dt> </dl>

 

 
