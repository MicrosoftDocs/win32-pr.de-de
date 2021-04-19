---
description: Ruft einen booleschen Wert ab, der angibt, ob das KeyAgreement-Bit festgelegt ist.
ms.assetid: 3dd1f6c7-893d-453e-92dc-ffeffd879519
title: KeyUsage. iskeyagreementaktivierte Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsKeyAgreementEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 74369996d9e525746e315d1dd2934ef854ffd110
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367411"
---
# <a name="keyusageiskeyagreementenabled-property"></a><span data-ttu-id="c791a-103">KeyUsage. iskeyagreementaktivierte Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c791a-103">KeyUsage.IsKeyAgreementEnabled property</span></span>

<span data-ttu-id="c791a-104">\[Die **iskeyagreementaktivierte** Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="c791a-104">\[The **IsKeyAgreementEnabled** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c791a-105">Verwenden Sie stattdessen die [**X509EnhancedKeyUsageExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="c791a-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="c791a-106">Die **iskeyagreementaktivierte** -Eigenschaft ruft einen booleschen Wert ab, der angibt, ob das KeyAgreement-Bit festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c791a-106">The **IsKeyAgreementEnabled** property retrieves a Boolean value that indicates whether the keyAgreement bit is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="c791a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c791a-107">Syntax</span></span>


```VB
KeyUsage.IsKeyAgreementEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="c791a-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c791a-108">Property value</span></span>

<span data-ttu-id="c791a-109">**True** gibt an, dass das KeyAgreement-Bit festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="c791a-109">If **true**, the keyAgreement bit is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="c791a-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c791a-110">Requirements</span></span>



| <span data-ttu-id="c791a-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c791a-111">Requirement</span></span> | <span data-ttu-id="c791a-112">Wert</span><span class="sxs-lookup"><span data-stu-id="c791a-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c791a-113">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="c791a-113">Redistributable</span></span><br/> | <span data-ttu-id="c791a-114">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="c791a-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c791a-115">DLL</span><span class="sxs-lookup"><span data-stu-id="c791a-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="c791a-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c791a-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c791a-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c791a-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c791a-118">**Endeinheits Zertifikaten der**</span><span class="sxs-lookup"><span data-stu-id="c791a-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
