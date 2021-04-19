---
description: Ruft einen booleschen Wert ab, der angibt, ob das nonablehnationaktivierte Bit festgelegt ist.
ms.assetid: d9bcf0fc-8b2d-408c-b587-71903ef5f5f6
title: KeyUsage. isnonablehnationaktivierte Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsNonRepudiationEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 30e0a532cd39f2150591a3eb74ed9bbba83a7080
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373561"
---
# <a name="keyusageisnonrepudiationenabled-property"></a><span data-ttu-id="2766f-103">KeyUsage. isnonablehnationaktivierte Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2766f-103">KeyUsage.IsNonRepudiationEnabled property</span></span>

<span data-ttu-id="2766f-104">\[Die **isnonablehnationaktivierte** Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="2766f-104">\[The **IsNonRepudiationEnabled** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2766f-105">Verwenden Sie stattdessen die [**X509EnhancedKeyUsageExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="2766f-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="2766f-106">Die **isnonablehnen ationaktivierte** Eigenschaft ruft einen booleschen Wert ab, der angibt, ob das nonablehnationaktivierte Bit festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2766f-106">The **IsNonRepudiationEnabled** property retrieves a Boolean value that indicates whether the nonRepudiationEnabled bit is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="2766f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2766f-107">Syntax</span></span>


```VB
KeyUsage.IsNonRepudiationEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="2766f-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="2766f-108">Property value</span></span>

<span data-ttu-id="2766f-109">**True** gibt an, dass das nonablehnationaktivierte Bit festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2766f-109">If **true**, the nonRepudiationEnabled bit is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="2766f-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2766f-110">Requirements</span></span>



| <span data-ttu-id="2766f-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2766f-111">Requirement</span></span> | <span data-ttu-id="2766f-112">Wert</span><span class="sxs-lookup"><span data-stu-id="2766f-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2766f-113">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="2766f-113">Redistributable</span></span><br/> | <span data-ttu-id="2766f-114">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="2766f-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="2766f-115">DLL</span><span class="sxs-lookup"><span data-stu-id="2766f-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="2766f-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2766f-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2766f-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2766f-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2766f-118">**Endeinheits Zertifikaten der**</span><span class="sxs-lookup"><span data-stu-id="2766f-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
