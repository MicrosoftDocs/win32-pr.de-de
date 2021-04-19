---
description: Ruft einen booleschen Wert ab, der angibt, ob die KeyUsage-Erweiterung vorhanden ist.
ms.assetid: d666049a-4b40-42b6-8c2d-c27a1bb4c48a
title: KeyUsage. ispree sent (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f70754c15a248cda69f93fcab2a0052bd8351261
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360253"
---
# <a name="keyusageispresent-property"></a><span data-ttu-id="ad2f0-103">KeyUsage. ispree sent (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ad2f0-103">KeyUsage.IsPresent property</span></span>

<span data-ttu-id="ad2f0-104">\[Die **ispree sent** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="ad2f0-104">\[The **IsPresent** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ad2f0-105">Verwenden Sie stattdessen die [**X509EnhancedKeyUsageExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="ad2f0-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="ad2f0-106">Die **ispree sent** -Eigenschaft ruft einen booleschen Wert ab, der angibt, ob die [**KeyUsage**](keyusage.md) -Erweiterung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ad2f0-106">The **IsPresent** property retrieves a Boolean value that indicates whether the [**KeyUsage**](keyusage.md) extension is present.</span></span>

<span data-ttu-id="ad2f0-107">Diese Eigenschaft ist die Standard Eigenschaft des [**KeyUsage**](keyusage.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="ad2f0-107">This property is the default property of the [**KeyUsage**](keyusage.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad2f0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad2f0-108">Syntax</span></span>


```VB
KeyUsage.IsPresent As Boolean
```



## <a name="property-value"></a><span data-ttu-id="ad2f0-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="ad2f0-109">Property value</span></span>

<span data-ttu-id="ad2f0-110">**True** gibt an, dass die KeyUsage-Erweiterung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ad2f0-110">If **true**, the KeyUsage extension is present.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad2f0-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad2f0-111">Requirements</span></span>



| <span data-ttu-id="ad2f0-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ad2f0-112">Requirement</span></span> | <span data-ttu-id="ad2f0-113">Wert</span><span class="sxs-lookup"><span data-stu-id="ad2f0-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad2f0-114">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="ad2f0-114">Redistributable</span></span><br/> | <span data-ttu-id="ad2f0-115">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="ad2f0-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ad2f0-116">DLL</span><span class="sxs-lookup"><span data-stu-id="ad2f0-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="ad2f0-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad2f0-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad2f0-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad2f0-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad2f0-119">**Endeinheits Zertifikaten der**</span><span class="sxs-lookup"><span data-stu-id="ad2f0-119">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
