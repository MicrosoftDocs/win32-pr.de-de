---
title: Definieren von Kanälen
description: Ereignisse können in Ereignisprotokoll Kanäle, Ereignis Ablauf Verfolgungs Protokolldateien oder beides geschrieben werden. Ein Kanal ist im Grunde genommen eine Senke, die Ereignisse sammelt.
ms.assetid: 3c2f39ee-fbc0-40ae-8279-566905250f47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab3c73697aa11e7b63ace0ece33be23ca7a1b883
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2020
ms.locfileid: "104101362"
---
# <a name="defining-channels"></a><span data-ttu-id="a8cc1-104">Definieren von Kanälen</span><span class="sxs-lookup"><span data-stu-id="a8cc1-104">Defining Channels</span></span>

<span data-ttu-id="a8cc1-105">Ereignisse können in Ereignisprotokoll Kanäle, Ereignis Ablauf Verfolgungs Protokolldateien oder beides geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="a8cc1-105">Events can be written to event log channels, event tracing log files, or both.</span></span> <span data-ttu-id="a8cc1-106">Ein Kanal ist im Grunde genommen eine Senke, die Ereignisse sammelt.</span><span class="sxs-lookup"><span data-stu-id="a8cc1-106">A channel is basically a sink that collects events.</span></span> <span data-ttu-id="a8cc1-107">Wenn die Zielgruppe für Ihre Ereignisse Ereignisconsumer verwendet, z. b. die Windows-Ereignisanzeige, müssen Sie neue Kanäle definieren, um die Ereignisse zu erfassen oder einen von einem anderen Anbieter definierten vorhandenen Kanal zu importieren.</span><span class="sxs-lookup"><span data-stu-id="a8cc1-107">If the target audience for your events uses event consumers such as the Windows Event Viewer, you must define new channels to collect your events or import an existing channel that another provider defined.</span></span>

<span data-ttu-id="a8cc1-108">Verwenden Sie das **Channel** -Element, um eigene Kanäle zu definieren.</span><span class="sxs-lookup"><span data-stu-id="a8cc1-108">To define your own channels, use the **channel** element.</span></span> <span data-ttu-id="a8cc1-109">Verwenden Sie das **importchannel** -Element, um einen importierten Kanal zu definieren.</span><span class="sxs-lookup"><span data-stu-id="a8cc1-109">To define an imported channel, use the **importChannel** element.</span></span> <span data-ttu-id="a8cc1-110">Sie können bis zu acht Kanäle in einer beliebigen Kombination aus importierten Kanälen oder Kanälen angeben, die Sie definieren.</span><span class="sxs-lookup"><span data-stu-id="a8cc1-110">You can specify up to eight channels in any combination of imported channels or channels that you define.</span></span>

<span data-ttu-id="a8cc1-111">Der Kanal muss einen von vier Typen aufweisen: "admin", "Operational", "Analytic" und "Debug".</span><span class="sxs-lookup"><span data-stu-id="a8cc1-111">The channel must be of one of four types: Admin, Operational, Analytic, and Debug.</span></span> <span data-ttu-id="a8cc1-112">Jeder Kanaltyp verfügt über eine beabsichtigte Zielgruppe, die den Typ der Ereignisse bestimmt, die Sie in den Kanal schreiben.</span><span class="sxs-lookup"><span data-stu-id="a8cc1-112">Each channel type has an intended audience, which determines the type of events that you write to the channel.</span></span> <span data-ttu-id="a8cc1-113">Eine Beschreibung der einzelnen Typen finden Sie unter der komplexe [**channelType**](eventmanifestschema-channeltype-complextype.md) -Typ.</span><span class="sxs-lookup"><span data-stu-id="a8cc1-113">For a description of each type, see the [**ChannelType**](eventmanifestschema-channeltype-complextype.md) complex type.</span></span>

<span data-ttu-id="a8cc1-114">Legen Sie zum Angeben des Kanals, auf den ein Ereignis geschrieben wird, das **Channel** -Attribut der Ereignis Definition auf denselben Wert wie das **Chid** -Attribut der Channeldefinition fest.</span><span class="sxs-lookup"><span data-stu-id="a8cc1-114">To specify the channel to which an event is written, set the event definition's **channel** attribute to the same value as the channel definition's **chid** attribute.</span></span> <span data-ttu-id="a8cc1-115">Ereignisse können jeweils nur in einen Kanal geschrieben werden, können jedoch auch von bis zu 7 anderen ETW-Sitzungen gleichzeitig gesammelt werden.</span><span class="sxs-lookup"><span data-stu-id="a8cc1-115">Events can only be written to one channel at a time, but can also be collected by up to 7 other ETW sessions at the same time.</span></span>

