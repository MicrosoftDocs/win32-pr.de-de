---
title: Komplexer importchanneltype-Typ
description: Identifiziert einen Kanal, der von einem anderen Anbieter oder einem Manifest definiert wurde, das einen Metadatenabschnitt enthält.
ms.assetid: da14d837-0ed8-4d85-9820-46c77753768d
keywords:
- Importchanneltype Complex-Typ EventLog
topic_type:
- apiref
api_name:
- ImportChannelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7500d52179c3282c7f15dcdd5dd5a32620bbc076
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103587"
---
# <a name="importchanneltype-complex-type"></a><span data-ttu-id="d658d-104">Komplexer importchanneltype-Typ</span><span class="sxs-lookup"><span data-stu-id="d658d-104">ImportChannelType Complex Type</span></span>

<span data-ttu-id="d658d-105">Identifiziert einen Kanal, der von einem anderen Anbieter oder einem Manifest definiert wurde, das einen Metadatenabschnitt enthält.</span><span class="sxs-lookup"><span data-stu-id="d658d-105">Identifies a channel that has been defined by another provider or in a manifest that contains a metadata section.</span></span>

``` syntax
<xs:complexType name="ImportChannelType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="chid"
                type="token"
                use="optional"
             />
            <xs:attribute name="name"
                type="anyURI"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="d658d-106">Attributes</span><span class="sxs-lookup"><span data-stu-id="d658d-106">Attributes</span></span>



| <span data-ttu-id="d658d-107">Name</span><span class="sxs-lookup"><span data-stu-id="d658d-107">Name</span></span>   | <span data-ttu-id="d658d-108">type</span><span class="sxs-lookup"><span data-stu-id="d658d-108">Type</span></span>                                                              | <span data-ttu-id="d658d-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d658d-109">Description</span></span>                                                                                                                                                                                                                                                                                                            |
|--------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d658d-110">Chid</span><span class="sxs-lookup"><span data-stu-id="d658d-110">chid</span></span>   | <span data-ttu-id="d658d-111">token</span><span class="sxs-lookup"><span data-stu-id="d658d-111">token</span></span>                                                             | <span data-ttu-id="d658d-112">Ein Bezeichner, der den Kanal in der Liste der vom Anbieter definierten oder importierten Kanäle eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d658d-112">An identifier that uniquely identifies the channel in the list of channels that the provider defines or imports.</span></span> <span data-ttu-id="d658d-113">Verwenden Sie diesen Wert, wenn Sie in einer Ereignis Definition auf diesen Kanal verweisen.</span><span class="sxs-lookup"><span data-stu-id="d658d-113">Use this value when referencing this channel in an event definition.</span></span> <span data-ttu-id="d658d-114">Wenn Sie keinen channelbezeichner angeben, verwenden Sie den Namen des Kanals, um auf diesen Kanal in einer Ereignis Definition zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="d658d-114">If you do not specify a channel identifier, use the channel's name to reference this channel in an event definition.</span></span><br/>  |
| <span data-ttu-id="d658d-115">name</span><span class="sxs-lookup"><span data-stu-id="d658d-115">name</span></span>   | <span data-ttu-id="d658d-116">anyURI</span><span class="sxs-lookup"><span data-stu-id="d658d-116">anyURI</span></span>                                                            | <span data-ttu-id="d658d-117">Der Name des zu importierenden Kanals.</span><span class="sxs-lookup"><span data-stu-id="d658d-117">The name of the channel to import.</span></span><br/>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="d658d-118">Symbol</span><span class="sxs-lookup"><span data-stu-id="d658d-118">symbol</span></span> | [<span data-ttu-id="d658d-119">**Csymboltype**</span><span class="sxs-lookup"><span data-stu-id="d658d-119">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="d658d-120">Das Symbol, das für den Verweis auf den Kanal in Ihrer Anwendung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d658d-120">The symbol to use to reference the channel in your application.</span></span> <span data-ttu-id="d658d-121">Der [**Nachrichten Compiler (MC.exe)**](message-compiler--mc-exe-.md) verwendet das Symbol, um eine Konstante für den Kanal in der vom Compiler generierten Header Datei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d658d-121">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the channel in the header file that the compiler generates.</span></span> <span data-ttu-id="d658d-122">Wenn Sie kein Symbol angeben, generiert der Compiler einen für Sie.</span><span class="sxs-lookup"><span data-stu-id="d658d-122">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d658d-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d658d-123">Remarks</span></span>

<span data-ttu-id="d658d-124">Das Manifest, das den importierten Kanal definiert hat, muss installiert werden, bevor der Anbieter Ereignisse schreibt. Andernfalls können die Ereignisse nicht in den Kanal geschrieben werden (der Schreibvorgang ist erfolgreich, die Ereignisse werden einfach nicht in den Kanal geschrieben).</span><span class="sxs-lookup"><span data-stu-id="d658d-124">The manifest that defined the imported channel must be installed before your provider writes events; otherwise, the events cannot be written to the channel (the write operation succeeds, the events are simply not written to the channel).</span></span>

## <a name="requirements"></a><span data-ttu-id="d658d-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d658d-125">Requirements</span></span>



| <span data-ttu-id="d658d-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d658d-126">Requirement</span></span> | <span data-ttu-id="d658d-127">Wert</span><span class="sxs-lookup"><span data-stu-id="d658d-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d658d-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d658d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d658d-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d658d-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d658d-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d658d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d658d-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d658d-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





