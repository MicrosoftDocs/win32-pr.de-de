---
title: Definieren von Filtern
description: Ein Anbieter kann Filter definieren, die eine Sitzung verwendet, um Ereignisse auf der Grundlage von Ereignisdaten zu filtern.
ms.assetid: b43912af-0e9c-414b-b3fa-03e7e35e493c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61dd2a21b9c4e01ebc4a32a160b24022c79197b0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102207"
---
# <a name="defining-filters"></a><span data-ttu-id="51160-103">Definieren von Filtern</span><span class="sxs-lookup"><span data-stu-id="51160-103">Defining Filters</span></span>

<span data-ttu-id="51160-104">Ein Anbieter kann Filter definieren, die eine Sitzung verwendet, um Ereignisse auf der Grundlage von Ereignisdaten zu filtern.</span><span class="sxs-lookup"><span data-stu-id="51160-104">A provider can define filters that a session uses to filter events based on event data.</span></span> <span data-ttu-id="51160-105">Mit der Ebene und den Schlüsselwörtern bestimmt etw, ob das Ereignis in das Protokoll geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="51160-105">With level and keywords, ETW determines whether the event is written to the log.</span></span> <span data-ttu-id="51160-106">Allerdings verwendet der Anbieter mit Filtern die Filterdaten Kriterien, die die steuernde Sitzung an ihn übergibt (siehe die [*enablecallback*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback) -Funktion), um zu bestimmen, ob das Ereignis in diese Sitzung geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="51160-106">However, with filters, the provider uses the filter data criteria that the controlling session passes to it (see the [*EnableCallback*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback) function) to determine whether it writes the event to that session.</span></span> <span data-ttu-id="51160-107">Die Filter sind nur anwendbar, wenn der Anbieter durch eine ETW-Ablauf Verfolgungs Sitzung aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="51160-107">The filters are applicable only when an ETW tracing session enables your provider.</span></span>

<span data-ttu-id="51160-108">In der Regel schreiben Anbieter nur Ereignisse, und die Sitzung identifiziert die Typen von Ereignissen, die Sie mit der Ebene und den Schlüsselwörtern verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="51160-108">Typically, providers just write events, and the session identifies the types of events that it wants using level and keywords.</span></span> <span data-ttu-id="51160-109">Wenn der Anbieter einen Daten Filter für einen Ereignistyp definiert hat, kann er von der Sitzung verwendet werden, um Ereignisse für diesen Ereignistyp basierend auf den Ereignisdaten herauszufiltern (die Semantik des Filters wird vom Anbieter definiert).</span><span class="sxs-lookup"><span data-stu-id="51160-109">If the provider defined a data filter for an event type, the session could use it to filter out events for that event type based on the event data (the semantics of the filter is defined by the provider).</span></span> <span data-ttu-id="51160-110">Wenn Ihr Anbieter z. b. Prozess Ereignisse generiert, können Sie einen Daten Filter definieren, der Prozess Ereignisse auf der Grundlage eines Prozess Bezeichners gefiltert hat.</span><span class="sxs-lookup"><span data-stu-id="51160-110">For example, if your provider generates process events, you could define a data filter that filtered process events based on a process identifier.</span></span> <span data-ttu-id="51160-111">Die Sitzung kann dann eine Prozess-ID als Filterdaten an den Anbieter übergeben und nur Prozess Ereignisse für diese Prozess-ID empfangen.</span><span class="sxs-lookup"><span data-stu-id="51160-111">The session could then pass a process identifier as filter data to the provider and receive only process events for that process identifier.</span></span>

<span data-ttu-id="51160-112">Im folgenden Beispiel wird gezeigt, wie das **Filter** -Element verwendet wird, um einen Filter zu definieren.</span><span class="sxs-lookup"><span data-stu-id="51160-112">The following example shows how to use the **filter** element to define a filter.</span></span> <span data-ttu-id="51160-113">Sie müssen die Attribute **Name** und **value** des Filters angeben. die anderen Attribute sind optional.</span><span class="sxs-lookup"><span data-stu-id="51160-113">You must specify the filter's **name** and **value** attributes; the other attributes are optional.</span></span> <span data-ttu-id="51160-114">Das **TID** -Attribut ist erforderlich, wenn der Filter erfordert, dass die Sitzung Filterdaten übergibt.</span><span class="sxs-lookup"><span data-stu-id="51160-114">The **tid** attribute is required if the filter requires that the session pass filter data.</span></span>


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="http://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="http://www.w3.org/2001/XMLSchema"
    >

    <instrumentation>
        <events>
            <provider name="Microsoft-Windows-SampleProvider"
                guid="{1db28f2e-8f80-4027-8c5a-a11f7f10f62d}"
                symbol="PROVIDER_GUID"
                resourceFileName="<path to the exe or dll that contains the metadata resources>"
                messageFileName="<path to the exe or dll that contains the string resources>"
                message="$(string.Provider.Name)">

                . . .

                <filters>
                    <filter name="Pid"
                            value="1"
                            tid="t1"
                            symbol="FILTER_PID"/>
                </filters>

                <templates>
                    <template tid="t1">
                        <data name="Pid" inType="win:UInt32"/>
                    </template>
                </templates>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Sample Provider"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```