---
description: Ruft den URI ab, der auf eine von der Zertifizierungsstelle (Certification Authority, ca) veröffentlichte Zertifizierungs Praxis Erklärung (Certification Practice Statement, CPS) verweist.
ms.assetid: fd030c1c-137c-4036-bf13-ae989a9703cc
title: Qualifizierer. cpspointer (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.CPSPointer
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: db16e8faa25fc929e884358fcd885943adc17e32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366838"
---
# <a name="qualifiercpspointer-property"></a><span data-ttu-id="e99ef-103">Qualifizierer. cpspointer (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e99ef-103">Qualifier.CPSPointer property</span></span>

<span data-ttu-id="e99ef-104">\[Die Eigenschaft " **cpspointer** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="e99ef-104">\[The **CPSPointer** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e99ef-105">Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace, indem Sie den Konstruktor aufrufen, der eine OID als Parameter annimmt, und dann die OID für Zertifikat Richtlinien verwenden, um Qualifizierer zu verarbeiten, die Teil der Richtlinien Informationen in der Zertifikat Richtlinien Erweiterung sind.\]</span><span class="sxs-lookup"><span data-stu-id="e99ef-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="e99ef-106">Die **cpspointer** -Eigenschaft ruft den URI ab, der auf eine von der Zertifizierungsstelle (Certification Authority, ca) veröffentlichte Zertifizierungs Praxis Erklärung (Certification Practice Statement, CPS) verweist.</span><span class="sxs-lookup"><span data-stu-id="e99ef-106">The **CPSPointer** property retrieves the URI that points to a Certification Practice Statement (CPS) published by the certification authority (CA).</span></span>

## <a name="syntax"></a><span data-ttu-id="e99ef-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e99ef-107">Syntax</span></span>


```VB
Qualifier.CPSPointer As String
```



## <a name="property-value"></a><span data-ttu-id="e99ef-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e99ef-108">Property value</span></span>

<span data-ttu-id="e99ef-109">Der URI, der auf ein von der Zertifizierungsstelle veröffentlichtes CPS zeigt.</span><span class="sxs-lookup"><span data-stu-id="e99ef-109">The URI that points to a CPS published by the CA.</span></span>

## <a name="requirements"></a><span data-ttu-id="e99ef-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e99ef-110">Requirements</span></span>



| <span data-ttu-id="e99ef-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e99ef-111">Requirement</span></span> | <span data-ttu-id="e99ef-112">Wert</span><span class="sxs-lookup"><span data-stu-id="e99ef-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e99ef-113">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="e99ef-113">Redistributable</span></span><br/> | <span data-ttu-id="e99ef-114">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="e99ef-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e99ef-115">DLL</span><span class="sxs-lookup"><span data-stu-id="e99ef-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="e99ef-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e99ef-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e99ef-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e99ef-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e99ef-118">**Qualifizierer**</span><span class="sxs-lookup"><span data-stu-id="e99ef-118">**Qualifier**</span></span>](qualifier.md)
</dt> </dl>

 

 