<span data-ttu-id="a8cc1-116">Im folgenden Beispiel wird gezeigt, wie ein Kanal importiert wird.</span><span class="sxs-lookup"><span data-stu-id="a8cc1-116">The following example shows how to import a channel.</span></span> <span data-ttu-id="a8cc1-117">Sie müssen die Attribute " **Chid** " und " **Name** " festlegen.</span><span class="sxs-lookup"><span data-stu-id="a8cc1-117">You must set the **chid** and **name** attributes.</span></span> <span data-ttu-id="a8cc1-118">Das **Chid** -Attribut identifiziert den Channel eindeutig – jeder Kanal Bezeichner in der Liste der Channels muss eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="a8cc1-118">The **chid** attribute uniquely identifies the channel—each channel identifier in your list of channels must be unique.</span></span> <span data-ttu-id="a8cc1-119">Legen Sie das **Name** -Attribut auf den Namen fest, der vom Anbieter beim Definieren des Kanals verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="a8cc1-119">Set the **name** attribute to the same name that the provider used when it defined the channel.</span></span>


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

                <channels>
                    <channel chid="c1"
                             name="Microsoft-Windows-BaseProvider/Admin"
                             symbol="CHANNEL_BASEPROVIDER_ADMIN"
                             type="Admin"/>
                </channels>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Microsoft-Windows-SampleProvider"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```

<span data-ttu-id="a8cc1-120">Obwohl Winmeta.xml Legacy Kanäle definiert, die importiert werden können, sollten Sie Sie nicht verwenden, es sei denn, Sie unterstützen Legacy-Consumer, die Ereignisse aus den Legacy Kanälen (z. b. Anwendung oder System) nutzen.</span><span class="sxs-lookup"><span data-stu-id="a8cc1-120">Although Winmeta.xml defines legacy channels that you can import, you should not use them unless you are supporting legacy consumers that consume events out of the legacy channels (for example, Application or System).</span></span> <span data-ttu-id="a8cc1-121">Die Winmeta.xml-Datei ist im Windows SDK enthalten.</span><span class="sxs-lookup"><span data-stu-id="a8cc1-121">The Winmeta.xml file is included in the Windows SDK.</span></span>

<span data-ttu-id="a8cc1-122">Im folgenden Beispiel wird gezeigt, wie ein Kanal definiert wird.</span><span class="sxs-lookup"><span data-stu-id="a8cc1-122">The following example shows how to define a channel.</span></span> <span data-ttu-id="a8cc1-123">Sie müssen die Attribute " **Chid**", " **Name**" und " **Type** " festlegen.</span><span class="sxs-lookup"><span data-stu-id="a8cc1-123">You must set the **chid**, **name**, and **type** attributes.</span></span> <span data-ttu-id="a8cc1-124">Das **Chid** -Attribut identifiziert den Channel eindeutig – jeder Kanal Bezeichner in der Liste der Channels muss eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="a8cc1-124">The **chid** attribute uniquely identifies the channel—each channel identifier in your list of channels must be unique.</span></span> <span data-ttu-id="a8cc1-125">Legen Sie das **Chid** -Attribut auf einen Wert fest, der für die Kanäle eindeutig ist, die Ihr Anbieter auflistet. auf den Kanal Bezeichner wird in einer oder mehreren Ereignis Definitionen verwiesen.</span><span class="sxs-lookup"><span data-stu-id="a8cc1-125">Set the **chid** attribute to a value that is unique for the channels that your provider lists; the channel identifier is referenced in one or more of your event definitions.</span></span> <span data-ttu-id="a8cc1-126">Die Konvention für die Benennung des Kanals besteht darin, den Anbieter Namen und den Kanaltyp in der Form *Provider Name* / *channelType* zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a8cc1-126">The convention for naming the channel is to use the provider name and channel type in the form, *providername*/*channeltype*.</span></span>

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

                <channels>
                    <importChannel chid="c1"
                                   name="Microsoft-Windows-BaseProvider/Admin"
                                   symbol="CHANNEL_BASEPROVIDER_ADMIN"
                                   />

                    <channel chid="c2"
                             name="Microsoft-Windows-SampleProvider/Operational"
                             type="Operational"
                             enabled="true"
                             />
                </channels>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Microsoft-Windows-SampleProvider"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```
