---
description: Ruft einen booleschen Wert ab, der angibt, ob die KeyUsage-Erweiterung als kritisch markiert ist.
ms.assetid: f7d53570-2b89-40a9-ab56-fcae4e4cb70c
title: KeyUsage. IsCritical (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b1829da9c9ddbcf5261f4cc595b72b8596193078
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355858"
---
# <a name="keyusageiscritical-property"></a><span data-ttu-id="8bb83-103">KeyUsage. IsCritical (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="8bb83-103">KeyUsage.IsCritical property</span></span>

<span data-ttu-id="8bb83-104">\[Die **IsCritical** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="8bb83-104">\[The **IsCritical** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8bb83-105">Verwenden Sie stattdessen die [**X509EnhancedKeyUsageExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="8bb83-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="8bb83-106">Die **IsCritical** -Eigenschaft ruft einen booleschen Wert ab, der angibt, ob die KeyUsage-Erweiterung als kritisch markiert ist.</span><span class="sxs-lookup"><span data-stu-id="8bb83-106">The **IsCritical** property retrieves a Boolean value that indicates whether the KeyUsage extension is marked critical.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bb83-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8bb83-107">Syntax</span></span>


```VB
KeyUsage.IsCritical As Boolean
```



## <a name="property-value"></a><span data-ttu-id="8bb83-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="8bb83-108">Property value</span></span>

<span data-ttu-id="8bb83-109">**True** gibt an, dass die KeyUsage-Erweiterung als kritisch markiert ist.</span><span class="sxs-lookup"><span data-stu-id="8bb83-109">If **true**, the KeyUsage extension is marked critical.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bb83-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8bb83-110">Requirements</span></span>



| <span data-ttu-id="8bb83-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8bb83-111">Requirement</span></span> | <span data-ttu-id="8bb83-112">Wert</span><span class="sxs-lookup"><span data-stu-id="8bb83-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8bb83-113">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="8bb83-113">Redistributable</span></span><br/> | <span data-ttu-id="8bb83-114">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="8bb83-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="8bb83-115">DLL</span><span class="sxs-lookup"><span data-stu-id="8bb83-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="8bb83-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8bb83-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bb83-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8bb83-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bb83-118">**Endeinheits Zertifikaten der**</span><span class="sxs-lookup"><span data-stu-id="8bb83-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
