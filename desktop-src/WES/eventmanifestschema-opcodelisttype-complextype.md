---
title: Komplexer opcodelisttype-Typ
description: Definiert eine Liste von Opcodes, die verwendet werden, um die Vorgänge einer Komponente der Anwendung zu identifizieren.
ms.assetid: 0cbca036-b32e-4fc4-96ee-1dd5bee019bf
keywords:
- Opcodelisttype komplexer Typ EventLog
topic_type:
- apiref
api_name:
- OpcodeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dce0942ef0268f50b25987a6be0fd4fffeebd614
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476527"
---
# <a name="opcodelisttype-complex-type"></a><span data-ttu-id="060eb-104">Komplexer opcodelisttype-Typ</span><span class="sxs-lookup"><span data-stu-id="060eb-104">OpcodeListType Complex Type</span></span>

<span data-ttu-id="060eb-105">Definiert eine Liste von Opcodes, die verwendet werden, um die Vorgänge einer Komponente der Anwendung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="060eb-105">Defines a list of opcodes that are used to identify the operations of a component of the application.</span></span>

``` syntax
<xs:complexType name="OpcodeListType">
    <xs:sequence>
        <xs:element name="opcode"
            type="OpcodeType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="060eb-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="060eb-106">Child elements</span></span>



| <span data-ttu-id="060eb-107">Element</span><span class="sxs-lookup"><span data-stu-id="060eb-107">Element</span></span>                                                             | <span data-ttu-id="060eb-108">type</span><span class="sxs-lookup"><span data-stu-id="060eb-108">Type</span></span>                                                             | <span data-ttu-id="060eb-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="060eb-109">Description</span></span>                                                            |
|---------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="060eb-110">**OpCode**</span><span class="sxs-lookup"><span data-stu-id="060eb-110">**opcode**</span></span>](eventmanifestschema-opcode-opcodelisttype-element.md) | [<span data-ttu-id="060eb-111">**OpCodeType**</span><span class="sxs-lookup"><span data-stu-id="060eb-111">**OpcodeType**</span></span>](eventmanifestschema-opcodetype-complextype.md) | <span data-ttu-id="060eb-112">Definiert einen Vorgang innerhalb einer Komponente der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="060eb-112">Defines an operation within a component of the application.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="060eb-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="060eb-113">Requirements</span></span>



| <span data-ttu-id="060eb-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="060eb-114">Requirement</span></span> | <span data-ttu-id="060eb-115">Wert</span><span class="sxs-lookup"><span data-stu-id="060eb-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="060eb-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="060eb-116">Minimum supported client</span></span><br/> | <span data-ttu-id="060eb-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="060eb-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="060eb-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="060eb-118">Minimum supported server</span></span><br/> | <span data-ttu-id="060eb-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="060eb-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





