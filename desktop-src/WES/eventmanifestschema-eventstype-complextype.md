---
title: Komplexer eventstype-Typ
description: Enthält eine Liste von Anbietern, die im Manifest definiert sind. | Komplexer eventstype-Typ
ms.assetid: 43f9f577-eae0-45c5-aaf0-5a6df28d3b79
keywords:
- Ereignisprotokoll für komplexen eventstype-Typ
topic_type:
- apiref
api_name:
- EventsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 36500aa037c8e33a48b4f9dd6e38e46eaac58da2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106350625"
---
# <a name="eventstype-complex-type"></a><span data-ttu-id="b76d6-105">Komplexer eventstype-Typ</span><span class="sxs-lookup"><span data-stu-id="b76d6-105">EventsType Complex Type</span></span>

<span data-ttu-id="b76d6-106">Enthält eine Liste von Anbietern, die im Manifest definiert sind.</span><span class="sxs-lookup"><span data-stu-id="b76d6-106">Contains a list of providers that are defined in the manifest.</span></span>

``` syntax
<xs:complexType name="EventsType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="provider"
            type="ProviderType"
            maxOccurs="unbounded"
         />
        <xs:element name="messageTable"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="message"
                        minOccurs="0"
                        maxOccurs="unbounded"
                    >
                        <xs:complexType>
                            <xs:attribute name="value"
                                type="UInt32Type"
                                use="required"
                             />
                            <xs:attribute name="mid"
                                type="xs:string"
                                use="optional"
                             />
                            <xs:attribute name="message"
                                type="strTableRef"
                                use="required"
                             />
                            <xs:attribute name="symbol"
                                type="CSymbolType"
                                use="optional"
                             />
                        </xs:complexType>
                    </xs:element>
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:choice>
    <xs:anyAttribute
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="b76d6-107">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b76d6-107">Child elements</span></span>

| <span data-ttu-id="b76d6-108">Element</span><span class="sxs-lookup"><span data-stu-id="b76d6-108">Element</span></span> | <span data-ttu-id="b76d6-109">type</span><span class="sxs-lookup"><span data-stu-id="b76d6-109">Type</span></span> | <span data-ttu-id="b76d6-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b76d6-110">Description</span></span> |
|---------|------|-------------|
| <span data-ttu-id="b76d6-111">message</span><span class="sxs-lookup"><span data-stu-id="b76d6-111">message</span></span> |      | <span data-ttu-id="b76d6-112">Definiert eine Meldungs Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="b76d6-112">Defines a message string.</span></span> |
| <span data-ttu-id="b76d6-113">messagetable</span><span class="sxs-lookup"><span data-stu-id="b76d6-113">messageTable</span></span> | | <span data-ttu-id="b76d6-114">Definiert eine Liste von Meldungs Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="b76d6-114">Defines a list of message strings.</span></span> <span data-ttu-id="b76d6-115">Sie sollten keine Nachrichten Tabelle verwenden, außer in den folgenden Fällen, in denen Sie eine Nachrichten Tabelle definieren müssen, um Nachrichten Zeichenfolgen explizit Ressourcen Nummern zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="b76d6-115">You should not have to use a message table except in the following cases where you must define a message table to explicitly assign resource numbers to message strings.</span></span> <ul><li><span data-ttu-id="b76d6-116">Sie Migrieren von einer nachrichtentexttextdatei (. MC) zu einem Manifest, schreiben aber immer noch Ereignisse in die Anwendungs-und System Kanäle, damit Legacy Consumer die Ereignisse weiterhin nutzen können.</span><span class="sxs-lookup"><span data-stu-id="b76d6-116">You are migrating from a message text (.mc) file to a manifest but are still writing events to the application and system channels, so that legacy consumers to continue consuming the events.</span></span> <span data-ttu-id="b76d6-117">Um dies zu ermöglichen, müssen die Ressourcen Bezeichner für die im Manifest definierten Nachrichten Zeichenfolgen mit den Ereignis bezeichlern identisch sein.</span><span class="sxs-lookup"><span data-stu-id="b76d6-117">To make this work, the resource identifiers for the message strings defined in the manifest must be the same as the event identifiers.</span></span> <span data-ttu-id="b76d6-118">Der Nachrichten Compiler weist den Meldungs Zeichenfolgen jedoch automatisch Ressourcen Bezeichner zu.</span><span class="sxs-lookup"><span data-stu-id="b76d6-118">However, the message compiler automatically assigns resource identifiers to the message strings.</span></span> <span data-ttu-id="b76d6-119">Um den Compiler zu überschreiben, verwenden Sie die Message-Tabelle, und legen Sie das value-Attribut auf den Ereignis Bezeichner und das Message-Attribut fest, um auf eine Zeichenfolge in der Zeichen folgen Tabelle im Lokalisierungs Abschnitt des Manifests zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="b76d6-119">To override the compiler, use the message table and set the value attribute to the event identifier and the message attribute to refer to a string in the string table in the localization section of the manifest.</span></span></li><li><span data-ttu-id="b76d6-120">Wenn Sie mehr als 16 Anbieter identifizieren möchten, müssen Sie die Nachrichten Tabelle einschließen, mit der die-und-Anbieter Ressourcen Werte für die von Ihnen definierten Nachrichten Zeichenfolgen zuweisen müssen.</span><span class="sxs-lookup"><span data-stu-id="b76d6-120">If you want to identify more than 16 providers, you must include the message table that the seventeenth and on providers must use to assign resource values for the message strings that they define.</span></span> <span data-ttu-id="b76d6-121">Wenn der Anbieter auf Meldungs Zeichenfolgen verweist, die von den Anbietern 1 bis 16 definiert wurden, schließen Sie diese Nachrichten Zeichenfolgen nicht in die Nachrichten Tabelle ein</span><span class="sxs-lookup"><span data-stu-id="b76d6-121">If the provider references message strings that providers 1 through 16 defined, you do not include those message strings in the message table.</span></span></li></ul>|
| [<span data-ttu-id="b76d6-122">**ab**</span><span class="sxs-lookup"><span data-stu-id="b76d6-122">**provider**</span></span>](eventmanifestschema-provider-eventstype-element.md) | [<span data-ttu-id="b76d6-123">**ProviderType**</span><span class="sxs-lookup"><span data-stu-id="b76d6-123">**ProviderType**</span></span>](eventmanifestschema-providertype-complextype.md) | <span data-ttu-id="b76d6-124">Eine Liste von Anbietern, die Sie definieren möchten.</span><span class="sxs-lookup"><span data-stu-id="b76d6-124">A list of providers that you want to define.</span></span> |

## <a name="attributes"></a><span data-ttu-id="b76d6-125">Attributes</span><span class="sxs-lookup"><span data-stu-id="b76d6-125">Attributes</span></span>

| <span data-ttu-id="b76d6-126">Name</span><span class="sxs-lookup"><span data-stu-id="b76d6-126">Name</span></span>    | <span data-ttu-id="b76d6-127">type</span><span class="sxs-lookup"><span data-stu-id="b76d6-127">Type</span></span>                                                             | <span data-ttu-id="b76d6-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b76d6-128">Description</span></span>                                                                            |
|---------|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b76d6-129">message</span><span class="sxs-lookup"><span data-stu-id="b76d6-129">message</span></span> | [<span data-ttu-id="b76d6-130">**"Strauch"**</span><span class="sxs-lookup"><span data-stu-id="b76d6-130">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="b76d6-131">Ein Verweis auf die lokalisierte Zeichenfolge in der Zeichen folgen Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b76d6-131">A reference to the localized string in the string table.</span></span>                               |
| <span data-ttu-id="b76d6-132">mId</span><span class="sxs-lookup"><span data-stu-id="b76d6-132">mid</span></span>     | <span data-ttu-id="b76d6-133">xs:string</span><span class="sxs-lookup"><span data-stu-id="b76d6-133">xs:string</span></span>                                                        | <span data-ttu-id="b76d6-134">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b76d6-134">Not used.</span></span>                                                                              |
| <span data-ttu-id="b76d6-135">Symbol</span><span class="sxs-lookup"><span data-stu-id="b76d6-135">symbol</span></span>  | [<span data-ttu-id="b76d6-136">**Csymboltype**</span><span class="sxs-lookup"><span data-stu-id="b76d6-136">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="b76d6-137">Der symbolische Name, den der Nachrichten Compiler für diese Meldungs Zeichenfolge erstellen soll.</span><span class="sxs-lookup"><span data-stu-id="b76d6-137">The symbolic name that you want the message compiler to create for this message string.</span></span>|
| <span data-ttu-id="b76d6-138">value</span><span class="sxs-lookup"><span data-stu-id="b76d6-138">value</span></span>   | [<span data-ttu-id="b76d6-139">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="b76d6-139">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="b76d6-140">Die Zahl, die als Nachrichten-ID für diese Nachricht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b76d6-140">The number to use as the message identifier for this message.</span></span>                          |


## <a name="remarks"></a><span data-ttu-id="b76d6-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b76d6-141">Remarks</span></span>

<span data-ttu-id="b76d6-142">Der praktische Grenzwert für die Anzahl von Anbietern, die Sie in einem Manifest definieren können, sind 16 Anbieter.</span><span class="sxs-lookup"><span data-stu-id="b76d6-142">The practical limit of the number of providers that you can define in a manifest is 16 providers.</span></span> <span data-ttu-id="b76d6-143">Wenn Sie mehr als 16 Anbieter angeben, müssen Sie eine Nachrichten Tabelle zum expliziten Zuweisen von Ressourcen Nummern zu den Nachrichten Zeichenfolgen verwenden, auf die der Anbieter verweist.</span><span class="sxs-lookup"><span data-stu-id="b76d6-143">If you specify more than 16 providers, you must use a message table to explicitly assign resource numbers to the message strings that the provider references.</span></span> <span data-ttu-id="b76d6-144">Weitere Informationen finden Sie im obigen Nachrichten Element.</span><span class="sxs-lookup"><span data-stu-id="b76d6-144">For more details, see the message element above.</span></span>

## <a name="requirements"></a><span data-ttu-id="b76d6-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b76d6-145">Requirements</span></span>

| <span data-ttu-id="b76d6-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b76d6-146">Requirement</span></span> | <span data-ttu-id="b76d6-147">Wert</span><span class="sxs-lookup"><span data-stu-id="b76d6-147">Value</span></span> |
|--------------------------|-------------------------------------------|
| <span data-ttu-id="b76d6-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b76d6-148">Minimum supported client</span></span> | <span data-ttu-id="b76d6-149">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b76d6-149">Windows Vista \[desktop apps only\]</span></span>       |
| <span data-ttu-id="b76d6-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b76d6-150">Minimum supported server</span></span> | <span data-ttu-id="b76d6-151">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b76d6-151">Windows Server 2008 \[desktop apps only\]</span></span> |
