---
description: Ruft einen booleschen Wert ab, der angibt, ob das keyCertSign-Bit festgelegt ist.
ms.assetid: c0331293-4a65-40f0-a404-87d8546349c2
title: KeyUsage. iskeycertsignenabled (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsKeyCertSignEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d475565896910f76211e3843526e9a889586efa0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355253"
---
# <a name="keyusageiskeycertsignenabled-property"></a><span data-ttu-id="0a3ee-103">KeyUsage. iskeycertsignenabled (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0a3ee-103">KeyUsage.IsKeyCertSignEnabled property</span></span>

<span data-ttu-id="0a3ee-104">\[Die **iskeycertsignenabled** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="0a3ee-104">\[The **IsKeyCertSignEnabled** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0a3ee-105">Verwenden Sie stattdessen die [**X509EnhancedKeyUsageExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="0a3ee-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="0a3ee-106">Die **iskeycertsignenabled** -Eigenschaft ruft einen booleschen Wert ab, der angibt, ob das keyCertSign-Bit festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0a3ee-106">The **IsKeyCertSignEnabled** property retrieves a Boolean value that indicates whether the keyCertSign bit is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a3ee-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a3ee-107">Syntax</span></span>


```VB
KeyUsage.IsKeyCertSignEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="0a3ee-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="0a3ee-108">Property value</span></span>

<span data-ttu-id="0a3ee-109">**True** gibt an, dass das keyCertSign-Bit festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="0a3ee-109">If **true**, the keyCertSign bit is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a3ee-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0a3ee-110">Requirements</span></span>



| <span data-ttu-id="0a3ee-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0a3ee-111">Requirement</span></span> | <span data-ttu-id="0a3ee-112">Wert</span><span class="sxs-lookup"><span data-stu-id="0a3ee-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a3ee-113">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="0a3ee-113">Redistributable</span></span><br/> | <span data-ttu-id="0a3ee-114">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="0a3ee-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="0a3ee-115">DLL</span><span class="sxs-lookup"><span data-stu-id="0a3ee-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="0a3ee-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a3ee-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a3ee-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0a3ee-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a3ee-118">**Endeinheits Zertifikaten der**</span><span class="sxs-lookup"><span data-stu-id="0a3ee-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
