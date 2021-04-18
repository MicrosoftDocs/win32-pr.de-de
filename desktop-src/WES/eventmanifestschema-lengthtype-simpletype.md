---
title: Einfacher Typ des Längen Typs
description: Definiert einen length-Typ, der verwendet wird, um die Anzahl von Bytes oder Zeichen in einem Datenelement variabler Länge anzugeben, z. b. Binärdaten oder eine ANSI-oder Unicode-Zeichenfolge.
ms.assetid: a15e4241-cce3-4f62-bc1c-f70fb1ea5d38
keywords:
- Simple Type-Ereignistyp EventLog
topic_type:
- apiref
api_name:
- LengthType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dbb0720c2e26fa73056ccffdd17392e93e491c11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341207"
---
# <a name="lengthtype-simple-type"></a><span data-ttu-id="aa55f-104">Einfacher Typ des Längen Typs</span><span class="sxs-lookup"><span data-stu-id="aa55f-104">LengthType Simple Type</span></span>

<span data-ttu-id="aa55f-105">Definiert einen length-Typ, der verwendet wird, um die Anzahl von Bytes oder Zeichen in einem Datenelement variabler Länge anzugeben, z. b. Binärdaten oder eine ANSI-oder Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="aa55f-105">Defines a length type that is used to specify the number of bytes or characters in a variable length data item such as binary data or an ANSI or Unicode string.</span></span> <span data-ttu-id="aa55f-106">Der Wert kann als xs: unsignedshort-Wert oder als Zeichenfolge angegeben werden, die auf den Namen des Datenelement Knotens verweist, der den Ganzzahl ohne Vorzeichen Short-Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="aa55f-106">The value can be specified as an xs:unsignedShort value or as a string that references the name of data item node that contains the unsigned short value.</span></span>

``` syntax
<xs:simpleType name="LengthType">
    <xs:union
        memberValues="unsignedShort string"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="aa55f-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aa55f-107">Requirements</span></span>



| <span data-ttu-id="aa55f-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aa55f-108">Requirement</span></span> | <span data-ttu-id="aa55f-109">Wert</span><span class="sxs-lookup"><span data-stu-id="aa55f-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="aa55f-110">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aa55f-110">Minimum supported client</span></span><br/> | <span data-ttu-id="aa55f-111">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aa55f-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="aa55f-112">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aa55f-112">Minimum supported server</span></span><br/> | <span data-ttu-id="aa55f-113">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aa55f-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





