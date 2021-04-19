---
description: Ruft den Wert des öffentlichen Schlüssels ab.
ms.assetid: d9846ebe-44df-4ee0-8f15-cc96883d9d53
title: PublicKey. encodecodkey (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey.EncodedKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: de2c7b2bfbbdaf28345ae29e260bfd30c5754ffd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370817"
---
# <a name="publickeyencodedkey-property"></a><span data-ttu-id="bf868-103">PublicKey. encodecodkey (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="bf868-103">PublicKey.EncodedKey property</span></span>

<span data-ttu-id="bf868-104">\[Die **encodedkey** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="bf868-104">\[The **EncodedKey** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="bf868-105">Verwenden Sie stattdessen die [**X509Certificate2. PublicKey-Eigenschaft**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="bf868-105">Instead, use the [**X509Certificate2.PublicKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="bf868-106">Die **encodecodkey** -Eigenschaft ruft den Wert des öffentlichen Schlüssels ab.</span><span class="sxs-lookup"><span data-stu-id="bf868-106">The **EncodedKey** property retrieves the value of the public key.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf868-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf868-107">Syntax</span></span>


```VB
PublicKey.EncodedKey As EncodedData
```



## <a name="property-value"></a><span data-ttu-id="bf868-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="bf868-108">Property value</span></span>

<span data-ttu-id="bf868-109">Ein [**encoddata**](encodeddata.md) -Objekt, das Zugriff auf den Wert des öffentlichen Schlüssels bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="bf868-109">An [**EncodedData**](encodeddata.md) object that provides access to the value of the public key.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf868-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bf868-110">Requirements</span></span>



| <span data-ttu-id="bf868-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bf868-111">Requirement</span></span> | <span data-ttu-id="bf868-112">Wert</span><span class="sxs-lookup"><span data-stu-id="bf868-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf868-113">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="bf868-113">Redistributable</span></span><br/> | <span data-ttu-id="bf868-114">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="bf868-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="bf868-115">DLL</span><span class="sxs-lookup"><span data-stu-id="bf868-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="bf868-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf868-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf868-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bf868-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf868-118">**PublicKey**</span><span class="sxs-lookup"><span data-stu-id="bf868-118">**PublicKey**</span></span>](publickey.md)
</dt> </dl>

 

 
