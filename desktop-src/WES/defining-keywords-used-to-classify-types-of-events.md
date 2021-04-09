---
title: Definieren von Schlüsselwörtern zum Klassifizieren von Ereignis Typen
description: Anbieter verwenden Schlüsselwörter, um unterschiedliche Arten von Ereignissen zu klassifizieren.
ms.assetid: 1cbad719-bc59-4255-8a15-9e45f363d199
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d48992c5cbafec5f945fa2f133924ccf0e2e7e96
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2020
ms.locfileid: "103858092"
---
# <a name="defining-keywords-used-to-classify-types-of-events"></a><span data-ttu-id="7edbd-103">Definieren von Schlüsselwörtern zum Klassifizieren von Ereignis Typen</span><span class="sxs-lookup"><span data-stu-id="7edbd-103">Defining Keywords Used to Classify Types of Events</span></span>

<span data-ttu-id="7edbd-104">Anbieter verwenden Schlüsselwörter, um unterschiedliche Arten von Ereignissen zu klassifizieren.</span><span class="sxs-lookup"><span data-stu-id="7edbd-104">Providers use keywords to classify different types of events.</span></span> <span data-ttu-id="7edbd-105">Sie können z. b. ein Schlüsselwort für alle Lese Ereignisse erstellen und dann das Read-Schlüsselwort auf jedes Ereignis anwenden, das einen Lesevorgang ausführt, z. b. das Lesen aus einer Datei oder einer Registrierung.</span><span class="sxs-lookup"><span data-stu-id="7edbd-105">For example, you can create a keyword for all read events and then apply the read keyword to any event that performs a read operation such as reading from a file or registry.</span></span> <span data-ttu-id="7edbd-106">Consumer können dann die Bitwerte des-Schlüssel Worts verwenden, um nach einer anderen Klassifizierung von Ereignissen zu filtern.</span><span class="sxs-lookup"><span data-stu-id="7edbd-106">Consumers could then use the keyword bit values to filter for different classification of events.</span></span> <span data-ttu-id="7edbd-107">Der Consumer könnte z. b. alle Lese Ereignisse oder alle gelesenen Ereignisse von Aufgabe X anfordern (wenn Sie auch Ereignisse nach Aufgabe gruppieren).</span><span class="sxs-lookup"><span data-stu-id="7edbd-107">For example, the consumer could request all read events or all read events from task X (if you also group events by task).</span></span> <span data-ttu-id="7edbd-108">Um ein Schlüsselwort zu definieren, verwenden Sie das- **Schlüsselwort** Element.</span><span class="sxs-lookup"><span data-stu-id="7edbd-108">To define a keyword, use the **keyword** element.</span></span>

<span data-ttu-id="7edbd-109">Eine ETW-Ablauf Verfolgungs Sitzung kann die Schlüsselwörter (auf die gleiche Weise wie die Ebene) verwenden, um die Ereignisse einzuschränken, die der etw-Dienst in seine Ereignis Ablauf Verfolgungs Protokolldatei schreibt.</span><span class="sxs-lookup"><span data-stu-id="7edbd-109">An ETW tracing session can use the keywords (in the same way that it uses level) to limit the events that the ETW service writes to its event tracing log file.</span></span> <span data-ttu-id="7edbd-110">Eine Ablauf Verfolgungs Sitzung kann den Anbieter mithilfe von zwei Sätzen von Schlüsselwort-Bitmasks aktivieren: eine "beliebige" Bitmaske, bei der das Ereignis geschrieben wird, wenn eines der Schlüsselwort Bits eines Ereignisses mit einer der in dieser Maske festgelegten Bits übereinstimmt, und einer "All"-Bitmaske, bei der für die Ereignisse, die mit "Any" übereinstimmen, das Ereignis nur dann geschrieben wird, wenn alle Bits in der "All"-Maske in der</span><span class="sxs-lookup"><span data-stu-id="7edbd-110">A tracing session can enable the provider using two sets of keyword bitmasks: an "Any" bitmask where the event is written if any of the event's keyword bits match any of the bits set in this mask, and an "All" bitmask where for those events that matched the "Any" case, the event is written only if all of the bits in the "All" mask exist in the event's keyword bitmask.</span></span>

<span data-ttu-id="7edbd-111">Wenn der Anbieter z. b. ein Ereignis definiert, das ein Lese Schlüsselwort (Bit 0) und ein lokales Zugriffs Schlüsselwort (Bit 1) angibt, und ein zweites Ereignis, das ein Read-Schlüsselwort (Bit 0) und ein RAS-Schlüsselwort (Bit 2) angibt, können Sie die Bitmaske "Any" auf 1 festlegen, um alle Lese Ereignisse zu empfangen, oder Sie können die Bitmaske "beliebig" auf 1 und die Bitmaske "All" auf "3" festlegen, um nur lokale Lese</span><span class="sxs-lookup"><span data-stu-id="7edbd-111">For example, if the provider defines an event that specifies a read keyword (bit 0) and a local access keyword (bit 1), and a second event that specifies a read keyword (bit 0) and a remote access keyword (bit 2), you could set the "Any" bitmask to 1 to receive all read events, or you could set the "Any" bitmask to 1 and "All" bitmask to 3 to receive only local reads.</span></span>

<span data-ttu-id="7edbd-112">Sie müssen die Attribute **Name** und **Mask** des Schlüssel Worts angeben.</span><span class="sxs-lookup"><span data-stu-id="7edbd-112">You must specify the keyword's **name** and **mask** attributes.</span></span> <span data-ttu-id="7edbd-113">Die Maske muss nur ein Bit zwischen Bit 0 und Bit 47 festlegen.</span><span class="sxs-lookup"><span data-stu-id="7edbd-113">The mask must set only one bit, between bit 0 and bit 47.</span></span> <span data-ttu-id="7edbd-114">Bits 48 bis 64 sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="7edbd-114">Bits 48 through 64 are reserved.</span></span>

<span data-ttu-id="7edbd-115">Das **Symbol** und die **Nachrichten** Attribute sind optional.</span><span class="sxs-lookup"><span data-stu-id="7edbd-115">The **symbol** and **message** attributes are optional.</span></span>

<span data-ttu-id="7edbd-116">Im folgenden Beispiel wird gezeigt, wie Sie ein Schlüsselwort definieren.</span><span class="sxs-lookup"><span data-stu-id="7edbd-116">The following example shows how to define a keyword.</span></span>

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

                <keywords>
                    <keyword name="Read" mask="0x1" symbol="READ_KEYWORD"/>
                    <keyword name="Write" mask="0x2" symbol="WRITE_KEYWORD"/>
                    <keyword name="Local" mask="0x4" symbol="LOCAL_KEYWORD"/>
                    <keyword name="Remote" mask="0x8" symbol="REMOTE_KEYWORD"/>
                </keywords>

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
