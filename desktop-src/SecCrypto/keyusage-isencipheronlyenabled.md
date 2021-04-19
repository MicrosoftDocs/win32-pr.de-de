---
description: Ruft einen booleschen Wert ab, der angibt, ob das encipheronly-Bit festgelegt ist.
ms.assetid: 60d79ea4-4968-49e0-8d16-873fbcbd951c
title: KeyUsage. isencipheronlyaktivierte Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsEncipherOnlyEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8a473797f989d18e090af33f08274ecede2630b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373562"
---
# <a name="keyusageisencipheronlyenabled-property"></a><span data-ttu-id="08e85-103">KeyUsage. isencipheronlyaktivierte Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="08e85-103">KeyUsage.IsEncipherOnlyEnabled property</span></span>

<span data-ttu-id="08e85-104">\[Die Eigenschaft " **isencipheronlyaktivierte** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="08e85-104">\[The **IsEncipherOnlyEnabled** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="08e85-105">Verwenden Sie stattdessen die [**X509EnhancedKeyUsageExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="08e85-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="08e85-106">Die Eigenschaft " **isencipheronlyaktivierte** " Ruft einen booleschen Wert ab, der angibt, ob das encipheronly-Bit festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="08e85-106">The **IsEncipherOnlyEnabled** property retrieves a Boolean value that indicates whether the encipherOnly bit is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="08e85-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="08e85-107">Syntax</span></span>


```VB
KeyUsage.IsEncipherOnlyEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="08e85-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="08e85-108">Property value</span></span>

<span data-ttu-id="08e85-109">**True** gibt an, dass das encipheronly-Bit festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="08e85-109">If **true**, the encipherOnly bit is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="08e85-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="08e85-110">Requirements</span></span>



| <span data-ttu-id="08e85-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="08e85-111">Requirement</span></span> | <span data-ttu-id="08e85-112">Wert</span><span class="sxs-lookup"><span data-stu-id="08e85-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="08e85-113">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="08e85-113">Redistributable</span></span><br/> | <span data-ttu-id="08e85-114">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="08e85-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="08e85-115">DLL</span><span class="sxs-lookup"><span data-stu-id="08e85-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="08e85-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08e85-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08e85-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08e85-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08e85-118">**Endeinheits Zertifikaten der**</span><span class="sxs-lookup"><span data-stu-id="08e85-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
