---
description: Ruft einen Qualifizierer basierend auf einem angegebenen Index ab.
ms.assetid: 4d54358d-99de-4a1c-b843-41006f47a279
title: Qualifizierer. Item-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 798b1f212aabd5b1ab34a1eefb626be4572b9c1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368678"
---
# <a name="qualifiersitem-property"></a><span data-ttu-id="d8bb5-103">Qualifizierer. Item-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d8bb5-103">Qualifiers.Item property</span></span>

<span data-ttu-id="d8bb5-104">\[Die **Item** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="d8bb5-104">\[The **Item** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d8bb5-105">Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace, indem Sie den Konstruktor aufrufen, der eine OID als Parameter annimmt, und dann die OID für Zertifikat Richtlinien verwenden, um Qualifizierer zu verarbeiten, die Teil der Richtlinien Informationen in der Zertifikat Richtlinien Erweiterung sind.\]</span><span class="sxs-lookup"><span data-stu-id="d8bb5-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="d8bb5-106">Die **Item** -Eigenschaft ruft einen Qualifizierer basierend auf einem angegebenen Index ab.</span><span class="sxs-lookup"><span data-stu-id="d8bb5-106">The **Item** property retrieves a qualifier based on a specified index.</span></span> <span data-ttu-id="d8bb5-107">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="d8bb5-107">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8bb5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8bb5-108">Syntax</span></span>


```VB
Qualifiers.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="d8bb5-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="d8bb5-109">Property value</span></span>

<span data-ttu-id="d8bb5-110">Ein [**qualifiziererobjekt**](qualifier.md) , das den indizierten Qualifizierer der Auflistung darstellt.</span><span class="sxs-lookup"><span data-stu-id="d8bb5-110">A [**Qualifier**](qualifier.md) object that represents the indexed qualifier of the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8bb5-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d8bb5-111">Requirements</span></span>



| <span data-ttu-id="d8bb5-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d8bb5-112">Requirement</span></span> | <span data-ttu-id="d8bb5-113">Wert</span><span class="sxs-lookup"><span data-stu-id="d8bb5-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8bb5-114">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="d8bb5-114">Redistributable</span></span><br/> | <span data-ttu-id="d8bb5-115">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="d8bb5-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d8bb5-116">DLL</span><span class="sxs-lookup"><span data-stu-id="d8bb5-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="d8bb5-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8bb5-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8bb5-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d8bb5-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8bb5-119">**Qualifikation**</span><span class="sxs-lookup"><span data-stu-id="d8bb5-119">**Qualifiers**</span></span>](qualifiers.md)
</dt> </dl>

 

 
