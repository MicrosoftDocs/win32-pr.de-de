---
description: Ruft einen booleschen Wert ab, der angibt, ob das decodische Bit festgelegt ist.
ms.assetid: 69d8649d-c7bc-438b-afdd-6c9d2627cd72
title: KeyUsage. isdecocipheronlyaktivierte Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsDecipherOnlyEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5ca72348220d6943ad367e88f404e0f3163f4c42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370487"
---
# <a name="keyusageisdecipheronlyenabled-property"></a><span data-ttu-id="e5364-103">KeyUsage. isdecocipheronlyaktivierte Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e5364-103">KeyUsage.IsDecipherOnlyEnabled property</span></span>

<span data-ttu-id="e5364-104">\[Die **isdecipheronlyaktivierte** Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="e5364-104">\[The **IsDecipherOnlyEnabled** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e5364-105">Verwenden Sie stattdessen die [**X509EnhancedKeyUsageExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="e5364-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="e5364-106">Die **isdecocipheronlyaktivierte** -Eigenschaft ruft einen booleschen Wert ab, der angibt, ob das decodische Bit festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e5364-106">The **IsDecipherOnlyEnabled** property retrieves a Boolean value that indicates whether the decipherOnly bit is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5364-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5364-107">Syntax</span></span>


```VB
KeyUsage.IsDecipherOnlyEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="e5364-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e5364-108">Property value</span></span>

<span data-ttu-id="e5364-109">**True** gibt an, dass das "decoheronly"-Bit festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="e5364-109">If **true**, the decipherOnly bit is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5364-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e5364-110">Requirements</span></span>



| <span data-ttu-id="e5364-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e5364-111">Requirement</span></span> | <span data-ttu-id="e5364-112">Wert</span><span class="sxs-lookup"><span data-stu-id="e5364-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5364-113">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="e5364-113">Redistributable</span></span><br/> | <span data-ttu-id="e5364-114">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="e5364-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e5364-115">DLL</span><span class="sxs-lookup"><span data-stu-id="e5364-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="e5364-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5364-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5364-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e5364-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5364-118">**Endeinheits Zertifikaten der**</span><span class="sxs-lookup"><span data-stu-id="e5364-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
