---
description: Enumerationen verwenden tendenziell eine beträchtliche Menge an Systemressourcen.
ms.assetid: 4163e6c2-4ee3-4906-b297-618509666c90
ms.tgt_platform: multiple
title: Verbessern der enumerationsleistung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2554e9e1df2f2ece58f5703d6099d84acbe01c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217123"
---
# <a name="improving-enumeration-performance"></a><span data-ttu-id="2b575-103">Verbessern der enumerationsleistung</span><span class="sxs-lookup"><span data-stu-id="2b575-103">Improving Enumeration Performance</span></span>

<span data-ttu-id="2b575-104">Enumerationen verwenden tendenziell eine beträchtliche Menge an Systemressourcen.</span><span class="sxs-lookup"><span data-stu-id="2b575-104">Enumerations tend to use a significant amount of system resources.</span></span> <span data-ttu-id="2b575-105">Daher sollten Sie versuchen, den WMI-enumerationsprozess zu optimieren, wenn Sie in einer großen Gruppe Enumerationen ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="2b575-105">Therefore, you should try to optimize the WMI enumeration process if you plan on performing enumerations on a large group.</span></span> <span data-ttu-id="2b575-106">Skripts können auch eine Abfrage verwenden, um Leistungseinbußen in "for each.... Next"-Vorgängen mit einer großen Menge zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="2b575-106">Scripts can also use a query to avoid performance degradation in "For each….Next" operations with a large set.</span></span> <span data-ttu-id="2b575-107">Weitere Informationen finden Sie unter [WMI-Abfrage](querying-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="2b575-107">For more information, see [Querying WMI](querying-wmi.md).</span></span>

<span data-ttu-id="2b575-108">Im folgenden Verfahren wird beschrieben, wie die enumerationsleistung verbessert wird.</span><span class="sxs-lookup"><span data-stu-id="2b575-108">The following procedure describes how to improve enumeration performance.</span></span>

<span data-ttu-id="2b575-109">**So verbessern Sie die Enumeration**</span><span class="sxs-lookup"><span data-stu-id="2b575-109">**To improve enumeration performance**</span></span>

1.  <span data-ttu-id="2b575-110">Legen Sie den *lFlags* -Parameter fest, um die semisynchrone Rückgabe der Daten mit einem Enumerator zuzulassen, der jedes Element bei der Übermittlung aus WMI verwirft.</span><span class="sxs-lookup"><span data-stu-id="2b575-110">Set the *lFlags* parameter to allow semisynchronous return of the data with an enumerator that discards each item from WMI as it is delivered.</span></span> <span data-ttu-id="2b575-111">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="2b575-111">For more information, see [Calling a Method](calling-a-method.md).</span></span>

    <span data-ttu-id="2b575-112">Im folgenden C++-Codebeispiel wird gezeigt, wie das **WBEM- \_ Flag " \_ \_ immediate Return** " und das **WBEM-Flag " \_ \_ Forward \_ only** " verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2b575-112">The following C++ code example shows how to use the **WBEM\_FLAG\_RETURN\_IMMEDIATE** and **WBEM\_FLAG\_FORWARD\_ONLY** flags.</span></span>

    `WBEM_FLAG_RETURN_IMMEDIATE | WBEM_FLAG_FORWARD_ONLY`

    <span data-ttu-id="2b575-113">Verwenden Sie in VBScript oder Visual Basic die skriptingflags **wbemFlagReturnImmediately** und **wbemFlagForwardOnly** aus [wbemflagenum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).</span><span class="sxs-lookup"><span data-stu-id="2b575-113">In VBScript or Visual Basic, use the scripting flags **WbemFlagReturnImmediately** and **WbemFlagForwardOnly** from [WbemFlagEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).</span></span> <span data-ttu-id="2b575-114">Der kombinierte Wert dieser Flags ist Decimal 48.</span><span class="sxs-lookup"><span data-stu-id="2b575-114">The combined value of these flags is decimal 48.</span></span>

    <span data-ttu-id="2b575-115">Die Skripting-und Parameterflags bewirken folgendes Verhalten:</span><span class="sxs-lookup"><span data-stu-id="2b575-115">The scripting and parameter flags cause the following behavior:</span></span>

    -   <span data-ttu-id="2b575-116">Das **WBEM- \_ Flag \_ gibt das \_ unmittelbare** oder **wbemFlagReturnImmediately** -Flag zurück, das semisynchrone Verhalten anfordert.</span><span class="sxs-lookup"><span data-stu-id="2b575-116">The **WBEM\_FLAG\_RETURN\_IMMEDIATE** or **wbemFlagReturnImmediately** flag requests semisynchronous behavior.</span></span> <span data-ttu-id="2b575-117">Der-Befehl zum Erstellen des Enumerators wird sofort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2b575-117">The call to create the enumerator returns immediately.</span></span> <span data-ttu-id="2b575-118">Sie können dann beginnen, den Objekt Satz zu durchlaufen, den Sie erhalten.</span><span class="sxs-lookup"><span data-stu-id="2b575-118">You can then begin to traverse the object set that you receive.</span></span>
    -   <span data-ttu-id="2b575-119">Das Flag " **WBEM- \_ Flag \_ weiterleiten \_** " oder das Flag " **wbemFlagForwardOnly** " fordert einen Enumerator an, den Sie nicht zurückspulen können.</span><span class="sxs-lookup"><span data-stu-id="2b575-119">The **WBEM\_FLAG\_FORWARD\_ONLY** flag or **wbemFlagForwardOnly** flag requests an enumerator that you cannot rewind.</span></span> <span data-ttu-id="2b575-120">Das heißt, dass WMI ein Objekt freigeben kann, nachdem Sie das Objekt angezeigt haben.</span><span class="sxs-lookup"><span data-stu-id="2b575-120">That is, WMI can release an object after you view the object.</span></span>

    <span data-ttu-id="2b575-121">In Situationen, in denen die Enumeration groß ist und die Anwendung sehr schnell ist, ermöglicht die Verwendung von vorwärts-Enumeratoren mit semisynchroner Verarbeitung, dass WMI viel weniger Objekte speichert, wodurch die Reaktionszeit und die Arbeitsspeicher Leistung erheblich erhöht werden.</span><span class="sxs-lookup"><span data-stu-id="2b575-121">In situations where the enumeration is large and the application is very fast, using forward-only enumerators with semisynchronous processing allows WMI to hold on to far fewer objects, thereby increasing response time and memory performance significantly.</span></span>

    <span data-ttu-id="2b575-122">Im folgenden VBScript-Codebeispiel wird veranschaulicht, wie Sie mithilfe der kombinierten **wbemFlagReturnImmediately** -und **wbemFlagForwardOnly** -Flags eine Auflistung von Ereignissen aus einem Ereignisprotokoll abrufen.</span><span class="sxs-lookup"><span data-stu-id="2b575-122">The following VBScript code example shows how to make a call using the combined **wbemFlagReturnImmediately** and **wbemFlagForwardOnly** flags to obtain a collection of events from an event log.</span></span>

    ```VB
    Set Events = GetObject("winmgmts:").ExecQuery _
         ("SELECT * FROM Win32_NTLogEvent " _
          & "WHERE Logfile = 'System'",,48)
    ```

    

2.  <span data-ttu-id="2b575-123">Vermeiden Sie nach Möglichkeit die Verwendung von "" in "C++" oder " [**slibemservices. InstancesOf**](swbemservices-instancesof.md)" mit der Verwendung von "" [**. verwenden Sie**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) stattdessen " **ExecQuery**".</span><span class="sxs-lookup"><span data-stu-id="2b575-123">Whenever possible, avoid using [**CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) in C++ or [**SWbemServices.InstancesOf**](swbemservices-instancesof.md), and instead use **ExecQuery**.</span></span>

    <span data-ttu-id="2b575-124">Von der **ExecQuery** -Methode wird WMI mithilfe von Datenbanktechnologien abgefragt, während mit "" von "" "" "" "," "," [**"und"**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) [**slibemservices. InstancesOf**](swbemservices-instancesof.md) "</span><span class="sxs-lookup"><span data-stu-id="2b575-124">The **ExecQuery** method queries WMI using database technologies, while [**CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) or [**SWbemServices.InstancesOf**](swbemservices-instancesof.md) enumerates WMI objects.</span></span> <span data-ttu-id="2b575-125">Insbesondere kann **ExecQuery** bestimmte Teilmengen von Daten anfordern, die von den enumeringmethoden nicht möglich sind.</span><span class="sxs-lookup"><span data-stu-id="2b575-125">Specifically, **ExecQuery** can request specific subsets of data that the enumerating methods cannot.</span></span>

    <span data-ttu-id="2b575-126">Da einige Anbieter keine Abfragefunktionen haben, bietet WMI eine Funktion für den Post-Filter, die es WMI ermöglicht, Instanzen zu verwerfen, die die Spezifikationen einer Abfrage nicht erfüllen.</span><span class="sxs-lookup"><span data-stu-id="2b575-126">Because some providers do not have querying capabilities, WMI provides a "post filter" feature that allows WMI to discard instances that do not fulfill a query's specifications.</span></span> <span data-ttu-id="2b575-127">Ob ein bestimmter Anbieter dieses Feature nutzt, ist der Autor des Anbieters.</span><span class="sxs-lookup"><span data-stu-id="2b575-127">Whether a particular provider takes advantage of this feature is up to the provider author.</span></span>

3.  <span data-ttu-id="2b575-128">Experimentieren Sie mit verschiedenen Abfragen, um zu bestimmen, was Ihnen die beste Leistung bietet.</span><span class="sxs-lookup"><span data-stu-id="2b575-128">Experiment with different queries to determine what gives you the best performance.</span></span>

    <span data-ttu-id="2b575-129">WMI verarbeitet z. b. nur selten Abfragen mit **Where** -Klauseln der Form Eigenschaft PROP1 < "x".</span><span class="sxs-lookup"><span data-stu-id="2b575-129">For example, WMI seldom efficiently processes queries with **WHERE** clauses of the form Prop1 < "x".</span></span> <span data-ttu-id="2b575-130">Im Gegensatz dazu verarbeitet WMI in der Regel effizient Abfragen der Form KeyProp1 = "x".</span><span class="sxs-lookup"><span data-stu-id="2b575-130">In contrast, WMI normally processes queries of the form KeyProp1 = "x" efficiently.</span></span>

<span data-ttu-id="2b575-131">Weitere Informationen finden Sie unter Auflisten von [WMI](enumerating-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="2b575-131">For more information, see [Enumerating WMI](enumerating-wmi.md).</span></span>

 

 



