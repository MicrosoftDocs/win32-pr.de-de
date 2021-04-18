---
title: Komplexer userdatatype-Typ
description: Definiert ein XML-Fragment, das das Layout der Ereignisdaten angibt.
ms.assetid: 25147ace-cc36-43cc-ad85-6a1714f43dbe
keywords:
- Ereignisprotokoll des komplexen userdatatype-Typs
topic_type:
- apiref
api_name:
- UserDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 31186fbcc833219b6523f1fdeb986532984eb7b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338322"
---
# <a name="userdatatype-complex-type"></a><span data-ttu-id="30c2b-104">Komplexer userdatatype-Typ</span><span class="sxs-lookup"><span data-stu-id="30c2b-104">UserDataType Complex Type</span></span>

<span data-ttu-id="30c2b-105">Definiert ein XML-Fragment, das das Layout der Ereignisdaten angibt.</span><span class="sxs-lookup"><span data-stu-id="30c2b-105">Defines an XML fragment that specifies the layout of the event data.</span></span>

``` syntax
<xs:complexType name="UserDataType">
    <xs:sequence>
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

## <a name="requirements"></a><span data-ttu-id="30c2b-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30c2b-106">Requirements</span></span>



| <span data-ttu-id="30c2b-107">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30c2b-107">Requirement</span></span> | <span data-ttu-id="30c2b-108">Wert</span><span class="sxs-lookup"><span data-stu-id="30c2b-108">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="30c2b-109">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="30c2b-109">Minimum supported client</span></span><br/> | <span data-ttu-id="30c2b-110">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="30c2b-110">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="30c2b-111">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="30c2b-111">Minimum supported server</span></span><br/> | <span data-ttu-id="30c2b-112">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="30c2b-112">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





