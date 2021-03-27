---
description: Nachdem Sie eine Ereignis Ablauf Verfolgungs Sitzung gestartet haben, können Sie tracesetinformation verwenden, um das System anzuweisen, zusätzliche Ereignis Ablauf Verfolgungs Daten zurückzugeben.
ms.assetid: 65CCD658-869E-40C4-83AE-34CC2720B7CB
title: Abrufen von zusätzlichen Ereignis Ablauf Verfolgungs Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef864de40b924e0210603646d5ba5430d5d9b643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959121"
---
# <a name="retrieving-additional-event-tracing-data"></a>Abrufen von zusätzlichen Ereignis Ablauf Verfolgungs Daten

Nachdem Sie eine Ereignis Ablauf Verfolgungs Sitzung gestartet haben, können Sie [**tracesetinformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) verwenden, um das System anzuweisen, zusätzliche Ereignis Ablauf Verfolgungs Daten zurückzugeben. Die zusätzlichen Informationen werden im erweiterten Daten Abschnitt der relevanten Ereignis Ablauf Verfolgung abgelegt.

Im folgenden Verfahren wird beschrieben, wie die [**tracesetinformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) -Funktion verwendet wird, um zusätzliche Daten aus einer Ereignis Ablauf Verfolgungs Sitzung abzurufen.

**So rufen Sie zusätzliche Ereignis Ablauf Verfolgungs Daten ab**

1.  Starten Sie die Sitzung mit einem Aufrufen von [**starttrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea).

    Weitere Informationen finden Sie unter [Konfigurieren und Starten einer Ereignis Ablauf Verfolgungs Sitzung](configuring-and-starting-an-event-tracing-session.md).

2.  Ruft [**tracesetinformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) auf, um zusätzliche Ereignis Ablauf Verfolgungs Daten festzulegen.

    Verwenden Sie die [**Ereignis \_ Info- \_ Klassen**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) Enumeration im *classinformation* -Parameter, um die zusätzlichen Informationen zu beschreiben, die Sie abrufen möchten. Im folgenden Beispiel wird beschrieben, wie [**tracesetinformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation)mit dem Sitzungs Handle aufgerufen wird, das vom Aufrufen von [**starttrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)zurückgegeben wurde, und mit dem **traceproviderbinarytracking** -Wert aus der **Ereignis \_ Info- \_ Klasse**.

    ```C++
    BOOLEAN enabled = TRUE;
    Win32Error error = TraceSetInformation(
        m_sessionHandle,
        TraceProviderBinaryTracking,
        &enabled,
        sizeof(enabled));
    ```

    

3.  Alternativ können Sie [**tracequeryinformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) verwenden, um Informationen zu den aktuellen Sitzungs Einstellungen der Ereignis Ablauf Verfolgung abzurufen.

    Wie [**tracesetinformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation)verwendet [**tracequeryinformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) die [**Ereignis \_ Info- \_ Klassen**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) Enumeration, um zu beschreiben, welche Informationen aus dem System abgerufen werden sollen.

 

 
