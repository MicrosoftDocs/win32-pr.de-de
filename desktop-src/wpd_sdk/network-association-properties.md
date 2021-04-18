---
description: Tragbare Windows-Geräte unterstützen die folgenden Netzwerk Zuordnungs Eigenschaften.
ms.assetid: 5e1b3e8d-9620-4b68-b7ef-1642404ed6ed
title: Netzwerk Zuordnungs Eigenschaften (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Network
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 41e40e456d4671d1aa8fb190274afd2f5ace98b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351335"
---
# <a name="network-association-properties"></a><span data-ttu-id="cd63e-103">Netzwerk Zuordnungs Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cd63e-103">Network Association Properties</span></span>

<span data-ttu-id="cd63e-104">Tragbare Windows-Geräte unterstützen die folgenden Netzwerk Zuordnungs Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cd63e-104">Windows Portable Devices supports the following network association properties.</span></span>



| <span data-ttu-id="cd63e-105">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cd63e-105">Property</span></span>                                                  | <span data-ttu-id="cd63e-106">VarType</span><span class="sxs-lookup"><span data-stu-id="cd63e-106">VarType</span></span>                   | <span data-ttu-id="cd63e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cd63e-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd63e-108">**WPD-Netzwerk Zuordnungs \_ \_ \_ Host \_ Netzwerk \_ -Bezeichner**</span><span class="sxs-lookup"><span data-stu-id="cd63e-108">**WPD\_NETWORK\_ASSOCIATION\_HOST\_NETWORK\_IDENTIFIERS**</span></span> | <span data-ttu-id="cd63e-109">**VT \_ Vector \| VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="cd63e-109">**VT\_VECTOR \| VT\_UI1**</span></span> | <span data-ttu-id="cd63e-110">Die Liste der für diese Zuordnung gültigen EUI-64-Host Bezeichner. Dies ist ein Bytearray, das eine ganzzahlige Anzahl von physischen EUI-64-Netzwerkadressen enthält.</span><span class="sxs-lookup"><span data-stu-id="cd63e-110">The list of EUI-64 host identifiers valid for this association.This is an array of bytes that contains an integral number of EUI-64 physical network addresses.</span></span> <span data-ttu-id="cd63e-111">Diese EUI-64-Werte sind die physischen Netzwerkadressen, die auf dem Host zur Netzwerk Zuordnungs Zeit verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="cd63e-111">These EUI-64 values are the physical network addresses available on the host at Network Association time.</span></span> <span data-ttu-id="cd63e-112">Wenn der Host über Mac-48 physische Netzwerkadressen (typisch für IPv4-Netzwerke) verfügt, wird jede Mac-48-Adresse in der EUI-64-Adresse als die zwei Hälften der Mac-48-Adresse als getrennt durch FF-FF codiert.</span><span class="sxs-lookup"><span data-stu-id="cd63e-112">If the host has MAC-48 physical network addresses (typical of IPv4 networks), each MAC-48 address will be encoded in the EUI-64 address as the two halves of the MAC-48 address separated by FF-FF.</span></span><br/> |
| <span data-ttu-id="cd63e-113">**WPD- \_ Netzwerk Zuordnung \_ \_ X509V3SEQUENCE**</span><span class="sxs-lookup"><span data-stu-id="cd63e-113">**WPD\_NETWORK\_ASSOCIATION\_X509V3SEQUENCE**</span></span>             | <span data-ttu-id="cd63e-114">**VT \_ Vector \| VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="cd63e-114">**VT\_VECTOR \| VT\_UI1**</span></span> | <span data-ttu-id="cd63e-115">Die Sequenz der X. 509 v3-Zertifikate, die für die TLS-Server Authentifizierung bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cd63e-115">The sequence of X.509 v3 certificates to be provided for TLS server authentication.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="cd63e-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cd63e-116">Requirements</span></span>



| <span data-ttu-id="cd63e-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cd63e-117">Requirement</span></span> | <span data-ttu-id="cd63e-118">Wert</span><span class="sxs-lookup"><span data-stu-id="cd63e-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd63e-119">Header</span><span class="sxs-lookup"><span data-stu-id="cd63e-119">Header</span></span><br/> | <dl> <span data-ttu-id="cd63e-120"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd63e-120"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd63e-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd63e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd63e-122">**WPD-Eigenschaften und-Attribute**</span><span class="sxs-lookup"><span data-stu-id="cd63e-122">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




