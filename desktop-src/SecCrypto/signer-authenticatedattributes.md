---
description: Ruft die Auflistung der authentifizierten Attribute ab.
ms.assetid: d4b3efab-d71e-4fef-9691-0c0bbcb27281
title: Signer. authenticatedattributes-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.AuthenticatedAttributes
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3963ec60d699300c4cde368d4d78c39c0873edd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354042"
---
# <a name="signerauthenticatedattributes-property"></a><span data-ttu-id="39058-103">Signer. authenticatedattributes-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="39058-103">Signer.AuthenticatedAttributes property</span></span>

<span data-ttu-id="39058-104">\[Die **authenticatedattributes** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="39058-104">\[The **AuthenticatedAttributes** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="39058-105">Verwenden Sie stattdessen die [**CmsSigner-Klasse**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="39058-105">Instead, use the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="39058-106">Die **authenticatedattributes** -Eigenschaft ruft die Auflistung der authentifizierten Attribute ab.</span><span class="sxs-lookup"><span data-stu-id="39058-106">The **AuthenticatedAttributes** property retrieves the collection of authenticated attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="39058-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="39058-107">Syntax</span></span>


```VB
Signer.AuthenticatedAttributes As Attributes
```



## <a name="property-value"></a><span data-ttu-id="39058-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="39058-108">Property value</span></span>

<span data-ttu-id="39058-109">Eine [**Attribut**](attributes.md) Auflistung, die die authentifizierten Attribute des Signatur Gebers darstellt.</span><span class="sxs-lookup"><span data-stu-id="39058-109">An [**Attributes**](attributes.md) collection that represents the signer's authenticated attributes.</span></span>

## <a name="requirements"></a><span data-ttu-id="39058-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39058-110">Requirements</span></span>



| <span data-ttu-id="39058-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39058-111">Requirement</span></span> | <span data-ttu-id="39058-112">Wert</span><span class="sxs-lookup"><span data-stu-id="39058-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="39058-113">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="39058-113">Redistributable</span></span><br/> | <span data-ttu-id="39058-114">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="39058-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="39058-115">DLL</span><span class="sxs-lookup"><span data-stu-id="39058-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="39058-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39058-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39058-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39058-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39058-118">**Signatur Geber**</span><span class="sxs-lookup"><span data-stu-id="39058-118">**Signer**</span></span>](signer.md)
</dt> </dl>

 

 
