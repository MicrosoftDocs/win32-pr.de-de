---
description: Nachdem Sie eine Ereignisablaufverfolgungssitzung gestartet haben, können Sie TraceSetInformation verwenden, um das System anzuweisen, zusätzliche Ereignisablaufverfolgungsdaten zurückzugeben.
ms.assetid: 65CCD658-869E-40C4-83AE-34CC2720B7CB
title: Abrufen zusätzlicher Ereignisablaufverfolgungsdaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afbae65e516a63154fb76d3d558e02e9533e58e119e977f851c2404f0a218ec5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393898"
---
# <a name="retrieving-additional-event-tracing-data"></a>Abrufen zusätzlicher Ereignisablaufverfolgungsdaten

Nachdem Sie eine Ereignisablaufverfolgungssitzung gestartet haben, können Sie [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) verwenden, um das System anzuweisen, zusätzliche Ereignisablaufverfolgungsdaten zurückzugeben. Die zusätzlichen Informationen werden im erweiterten Datenabschnitt der relevanten Ereignisablaufverfolgung platziert.

Im folgenden Verfahren wird beschrieben, wie Sie die [**TraceSetInformation-Funktion**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) verwenden, um zusätzliche Daten aus einer Ereignisablaufverfolgungssitzung abzurufen.

**So rufen Sie zusätzliche Ereignisablaufverfolgungsdaten ab**

1.  Starten Sie Ihre Sitzung mit einem Aufruf von [**StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea)

    Weitere Informationen finden Sie unter [Konfigurieren und Starten einer Ereignisablaufverfolgungssitzung.](configuring-and-starting-an-event-tracing-session.md)

2.  Rufen Sie [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) auf, um zusätzliche Ereignisablaufverfolgungsdaten festzulegen.

    Verwenden Sie die [**EVENT \_ INFO \_ CLASS-Enumeration**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) im *ClassInformation-Parameter,* um die zusätzlichen Informationen zu beschreiben, die Sie abrufen möchten. Im folgenden Beispiel wird beschrieben, wie [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation)mithilfe des vom Aufruf von [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)zurückgegebenen Sitzungshandle und des **TraceProviderBinaryTracking-Werts** aus **der EVENT INFO \_ \_ CLASS** aufgerufen wird.

    ```C++
    BOOLEAN enabled = TRUE;
    Win32Error error = TraceSetInformation(
        m_sessionHandle,
        TraceProviderBinaryTracking,
        &enabled,
        sizeof(enabled));
    ```

    

3.  Alternativ können Sie [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) verwenden, um Informationen zu den aktuellen Einstellungen der Ereignisablaufverfolgungssitzung abzurufen.

    Wie [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation)verwendet [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) die [**EVENT INFO \_ \_ CLASS-Enumeration,**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) um zu beschreiben, welche Informationen aus dem System abgerufen werden sollen.

 

 
