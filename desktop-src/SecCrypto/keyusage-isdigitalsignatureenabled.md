---
description: Ruft einen booleschen Wert ab, der angibt, ob das DigitalSignature-Bit festgelegt ist.
ms.assetid: 561eea86-ff23-4a26-adf2-b43009566eaa
title: KeyUsage. isdigitalsignatureaktivierte Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsDigitalSignatureEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3b323effebe60597e1d6cf66e75d48c39fcdca4f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364026"
---
# <a name="keyusageisdigitalsignatureenabled-property"></a><span data-ttu-id="be521-103">KeyUsage. isdigitalsignatureaktivierte Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="be521-103">KeyUsage.IsDigitalSignatureEnabled property</span></span>

<span data-ttu-id="be521-104">\[Die **isdigitalsignatureaktivierte** Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="be521-104">\[The **IsDigitalSignatureEnabled** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="be521-105">Verwenden Sie stattdessen die [**X509EnhancedKeyUsageExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="be521-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="be521-106">Die **isdigitalsignatureaktivierte** -Eigenschaft ruft einen booleschen Wert ab, der angibt, ob das DigitalSignature-Bit festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="be521-106">The **IsDigitalSignatureEnabled** property retrieves a Boolean value that indicates whether the digitalSignature bit is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="be521-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="be521-107">Syntax</span></span>


```VB
KeyUsage.IsDigitalSignatureEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="be521-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="be521-108">Property value</span></span>

<span data-ttu-id="be521-109">**True** gibt an, dass das DigitalSignature-Bit festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="be521-109">If **true**, the digitalSignature bit is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="be521-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be521-110">Requirements</span></span>



| <span data-ttu-id="be521-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="be521-111">Requirement</span></span> | <span data-ttu-id="be521-112">Wert</span><span class="sxs-lookup"><span data-stu-id="be521-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="be521-113">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="be521-113">Redistributable</span></span><br/> | <span data-ttu-id="be521-114">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="be521-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="be521-115">DLL</span><span class="sxs-lookup"><span data-stu-id="be521-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="be521-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be521-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be521-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be521-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be521-118">**Endeinheits Zertifikaten der**</span><span class="sxs-lookup"><span data-stu-id="be521-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
