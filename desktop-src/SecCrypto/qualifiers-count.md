---
description: Ruft die Anzahl der qualifiziererobjekte in der Auflistung ab.
ms.assetid: 9dafb83a-ff7f-4317-8ed4-2a46dcebf409
title: Qualifizierer. Count-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2ffb79941a78602bfda8f5287b0f4df7205d4d86
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354813"
---
# <a name="qualifierscount-property"></a><span data-ttu-id="54516-103">Qualifizierer. Count-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="54516-103">Qualifiers.Count property</span></span>

<span data-ttu-id="54516-104">\[Die **count** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="54516-104">\[The **Count** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="54516-105">Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace, indem Sie den Konstruktor aufrufen, der eine OID als Parameter annimmt, und dann die OID für Zertifikat Richtlinien verwenden, um Qualifizierer zu verarbeiten, die Teil der Richtlinien Informationen in der Zertifikat Richtlinien Erweiterung sind.\]</span><span class="sxs-lookup"><span data-stu-id="54516-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="54516-106">Die **count** -Eigenschaft ruft die Anzahl der [**qualifiziererobjekte**](qualifier.md) in der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="54516-106">The **Count** property retrieves the number of [**Qualifier**](qualifier.md) objects in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="54516-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="54516-107">Syntax</span></span>


```VB
Qualifiers.Count As Long
```



## <a name="property-value"></a><span data-ttu-id="54516-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="54516-108">Property value</span></span>

<span data-ttu-id="54516-109">Anzahl der [**qualifiziererobjekte**](qualifier.md) in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="54516-109">Number of [**Qualifier**](qualifier.md) objects in the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="54516-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54516-110">Requirements</span></span>



| <span data-ttu-id="54516-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54516-111">Requirement</span></span> | <span data-ttu-id="54516-112">Wert</span><span class="sxs-lookup"><span data-stu-id="54516-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="54516-113">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="54516-113">Redistributable</span></span><br/> | <span data-ttu-id="54516-114">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="54516-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="54516-115">DLL</span><span class="sxs-lookup"><span data-stu-id="54516-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="54516-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54516-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54516-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54516-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54516-118">**Qualifikation**</span><span class="sxs-lookup"><span data-stu-id="54516-118">**Qualifiers**</span></span>](qualifiers.md)
</dt> </dl>

 

 
