---
description: Ruft einen booleschen Wert ab, der angibt, ob das Zertifikat für eine Zertifizierungsstelle (Certification Authority, ca) gilt.
ms.assetid: 3ca43475-fe97-4eb4-875d-dbc15a0b953c
title: Basiceinschränkungs. iscertificateauthority (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints.IsCertificateAuthority
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5d4878a8cb21f89f3abeeb9e4b530948ef12e9aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361409"
---
# <a name="basicconstraintsiscertificateauthority-property"></a><span data-ttu-id="4b84f-103">Basiceinschränkungs. iscertificateauthority (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4b84f-103">BasicConstraints.IsCertificateAuthority property</span></span>

<span data-ttu-id="4b84f-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4b84f-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="4b84f-105">Verwenden Sie stattdessen die [**X509BasicConstraintsExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/previous-versions/windows/) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="4b84f-105">Instead, use the [**X509BasicConstraintsExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="4b84f-106">Die **iscertificateauthority** -Eigenschaft ruft einen booleschen Wert ab, der angibt, ob das Zertifikat für eine Zertifizierungsstelle ( [*Certification Authority*](../secgloss/c-gly.md) , ca) gilt.</span><span class="sxs-lookup"><span data-stu-id="4b84f-106">The **IsCertificateAuthority** property retrieves a Boolean value that indicates whether the certificate is for a [*certification authority*](../secgloss/c-gly.md) (CA).</span></span>

<span data-ttu-id="4b84f-107">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="4b84f-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b84f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b84f-108">Syntax</span></span>


```VB
BasicConstraints.IsCertificateAuthority As Boolean
```



## <a name="property-value"></a><span data-ttu-id="4b84f-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="4b84f-109">Property value</span></span>

<span data-ttu-id="4b84f-110">**True** gibt an, dass das Zertifikat nur von einer Zertifizierungsstelle verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4b84f-110">If **True**, the certificate is to be used only by a CA.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b84f-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4b84f-111">Requirements</span></span>



| <span data-ttu-id="4b84f-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4b84f-112">Requirement</span></span> | <span data-ttu-id="4b84f-113">Wert</span><span class="sxs-lookup"><span data-stu-id="4b84f-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b84f-114">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="4b84f-114">End of client support</span></span><br/> | <span data-ttu-id="4b84f-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4b84f-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4b84f-116">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="4b84f-116">End of server support</span></span><br/> | <span data-ttu-id="4b84f-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4b84f-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4b84f-118">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="4b84f-118">Redistributable</span></span><br/>       | <span data-ttu-id="4b84f-119">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="4b84f-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4b84f-120">DLL</span><span class="sxs-lookup"><span data-stu-id="4b84f-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="4b84f-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b84f-121"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
