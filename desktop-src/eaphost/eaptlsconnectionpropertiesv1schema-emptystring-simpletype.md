---
title: einfacher emptystring-Typ
description: Erfahren Sie mehr über den einfachen emptystring-Typ, der nicht verwendet wird. Informationen finden Sie unter Anforderungen und Anzeigen zusätzlicher verfügbarer Ressourcen.
ms.assetid: e561b8d5-8683-41a1-bd72-73b1a767b6cf
keywords:
- emptystring Simple Type EAPHost
topic_type:
- apiref
api_name:
- emptyString
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 756c8976c8b989cf77be921491770fcff9ea62d5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039629"
---
# <a name="emptystring-simple-type"></a><span data-ttu-id="feec6-105">einfacher emptystring-Typ</span><span class="sxs-lookup"><span data-stu-id="feec6-105">emptyString Simple Type</span></span>

<span data-ttu-id="feec6-106">Der einfache **emptystring** -Typ wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="feec6-106">The **emptyString** simple type is not in use.</span></span>

``` syntax
<xs:simpleType name="emptyString">
    <xs:restriction
        base="string"
    >
        <xs:maxLength
            value="0"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="feec6-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="feec6-107">Requirements</span></span>



| <span data-ttu-id="feec6-108">Role</span><span class="sxs-lookup"><span data-stu-id="feec6-108">Role</span></span> | <span data-ttu-id="feec6-109">Mindestens unterstützte Betriebssystemversion</span><span class="sxs-lookup"><span data-stu-id="feec6-109">Minimum supported OS version</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="feec6-110">Client</span><span class="sxs-lookup"><span data-stu-id="feec6-110">Client</span></span><br/> | <span data-ttu-id="feec6-111">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="feec6-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="feec6-112">Server</span><span class="sxs-lookup"><span data-stu-id="feec6-112">Server</span></span><br/> | <span data-ttu-id="feec6-113">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="feec6-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="feec6-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="feec6-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="feec6-115">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="feec6-115">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="feec6-116">eaptlsconnectionpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="feec6-116">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="feec6-117">einfache eaptlsconnectionpropertiesv1 Schema Typen</span><span class="sxs-lookup"><span data-stu-id="feec6-117">eaptlsconnectionpropertiesv1 Schema Simple Types</span></span>](eaptlsconnectionpropertiesv1schema-simple-types.md)
</dt> </dl>

 

 





