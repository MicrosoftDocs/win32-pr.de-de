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
# <a name="retrieving-additional-event-tracing-data"></a><span data-ttu-id="9f5ae-103">Abrufen von zusätzlichen Ereignis Ablauf Verfolgungs Daten</span><span class="sxs-lookup"><span data-stu-id="9f5ae-103">Retrieving Additional Event Tracing Data</span></span>

<span data-ttu-id="9f5ae-104">Nachdem Sie eine Ereignis Ablauf Verfolgungs Sitzung gestartet haben, können Sie [**tracesetinformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) verwenden, um das System anzuweisen, zusätzliche Ereignis Ablauf Verfolgungs Daten zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="9f5ae-104">Once you have begun an event tracing session, you can use [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) to instruct the system to return additional event tracing data.</span></span> <span data-ttu-id="9f5ae-105">Die zusätzlichen Informationen werden im erweiterten Daten Abschnitt der relevanten Ereignis Ablauf Verfolgung abgelegt.</span><span class="sxs-lookup"><span data-stu-id="9f5ae-105">The additional information will be placed in the extended data section of the relevant event trace.</span></span>

<span data-ttu-id="9f5ae-106">Im folgenden Verfahren wird beschrieben, wie die [**tracesetinformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) -Funktion verwendet wird, um zusätzliche Daten aus einer Ereignis Ablauf Verfolgungs Sitzung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9f5ae-106">The following procedure describes how to use the [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) function to retrieve additional data from an event tracing session.</span></span>

<span data-ttu-id="9f5ae-107">**So rufen Sie zusätzliche Ereignis Ablauf Verfolgungs Daten ab**</span><span class="sxs-lookup"><span data-stu-id="9f5ae-107">**To retrieve additional event tracing data**</span></span>

1.  <span data-ttu-id="9f5ae-108">Starten Sie die Sitzung mit einem Aufrufen von [**starttrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea).</span><span class="sxs-lookup"><span data-stu-id="9f5ae-108">Start your session with a call to [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea).</span></span>

    <span data-ttu-id="9f5ae-109">Weitere Informationen finden Sie unter [Konfigurieren und Starten einer Ereignis Ablauf Verfolgungs Sitzung](configuring-and-starting-an-event-tracing-session.md).</span><span class="sxs-lookup"><span data-stu-id="9f5ae-109">For more information, see [Configuring and Starting an Event Tracing Session](configuring-and-starting-an-event-tracing-session.md).</span></span>

2.  <span data-ttu-id="9f5ae-110">Ruft [**tracesetinformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) auf, um zusätzliche Ereignis Ablauf Verfolgungs Daten festzulegen.</span><span class="sxs-lookup"><span data-stu-id="9f5ae-110">Call [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) to set additional event tracing data.</span></span>

    <span data-ttu-id="9f5ae-111">Verwenden Sie die [**Ereignis \_ Info- \_ Klassen**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) Enumeration im *classinformation* -Parameter, um die zusätzlichen Informationen zu beschreiben, die Sie abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="9f5ae-111">use the [**EVENT\_INFO\_CLASS**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) enumeration in the *ClassInformation* parameter to describe the additional information you wish to retrieve.</span></span> <span data-ttu-id="9f5ae-112">Im folgenden Beispiel wird beschrieben, wie [**tracesetinformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation)mit dem Sitzungs Handle aufgerufen wird, das vom Aufrufen von [**starttrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)zurückgegeben wurde, und mit dem **traceproviderbinarytracking** -Wert aus der **Ereignis \_ Info- \_ Klasse**.</span><span class="sxs-lookup"><span data-stu-id="9f5ae-112">The following example describes how to call [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation), using the session handle returned from the call to [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea), and the **TraceProviderBinaryTracking** value from **EVENT\_INFO\_CLASS**.</span></span>

    ```C++
    BOOLEAN enabled = TRUE;
    Win32Error error = TraceSetInformation(
        m_sessionHandle,
        TraceProviderBinaryTracking,
        &enabled,
        sizeof(enabled));
    ```

    

3.  <span data-ttu-id="9f5ae-113">Alternativ können Sie [**tracequeryinformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) verwenden, um Informationen zu den aktuellen Sitzungs Einstellungen der Ereignis Ablauf Verfolgung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9f5ae-113">Alternately, you can use [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) to retrieve information about the current event tracing session settings.</span></span>

    <span data-ttu-id="9f5ae-114">Wie [**tracesetinformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation)verwendet [**tracequeryinformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) die [**Ereignis \_ Info- \_ Klassen**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) Enumeration, um zu beschreiben, welche Informationen aus dem System abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9f5ae-114">Like [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation), [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) uses the [**EVENT\_INFO\_CLASS**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) enumeration to describe what information to retrieve from the system.</span></span>

 

 
