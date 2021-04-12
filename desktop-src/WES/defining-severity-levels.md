---
title: Definieren von Schweregraden
description: Ebenen werden verwendet, um Ereignisse zu gruppieren und in der Regel den Schweregrad oder die Ausführlichkeit eines Ereignisses anzugeben.
ms.assetid: dfa4e0a9-4d89-4f50-aef9-1dae0dc11726
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c8e2e979e75057a77cca267e540b3ec5469562f
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2020
ms.locfileid: "104390089"
---
# <a name="defining-severity-levels"></a><span data-ttu-id="6a670-103">Definieren von Schweregraden</span><span class="sxs-lookup"><span data-stu-id="6a670-103">Defining Severity Levels</span></span>

<span data-ttu-id="6a670-104">Ebenen werden verwendet, um Ereignisse zu gruppieren und in der Regel den Schweregrad oder die Ausführlichkeit eines Ereignisses anzugeben.</span><span class="sxs-lookup"><span data-stu-id="6a670-104">Levels are used to group events and typically indicate the severity or verbosity of an event.</span></span> <span data-ttu-id="6a670-105">Verwenden Sie das **Level** -Element, um eine Ebene zu definieren.</span><span class="sxs-lookup"><span data-stu-id="6a670-105">To define a level, use the **level** element.</span></span> <span data-ttu-id="6a670-106">Die Winmeta.xml Datei definiert die folgenden häufig verwendeten Schweregrade:</span><span class="sxs-lookup"><span data-stu-id="6a670-106">The Winmeta.xml file defines the following commonly used severity levels:</span></span>

-   <span data-ttu-id="6a670-107">win:Critical</span><span class="sxs-lookup"><span data-stu-id="6a670-107">win:Critical</span></span>
-   <span data-ttu-id="6a670-108">win:Error</span><span class="sxs-lookup"><span data-stu-id="6a670-108">win:Error</span></span>
-   <span data-ttu-id="6a670-109">win:Warning</span><span class="sxs-lookup"><span data-stu-id="6a670-109">win:Warning</span></span>
-   <span data-ttu-id="6a670-110">win:Informational</span><span class="sxs-lookup"><span data-stu-id="6a670-110">win:Informational</span></span>
-   <span data-ttu-id="6a670-111">win:Verbose</span><span class="sxs-lookup"><span data-stu-id="6a670-111">win:Verbose</span></span>

<span data-ttu-id="6a670-112">Consumer verwenden Ebenen zum Abfragen von Ereignissen, die einen bestimmten Level-Wert enthalten.</span><span class="sxs-lookup"><span data-stu-id="6a670-112">Consumers use levels to query for events that contain a specific level value.</span></span> <span data-ttu-id="6a670-113">Eine ETW-Ablauf Verfolgungs Sitzung kann auch Ebenen verwenden, um die Ereignisse einzuschränken, die in die Protokolldatei für die Ereignis Ablauf Verfolgung geschrieben werden. Ereignisse mit einem ebenendwert, der gleich oder kleiner als der angegebene ebenendwert ist, werden in die Protokolldatei geschrieben.</span><span class="sxs-lookup"><span data-stu-id="6a670-113">An ETW tracing session can also use levels to limit the events that are written to the event tracing log file; events with a level value equal to or less than the specified level value are written to the log file.</span></span> <span data-ttu-id="6a670-114">Wenn die Sitzung z. b. den Level-Wert für Win: Warning angegeben hat, enthält die Protokolldatei Warnungen, Fehler und kritische Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="6a670-114">For example, if the session specified the level value for win:Warning, the log file would contain warning, error, and critical events.</span></span>

<span data-ttu-id="6a670-115">Im folgenden Beispiel wird gezeigt, wie eine Ebene definiert wird.</span><span class="sxs-lookup"><span data-stu-id="6a670-115">The following example shows how to define a level.</span></span> <span data-ttu-id="6a670-116">Sie müssen die Attribute **Name** und **value** der Ebene angeben.</span><span class="sxs-lookup"><span data-stu-id="6a670-116">You must specify the level's **name** and **value** attributes.</span></span> <span data-ttu-id="6a670-117">Der Wert des **value** -Attributs muss zwischen 16 und 255 liegen.</span><span class="sxs-lookup"><span data-stu-id="6a670-117">The value of the **value** attribute must be in the range from 16 through 255.</span></span> <span data-ttu-id="6a670-118">Das **Symbol** und die **Nachrichten** Attribute sind optional.</span><span class="sxs-lookup"><span data-stu-id="6a670-118">The **symbol** and **message** attributes are optional.</span></span>


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

                <levels>
                    <level name="NotValid"
                           value="16"
                           symbol="LEVEL_SAMPLEPROVIDER_NOTVALID"
                           message="$(string.Level.NotValid)"/>
                    <level name="Valid"
                           value="17"
                           symbol="LEVEL_SAMPLEPROVIDER_VALID"
                           message="$(string.Level.Valid)"/>
                </levels>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Sample Provider"/>
                <string id="Level.Valid" value="Valid"/>
                <string id="Level.NotValid" value="Not Valid"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```
