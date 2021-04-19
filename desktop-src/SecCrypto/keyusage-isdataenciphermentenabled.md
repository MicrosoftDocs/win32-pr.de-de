---
description: Ruft einen booleschen Wert ab, der angibt, ob das DataEncipherment-Bit festgelegt ist.
ms.assetid: 9b29a76f-1494-4db3-a5d7-69fe631ca1dd
title: KeyUsage. isdataenciphermentaktivierte Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsDataEnciphermentEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0aad6cbcd21830ad127b9537749dfb1c05a4c9ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355255"
---
# <a name="keyusageisdataenciphermentenabled-property"></a><span data-ttu-id="e9597-103">KeyUsage. isdataenciphermentaktivierte Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e9597-103">KeyUsage.IsDataEnciphermentEnabled property</span></span>

<span data-ttu-id="e9597-104">\[Die **isdataenciphermentaktivierte** Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="e9597-104">\[The **IsDataEnciphermentEnabled** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e9597-105">Verwenden Sie stattdessen die [**X509EnhancedKeyUsageExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="e9597-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="e9597-106">Die **isdataenciphermentaktivierte** -Eigenschaft ruft einen booleschen Wert ab, der angibt, ob das DataEncipherment-Bit festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e9597-106">The **IsDataEnciphermentEnabled** property retrieves a Boolean value that indicates whether the dataEncipherment bit is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9597-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9597-107">Syntax</span></span>


```VB
KeyUsage.IsDataEnciphermentEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="e9597-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e9597-108">Property value</span></span>

<span data-ttu-id="e9597-109">**True** gibt an, dass das DataEncipherment-Bit festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="e9597-109">If **true**, the dataEncipherment bit is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9597-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e9597-110">Requirements</span></span>



| <span data-ttu-id="e9597-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e9597-111">Requirement</span></span> | <span data-ttu-id="e9597-112">Wert</span><span class="sxs-lookup"><span data-stu-id="e9597-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9597-113">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="e9597-113">Redistributable</span></span><br/> | <span data-ttu-id="e9597-114">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="e9597-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e9597-115">DLL</span><span class="sxs-lookup"><span data-stu-id="e9597-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="e9597-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9597-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9597-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e9597-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9597-118">**Endeinheits Zertifikaten der**</span><span class="sxs-lookup"><span data-stu-id="e9597-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
