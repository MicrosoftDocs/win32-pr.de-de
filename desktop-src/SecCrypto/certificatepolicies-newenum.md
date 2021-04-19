---
description: Die \_ Eigenschaft "netwenum" von "certificatepolicies" Ruft eine IEnumVARIANT-Schnittstelle für ein Objekt ab, das zum Auflisten der Auflistung verwendet werden kann.
ms.assetid: 631a11c8-4442-493e-9406-bc63f79db548
title: CertificatePolicies._NewEnum-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2d5e90d4b906661119936ca1e893e3b6e17c9bf5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361999"
---
# <a name="certificatepolicies_newenum-property"></a><span data-ttu-id="116b3-103">Certificatepolicies. \_ Eigenschaft "netwenum"</span><span class="sxs-lookup"><span data-stu-id="116b3-103">CertificatePolicies.\_NewEnum property</span></span>

<span data-ttu-id="116b3-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="116b3-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="116b3-105">Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace, indem Sie den Konstruktor aufrufen, der eine OID als Parameter annimmt, und dann die OID für Zertifikat Richtlinien verwenden, um die Zertifikat Richtlinien abzurufen.\]</span><span class="sxs-lookup"><span data-stu-id="116b3-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to retrieve the certificate policies.\]</span></span>

<span data-ttu-id="116b3-106">Die Eigenschaft " **\_ netwenum** " Ruft eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle für ein Objekt ab, das zum Auflisten der Auflistung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="116b3-106">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="116b3-107">Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="116b3-107">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="116b3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="116b3-108">Syntax</span></span>


```VB
CertificatePolicies._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="116b3-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="116b3-109">Property value</span></span>

<span data-ttu-id="116b3-110">Eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle für ein Objekt, das zum Auflisten der Auflistung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="116b3-110">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="116b3-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="116b3-111">Remarks</span></span>

<span data-ttu-id="116b3-112">Diese Eigenschaft wird automatisch intern verwendet, wenn Sie das- `For Each In` Konstrukt in Visual Basic Scripting Edition (VBScript) verwenden.</span><span class="sxs-lookup"><span data-stu-id="116b3-112">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="116b3-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="116b3-113">Requirements</span></span>



| <span data-ttu-id="116b3-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="116b3-114">Requirement</span></span> | <span data-ttu-id="116b3-115">Wert</span><span class="sxs-lookup"><span data-stu-id="116b3-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="116b3-116">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="116b3-116">End of client support</span></span><br/> | <span data-ttu-id="116b3-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="116b3-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="116b3-118">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="116b3-118">End of server support</span></span><br/> | <span data-ttu-id="116b3-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="116b3-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="116b3-120">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="116b3-120">Redistributable</span></span><br/>       | <span data-ttu-id="116b3-121">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="116b3-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="116b3-122">DLL</span><span class="sxs-lookup"><span data-stu-id="116b3-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="116b3-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="116b3-123"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
