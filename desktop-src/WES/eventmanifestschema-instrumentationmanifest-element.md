---
title: instrumentationmanifest-Element
description: Der Stamm Knoten des Manifests.
ms.assetid: cb7b5201-be11-48f9-bcca-4606904f0c1d
keywords:
- instrumentiermanifest-Element EventLog
topic_type:
- apiref
api_name:
- instrumentationManifest
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c15092d7a7eafd625e9c2026965af053d38fe4b9
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "104219087"
---
# <a name="instrumentationmanifest-element"></a><span data-ttu-id="e6571-104">instrumentationmanifest-Element</span><span class="sxs-lookup"><span data-stu-id="e6571-104">instrumentationManifest Element</span></span>

<span data-ttu-id="e6571-105">Der Stamm Knoten des Manifests.</span><span class="sxs-lookup"><span data-stu-id="e6571-105">The root node of the manifest.</span></span>

``` syntax
<xs:element name="instrumentationManifest">
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="InstrumentationManifestType"
            >
                <xs:choice
                    maxOccurs="3"
                >
                    <xs:choice>
                        <xs:element name="metadata"
                            type="MetadataType"
                         />
                        <xs:element name="instrumentation"
                            type="InstrumentationType"
                         />
                    </xs:choice>
                    <xs:element name="localization"
                        type="LocalizationType"
                     />
                    <xs:any
                        processContents="lax"
                        minOccurs="0"
                        maxOccurs="unbounded"
                        namespace="##other"
                     />
                </xs:choice>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="e6571-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e6571-106">Child elements</span></span>



| <span data-ttu-id="e6571-107">Element</span><span class="sxs-lookup"><span data-stu-id="e6571-107">Element</span></span>                                                                                        | <span data-ttu-id="e6571-108">type</span><span class="sxs-lookup"><span data-stu-id="e6571-108">Type</span></span>                                                                               | <span data-ttu-id="e6571-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e6571-109">Description</span></span>                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e6571-110">**Ener**</span><span class="sxs-lookup"><span data-stu-id="e6571-110">**instrumentation**</span></span>](eventmanifestschema-instrumentation-instrumentationmanifest-element.md) | [<span data-ttu-id="e6571-111">**InstrumentationType**</span><span class="sxs-lookup"><span data-stu-id="e6571-111">**InstrumentationType**</span></span>](eventmanifestschema-instrumentationtype-complextype.md) | <span data-ttu-id="e6571-112">In diesem Abschnitt werden ein oder mehrere Ereignis Anbieter und die Ereignisse definiert, die Sie protokollieren.</span><span class="sxs-lookup"><span data-stu-id="e6571-112">This section defines one or more event providers and the events that they log.</span></span><br/>                                                                                                                                                                                                                     |
| [<span data-ttu-id="e6571-113">**Lokalisierung**</span><span class="sxs-lookup"><span data-stu-id="e6571-113">**localization**</span></span>](eventmanifestschema-localization-instrumentationmanifest-element.md)       | [<span data-ttu-id="e6571-114">**Localizationtype**</span><span class="sxs-lookup"><span data-stu-id="e6571-114">**LocalizationType**</span></span>](eventmanifestschema-localizationtype-complextype.md)       | <span data-ttu-id="e6571-115">In diesem Abschnitt werden die lokalisierten Meldungs Zeichenfolgen definiert, die Consumer zur Anzeige verwenden</span><span class="sxs-lookup"><span data-stu-id="e6571-115">This section defines the localized message strings that consumers use for display.</span></span> <span data-ttu-id="e6571-116">Dieser Abschnitt enthält z. b. die lokalisierte Meldungs Zeichenfolge für den Namen des Anbieters, die von Ihnen definierten Ereignisse und alle von Ihnen definierten Ereignis Attribute, z. b. Kanäle, Tasks und OpCodes.</span><span class="sxs-lookup"><span data-stu-id="e6571-116">For example, this section would contain the localized message string for the name of your provider, the events that you define, and any event attributes that you define, such as channels, tasks, and opcodes.</span></span><br/> |
| [<span data-ttu-id="e6571-117">**benötigten**</span><span class="sxs-lookup"><span data-stu-id="e6571-117">**metadata**</span></span>](eventmanifestschema-metadata-instrumentationmanifest-element.md)               | [<span data-ttu-id="e6571-118">**MetadataType**</span><span class="sxs-lookup"><span data-stu-id="e6571-118">**MetadataType**</span></span>](eventmanifestschema-metadatatype-complextype.md)               | <span data-ttu-id="e6571-119">In diesem Abschnitt werden Metadatentypen definiert, die andere Manifeste verwenden können.</span><span class="sxs-lookup"><span data-stu-id="e6571-119">This section defines metadata types that other manifests can use.</span></span> <span data-ttu-id="e6571-120">Ein Beispiel finden Sie in der Winmeta.xml-Datei, die im \\ Ordner include des Windows SDK enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="e6571-120">For an example, see the Winmeta.xml file included in the \\Include folder of the Windows SDK.</span></span><br/>                                                                                                                                    |



## <a name="remarks"></a><span data-ttu-id="e6571-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e6571-121">Remarks</span></span>

<span data-ttu-id="e6571-122">Das **instrumentationmanifest** -Element muss die folgenden Namespaces enthalten:</span><span class="sxs-lookup"><span data-stu-id="e6571-122">The **instrumentationManifest** element must contain the following namespaces:</span></span>

<dl> <span data-ttu-id="e6571-123">xmlns = " https://schemas.microsoft.com/win/2004/08/events "</span><span class="sxs-lookup"><span data-stu-id="e6571-123">xmlns="https://schemas.microsoft.com/win/2004/08/events"</span></span>  
<span data-ttu-id="e6571-124">xmlns: Win = " https://manifests.microsoft.com/win/2004/08/windows/events "</span><span class="sxs-lookup"><span data-stu-id="e6571-124">xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"</span></span>  
<span data-ttu-id="e6571-125">xmlns: XS = " https://www.w3.org/2001/XMLSchema "</span><span class="sxs-lookup"><span data-stu-id="e6571-125">xmlns:xs="https://www.w3.org/2001/XMLSchema"</span></span>  
</dl>

<span data-ttu-id="e6571-126">Ein Manifest muss einen Instrumentations Abschnitt und einen Lokalisierungs Abschnitt enthalten.</span><span class="sxs-lookup"><span data-stu-id="e6571-126">A manifest must contain an instrumentation section and a localization section.</span></span> <span data-ttu-id="e6571-127">Der Instrumentations Abschnitt und der Metadatenabschnitt schließen sich gegenseitig aus (Sie können nicht beide Elemente im selben Manifest definieren).</span><span class="sxs-lookup"><span data-stu-id="e6571-127">The instrumentation section and metadata section are mutually exclusive (you cannot define both in the same manifest).</span></span> <span data-ttu-id="e6571-128">Obwohl Sie ein Manifest erstellen können, das einen Metadatenabschnitt enthält, wird es vom Dienst nicht verwendet. die einzigen Metadaten, die der Dienst erkennt, sind die Metadaten, die in der Winmeta.xml-Datei gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="e6571-128">Although you can create a manifest that contains a metadata section, the service will not use it; the only metadata that the service recognizes is the metadata found in the Winmeta.xml file.</span></span>

## <a name="examples"></a><span data-ttu-id="e6571-129">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e6571-129">Examples</span></span>

<span data-ttu-id="e6571-130">Das folgende Beispiel zeigt das Gerüst eines vollständig definierten Instrumentierungs Manifests.</span><span class="sxs-lookup"><span data-stu-id="e6571-130">The following example shows the skeleton of a fully defined instrumentation manifest.</span></span>


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="https://www.w3.org/2001/XMLSchema"    
    >

    <instrumentation>
        <events>
            <provider ...>
                <channels>
                    <importChanel .../>
                    <channel .../>
                </channels>
                <levels>
                <level .../>
                </levels>
                <tasks>
                    <task .../>
                </tasks>
                <opcodes>
                    <opcode .../>
                </opcodes>
                <keywords>
                    <keyword .../>
                </keywords>
                <filters>
                    <filter .../>
                </filters>
                <maps>
                    <valueMap ...>
                        <map .../>
                    </valueMap>
                    <bitMap ...>
                        <map .../>
                    </bitMap>
                </maps>
                <namedQueries>
                    <patternMap ...>
                        <map .../>
                    </patternMap>  
                </namedQueries>
                <templates>
                    <template ...>
                        <data .../>
                        <UserData>
                            <!-- valid XML fragment -->
                        </UserData>
                    </template>
                </templates>
                <events>
                    <event .../>
                </events>
            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources ...>
            <stringTable>
                <string .../>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```



## <a name="requirements"></a><span data-ttu-id="e6571-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e6571-131">Requirements</span></span>



| <span data-ttu-id="e6571-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e6571-132">Requirement</span></span> | <span data-ttu-id="e6571-133">Wert</span><span class="sxs-lookup"><span data-stu-id="e6571-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e6571-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e6571-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e6571-135">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6571-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e6571-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e6571-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e6571-137">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6571-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





