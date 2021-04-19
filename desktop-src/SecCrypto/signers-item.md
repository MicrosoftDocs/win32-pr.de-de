---
description: Ruft das Signatur Geber Objekt ab, das den indizierten Signatur Geber darstellt.
ms.assetid: a95f4e33-ab92-44e1-91ab-2c5335a04f05
title: Signers. Item (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signers.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9b0b4179c1ea7e2ded5d945f64f03124eb864fdc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362169"
---
# <a name="signersitem-property"></a><span data-ttu-id="8971c-103">Signers. Item (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="8971c-103">Signers.Item property</span></span>

<span data-ttu-id="8971c-104">\[Die **Item** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="8971c-104">\[The **Item** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8971c-105">Verwenden Sie stattdessen eine Auflistung von CmsSigner-Objekten.</span><span class="sxs-lookup"><span data-stu-id="8971c-105">Instead, use a collection of CmsSigner objects.</span></span> <span data-ttu-id="8971c-106">Weitere Informationen finden Sie unter der [**CmsSigner-Klasse**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="8971c-106">For more information, see the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="8971c-107">Die **Item** -Eigenschaft ruft das [**Signatur**](signer.md) Geber Objekt ab, das den indizierten Signatur Geber darstellt.</span><span class="sxs-lookup"><span data-stu-id="8971c-107">The **Item** property retrieves the [**Signer**](signer.md) object that represents the indexed signer.</span></span> <span data-ttu-id="8971c-108">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="8971c-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="8971c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="8971c-109">Syntax</span></span>


```VB
Signers.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="8971c-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="8971c-110">Property value</span></span>

<span data-ttu-id="8971c-111">Das [**Signatur**](signer.md) Geber Objekt, das den indizierten Signatur Geber darstellt.</span><span class="sxs-lookup"><span data-stu-id="8971c-111">The [**Signer**](signer.md) object that represents the indexed signer.</span></span>

## <a name="requirements"></a><span data-ttu-id="8971c-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8971c-112">Requirements</span></span>



| <span data-ttu-id="8971c-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8971c-113">Requirement</span></span> | <span data-ttu-id="8971c-114">Wert</span><span class="sxs-lookup"><span data-stu-id="8971c-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8971c-115">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="8971c-115">Redistributable</span></span><br/> | <span data-ttu-id="8971c-116">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="8971c-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="8971c-117">DLL</span><span class="sxs-lookup"><span data-stu-id="8971c-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="8971c-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8971c-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8971c-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8971c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8971c-120">**Signatur Geber**</span><span class="sxs-lookup"><span data-stu-id="8971c-120">**Signers**</span></span>](signers.md)
</dt> </dl>

 

 
