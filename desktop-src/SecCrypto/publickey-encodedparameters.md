---
description: Ruft die Parameter des Algorithmus des öffentlichen Schlüssels ab.
ms.assetid: 1d12f72e-0144-4b7b-b468-d2f35bf253d3
title: PublicKey. EncodedParameters (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey.EncodedParameters
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 316e9737633bccea46cb644da24e4cc98fd118bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366741"
---
# <a name="publickeyencodedparameters-property"></a><span data-ttu-id="fd9b2-103">PublicKey. EncodedParameters (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="fd9b2-103">PublicKey.EncodedParameters property</span></span>

<span data-ttu-id="fd9b2-104">\[Die **EncodedParameters** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="fd9b2-104">\[The **EncodedParameters** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fd9b2-105">Verwenden Sie stattdessen die [**X509Certificate2. PublicKey-Eigenschaft**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="fd9b2-105">Instead, use the [**X509Certificate2.PublicKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="fd9b2-106">Die **EncodedParameters** -Eigenschaft ruft die Parameter des Algorithmus des öffentlichen Schlüssels ab.</span><span class="sxs-lookup"><span data-stu-id="fd9b2-106">The **EncodedParameters** property retrieves the parameters of the public key algorithm.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd9b2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd9b2-107">Syntax</span></span>


```VB
PublicKey.EncodedParameters As EncodedData
```



## <a name="property-value"></a><span data-ttu-id="fd9b2-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="fd9b2-108">Property value</span></span>

<span data-ttu-id="fd9b2-109">Ein [**encodeddata**](encodeddata.md) -Objekt, das Zugriff auf die Parameter des Algorithmus des öffentlichen Schlüssels bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="fd9b2-109">An [**EncodedData**](encodeddata.md) object that provides access to the parameters of the public key algorithm.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd9b2-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd9b2-110">Requirements</span></span>



| <span data-ttu-id="fd9b2-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fd9b2-111">Requirement</span></span> | <span data-ttu-id="fd9b2-112">Wert</span><span class="sxs-lookup"><span data-stu-id="fd9b2-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd9b2-113">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="fd9b2-113">Redistributable</span></span><br/> | <span data-ttu-id="fd9b2-114">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="fd9b2-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="fd9b2-115">DLL</span><span class="sxs-lookup"><span data-stu-id="fd9b2-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="fd9b2-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd9b2-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd9b2-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd9b2-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd9b2-118">**PublicKey**</span><span class="sxs-lookup"><span data-stu-id="fd9b2-118">**PublicKey**</span></span>](publickey.md)
</dt> </dl>

 

 
