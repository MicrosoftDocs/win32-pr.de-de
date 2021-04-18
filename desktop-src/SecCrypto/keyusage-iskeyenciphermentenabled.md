---
description: Ruft einen booleschen Wert ab, der angibt, ob das KeyEncipherment-Bit festgelegt ist.
ms.assetid: 2bdce181-3de7-4dc1-8059-1e1ca96c0d2d
title: KeyUsage. iskeyenciphermentaktivierte Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsKeyEnciphermentEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: db34737954b0627953758ebc1c5bf7a64b45b1b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365151"
---
# <a name="keyusageiskeyenciphermentenabled-property"></a><span data-ttu-id="554ed-103">KeyUsage. iskeyenciphermentaktivierte Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="554ed-103">KeyUsage.IsKeyEnciphermentEnabled property</span></span>

<span data-ttu-id="554ed-104">\[Die **iskeyenciphermentaktivierte** Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="554ed-104">\[The **IsKeyEnciphermentEnabled** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="554ed-105">Verwenden Sie stattdessen die [**X509EnhancedKeyUsageExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="554ed-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="554ed-106">Die **iskeyenciphermentaktivierte** -Eigenschaft ruft einen booleschen Wert ab, der angibt, ob das KeyEncipherment-Bit festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="554ed-106">The **IsKeyEnciphermentEnabled** property retrieves a Boolean value that indicates whether the keyEncipherment bit is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="554ed-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="554ed-107">Syntax</span></span>


```VB
KeyUsage.IsKeyEnciphermentEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="554ed-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="554ed-108">Property value</span></span>

<span data-ttu-id="554ed-109">**True** gibt an, dass das KeyEncipherment-Bit festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="554ed-109">If **true**, the keyEncipherment bit is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="554ed-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="554ed-110">Requirements</span></span>



| <span data-ttu-id="554ed-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="554ed-111">Requirement</span></span> | <span data-ttu-id="554ed-112">Wert</span><span class="sxs-lookup"><span data-stu-id="554ed-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="554ed-113">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="554ed-113">Redistributable</span></span><br/> | <span data-ttu-id="554ed-114">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="554ed-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="554ed-115">DLL</span><span class="sxs-lookup"><span data-stu-id="554ed-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="554ed-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="554ed-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="554ed-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="554ed-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="554ed-118">**Endeinheits Zertifikaten der**</span><span class="sxs-lookup"><span data-stu-id="554ed-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
