---
description: Ruft ein Objekt aus der Auflistung der Empfänger ab.
ms.assetid: 03600d4a-5fd4-45c7-ae91-efdc26c084ee
title: Empfängers. Item (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2a80b472c8257597356c626a9e88aad97c447f4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370020"
---
# <a name="recipientsitem-property"></a><span data-ttu-id="5d3ff-103">Empfängers. Item (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5d3ff-103">Recipients.Item property</span></span>

<span data-ttu-id="5d3ff-104">\[Die **Item** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="5d3ff-104">\[The **Item** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5d3ff-105">Verwenden Sie stattdessen die [**cmsrecepentcollection-Klasse**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="5d3ff-105">Instead, use the [**CmsRecipientCollection Class**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="5d3ff-106">Die **Item** -Eigenschaft ruft ein Objekt aus der Auflistung der [**Empfänger**](recipients.md) ab.</span><span class="sxs-lookup"><span data-stu-id="5d3ff-106">The **Item** property retrieves an object from the [**Recipients**](recipients.md) collection.</span></span> <span data-ttu-id="5d3ff-107">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="5d3ff-107">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d3ff-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d3ff-108">Syntax</span></span>


```VB
Recipients.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="5d3ff-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="5d3ff-109">Property value</span></span>

<span data-ttu-id="5d3ff-110">Eine Variante, die das indizierte Element in der [**Empfänger**](recipients.md) Auflistung darstellt.</span><span class="sxs-lookup"><span data-stu-id="5d3ff-110">A variant that represents the indexed item in the [**Recipients**](recipients.md) collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d3ff-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d3ff-111">Requirements</span></span>



| <span data-ttu-id="5d3ff-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5d3ff-112">Requirement</span></span> | <span data-ttu-id="5d3ff-113">Wert</span><span class="sxs-lookup"><span data-stu-id="5d3ff-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d3ff-114">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="5d3ff-114">Redistributable</span></span><br/> | <span data-ttu-id="5d3ff-115">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="5d3ff-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="5d3ff-116">DLL</span><span class="sxs-lookup"><span data-stu-id="5d3ff-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="5d3ff-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d3ff-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d3ff-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d3ff-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d3ff-119">**Empfänger**</span><span class="sxs-lookup"><span data-stu-id="5d3ff-119">**Recipients**</span></span>](recipients.md)
</dt> </dl>

 

 
