---
description: Ruft den Inhalt der Benutzer Benachrichtigung ab.
ms.assetid: dcf73357-253d-4160-be4e-f826296f5eaa
title: Qualifizierer. explittext-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.ExplicitText
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 7d2ba5e6bbf6bb46e28c5dbb6fa9754c72b66dd4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358356"
---
# <a name="qualifierexplicittext-property"></a><span data-ttu-id="7d9d9-103">Qualifizierer. explittext-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7d9d9-103">Qualifier.ExplicitText property</span></span>

<span data-ttu-id="7d9d9-104">\[Die **explittext** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="7d9d9-104">\[The **ExplicitText** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7d9d9-105">Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace, indem Sie den Konstruktor aufrufen, der eine OID als Parameter annimmt, und dann die OID für Zertifikat Richtlinien verwenden, um Qualifizierer zu verarbeiten, die Teil der Richtlinien Informationen in der Zertifikat Richtlinien Erweiterung sind.\]</span><span class="sxs-lookup"><span data-stu-id="7d9d9-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="7d9d9-106">Die **explittext** -Eigenschaft ruft den Inhalt der Benutzer Benachrichtigung ab.</span><span class="sxs-lookup"><span data-stu-id="7d9d9-106">The **ExplicitText** property retrieves the content of the user notice.</span></span> <span data-ttu-id="7d9d9-107">Diese Eigenschaft ist möglicherweise leer.</span><span class="sxs-lookup"><span data-stu-id="7d9d9-107">This property may be empty.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d9d9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d9d9-108">Syntax</span></span>


```VB
Qualifier.ExplicitText As String
```



## <a name="property-value"></a><span data-ttu-id="7d9d9-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="7d9d9-109">Property value</span></span>

<span data-ttu-id="7d9d9-110">Der Inhalt der Benutzer Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="7d9d9-110">The content of the user notice.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d9d9-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7d9d9-111">Requirements</span></span>



| <span data-ttu-id="7d9d9-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7d9d9-112">Requirement</span></span> | <span data-ttu-id="7d9d9-113">Wert</span><span class="sxs-lookup"><span data-stu-id="7d9d9-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d9d9-114">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="7d9d9-114">Redistributable</span></span><br/> | <span data-ttu-id="7d9d9-115">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="7d9d9-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7d9d9-116">DLL</span><span class="sxs-lookup"><span data-stu-id="7d9d9-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="7d9d9-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d9d9-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d9d9-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d9d9-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d9d9-119">**Qualifizierer**</span><span class="sxs-lookup"><span data-stu-id="7d9d9-119">**Qualifier**</span></span>](qualifier.md)
</dt> </dl>

 

 
