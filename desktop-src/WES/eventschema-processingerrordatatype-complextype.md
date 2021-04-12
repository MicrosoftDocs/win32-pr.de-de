---
title: Komplexer processingerrordatatype-Typ
description: Definiert einen Fehler, der beim Rendern der Ereignisdaten für das Ereignis aufgetreten ist.
ms.assetid: fd1cc78c-1da5-43c5-8c4b-8abe7e1dc1e1
keywords:
- Ereignisprotokoll des komplexen processingerrordatatype-Typs
topic_type:
- apiref
api_name:
- ProcessingErrorDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ffcc9d2beed4050a8eed34925f30e52f67d129b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105177"
---
# <a name="processingerrordatatype-complex-type"></a><span data-ttu-id="a8151-104">Komplexer processingerrordatatype-Typ</span><span class="sxs-lookup"><span data-stu-id="a8151-104">ProcessingErrorDataType Complex Type</span></span>

<span data-ttu-id="a8151-105">Definiert einen Fehler, der beim Rendern der Ereignisdaten für das Ereignis aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="a8151-105">Defines an error that occurred while rendering the event data for the event.</span></span> <span data-ttu-id="a8151-106">Dies kann vorkommen, wenn die Ereignisdaten nicht mit der Definition der Ereignisdaten Vorlage im Manifest identisch sind.</span><span class="sxs-lookup"><span data-stu-id="a8151-106">This can occur if the event data does not match the event data template definition in the manifest.</span></span>

``` syntax
<xs:complexType name="ProcessingErrorDataType">
    <xs:sequence>
        <xs:element name="ErrorCode"
            type="unsignedInt"
         />
        <xs:element name="DataItemName"
            type="string"
         />
        <xs:element name="EventPayload"
            type="hexBinary"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="a8151-107">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a8151-107">Child elements</span></span>



| <span data-ttu-id="a8151-108">Element</span><span class="sxs-lookup"><span data-stu-id="a8151-108">Element</span></span>                                                                          | <span data-ttu-id="a8151-109">type</span><span class="sxs-lookup"><span data-stu-id="a8151-109">Type</span></span>        | <span data-ttu-id="a8151-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a8151-110">Description</span></span>                                                                          |
|----------------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="a8151-111">**DataItemName**</span><span class="sxs-lookup"><span data-stu-id="a8151-111">**DataItemName**</span></span>](eventschema-dataitemname-processingerrordatatype-element.md) | <span data-ttu-id="a8151-112">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a8151-112">string</span></span>      | <span data-ttu-id="a8151-113">Der Name des Ereignisdaten Elements, das den Fehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="a8151-113">The name of the event data item that caused the error.</span></span><br/>                    |
| [<span data-ttu-id="a8151-114">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="a8151-114">**ErrorCode**</span></span>](eventschema-errorcode-processingerrordatatype-element.md)       | <span data-ttu-id="a8151-115">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a8151-115">unsignedInt</span></span> | <span data-ttu-id="a8151-116">Der Fehlercode des Fehlers, der beim Rendern der Ereignisdaten aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="a8151-116">The error code of the error that occurred while rendering the event data.</span></span><br/> |
| [<span data-ttu-id="a8151-117">**EventPayload**</span><span class="sxs-lookup"><span data-stu-id="a8151-117">**EventPayload**</span></span>](eventschema-eventpayload-processingerrordatatype-element.md) | <span data-ttu-id="a8151-118">hexBinary</span><span class="sxs-lookup"><span data-stu-id="a8151-118">hexBinary</span></span>   | <span data-ttu-id="a8151-119">Ein binäres Blob, das die gesamten Ereignisdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="a8151-119">A binary blob that contains the entire event data.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="a8151-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8151-120">Requirements</span></span>



| <span data-ttu-id="a8151-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a8151-121">Requirement</span></span> | <span data-ttu-id="a8151-122">Wert</span><span class="sxs-lookup"><span data-stu-id="a8151-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a8151-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a8151-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a8151-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a8151-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a8151-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a8151-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a8151-126">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a8151-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





