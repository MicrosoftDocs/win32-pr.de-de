---
title: Komplexer tlsextensionstype-Typ
description: Erfahren Sie mehr über den komplexen tlsextensionstype-Typ. Dieser Typ ermöglicht zukünftige Erweiterungen des Schemas.
ms.assetid: 5e4f8ef8-1adb-4683-8001-ba7d2d392523
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833a93b9ecb0ba32a95e4c85856ac015f5135fb5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730329"
---
# <a name="tlsextensionstype-complex-type"></a><span data-ttu-id="bf379-104">Komplexer tlsextensionstype-Typ</span><span class="sxs-lookup"><span data-stu-id="bf379-104">TLSExtensionsType Complex Type</span></span>

<span data-ttu-id="bf379-105">Der komplexe Typ **tlsextensionstype** ermöglicht zukünftige Erweiterungen des Schemas.</span><span class="sxs-lookup"><span data-stu-id="bf379-105">The **TLSExtensionsType** complex type enables future enhancements to the schema.</span></span>


```XML
<xs:complexType name="TLSExtensionsType">
    <xs:sequence>
        <xs:any processContents="lax" 
            minOccurs="0" 
            maxOccurs="unbounded" 
            namespace="##other"
        />
    <xs:sequence>
</xs:complexType>

```



## <a name="remarks"></a><span data-ttu-id="bf379-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bf379-106">Remarks</span></span>

<span data-ttu-id="bf379-107">Das **tlsextensionstype** -Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="bf379-107">The **TLSExtensionsType** element is optional.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf379-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bf379-108">Related topics</span></span>

<dl> <span data-ttu-id="bf379-109"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="bf379-109"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="bf379-110">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="bf379-110">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="bf379-111">eaptlsconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="bf379-111">eaptlsconnectionpropertiesv2</span></span>](eaptlsconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="bf379-112">komplexe eaptlsconnectionpropertiesv2-Typen</span><span class="sxs-lookup"><span data-stu-id="bf379-112">eaptlsconnectionpropertiesv2 Complex Types</span></span>](eaptlsconnectionpropertiesv2schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="bf379-113">**Tlsextensions (tlsextensionstype)**</span><span class="sxs-lookup"><span data-stu-id="bf379-113">**TLSExtensions (TLSExtensionsType)**</span></span>](eaptlsconnectionpropertiesv2schema-performservervalidation-eaptype-element.md)
</dt> </dl>

 

 




