---
title: Komplexer baseeapmethodconfig-Typ
description: Erfahren Sie mehr über den komplexen Basistyp baseeapmethodconfig. Dieser Typ ist ein Platzhalter Element für die Methoden Konfiguration.
ms.assetid: 9aafd6ad-2342-4882-99d3-2f2e6c3d67b5
keywords:
- Komplexer baseeapmethodconfig-Typ EAPHost
topic_type:
- apiref
api_name:
- BaseEapMethodConfig
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ac7d628b554696fffd254a45b9b1021d68e2a55e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391032"
---
# <a name="baseeapmethodconfig-complex-type"></a><span data-ttu-id="f675e-105">Komplexer baseeapmethodconfig-Typ</span><span class="sxs-lookup"><span data-stu-id="f675e-105">BaseEapMethodConfig Complex Type</span></span>

<span data-ttu-id="f675e-106">Der komplexe **Basistyp baseeapmethodconfig** ist ein Platzhalter Element für die Methoden Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="f675e-106">The **BaseEapMethodConfig** complex type is a placeholder element for the method configuration.</span></span>

``` syntax
<xs:complexType name="BaseEapMethodConfig">
    <xs:sequence>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##any"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="remarks"></a><span data-ttu-id="f675e-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f675e-107">Remarks</span></span>

<span data-ttu-id="f675e-108">Die EAP-Methode führt eine Schema Validierung für den Inhalt des **baseeapmethodconfig** -Elements aus.</span><span class="sxs-lookup"><span data-stu-id="f675e-108">The EAP method performs schema validation on the contents of the **BaseEapMethodConfig** element.</span></span>

## <a name="requirements"></a><span data-ttu-id="f675e-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f675e-109">Requirements</span></span>



| <span data-ttu-id="f675e-110">Role</span><span class="sxs-lookup"><span data-stu-id="f675e-110">Role</span></span> | <span data-ttu-id="f675e-111">Mindestens unterstützte Betriebssystemversion</span><span class="sxs-lookup"><span data-stu-id="f675e-111">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="f675e-112">Client</span><span class="sxs-lookup"><span data-stu-id="f675e-112">Client</span></span><br/> | <span data-ttu-id="f675e-113">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f675e-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f675e-114">Server</span><span class="sxs-lookup"><span data-stu-id="f675e-114">Server</span></span><br/> | <span data-ttu-id="f675e-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f675e-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f675e-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f675e-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f675e-117">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="f675e-117">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="f675e-118">baseeapmethodconfig-Schema</span><span class="sxs-lookup"><span data-stu-id="f675e-118">baseeapmethodconfig Schema</span></span>](baseeapmethodconfigschema-schema.md)
</dt> </dl>

 

 





