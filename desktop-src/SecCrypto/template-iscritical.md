---
description: Ruft einen booleschen Wert ab, der angibt, ob die Vorlagen Erweiterung als kritisch markiert ist.
ms.assetid: 37e2000a-d3c8-46b5-84e5-a3904fdbaeea
title: Template. IsCritical (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 66f9dc90828cd474497478872f154adbd3fcd12a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357689"
---
# <a name="templateiscritical-property"></a><span data-ttu-id="49c8b-103">Template. IsCritical (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="49c8b-103">Template.IsCritical property</span></span>

<span data-ttu-id="49c8b-104">\[Die **IsCritical** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="49c8b-104">\[The **IsCritical** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="49c8b-105">Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace, indem Sie den Konstruktor aufrufen, der eine OID als Parameter annimmt, und verwenden Sie dann die OID für die Zertifikat Vorlage, um die Zertifikat Erweiterungs Vorlage abzurufen.\]</span><span class="sxs-lookup"><span data-stu-id="49c8b-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Template to retrieve the certificate extension template.\]</span></span>

<span data-ttu-id="49c8b-106">Die **IsCritical** -Eigenschaft ruft einen booleschen Wert ab, der angibt, ob die Vorlagen Erweiterung als kritisch markiert ist.</span><span class="sxs-lookup"><span data-stu-id="49c8b-106">The **IsCritical** property retrieves a Boolean value that indicates whether the template extension is marked critical.</span></span>

## <a name="syntax"></a><span data-ttu-id="49c8b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="49c8b-107">Syntax</span></span>


```VB
Template.IsCritical As Boolean
```



## <a name="property-value"></a><span data-ttu-id="49c8b-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="49c8b-108">Property value</span></span>

<span data-ttu-id="49c8b-109">**True** gibt an, dass die Vorlagen Erweiterung als kritisch markiert ist.</span><span class="sxs-lookup"><span data-stu-id="49c8b-109">If **true**, the template extension is marked critical.</span></span>

## <a name="requirements"></a><span data-ttu-id="49c8b-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="49c8b-110">Requirements</span></span>



| <span data-ttu-id="49c8b-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="49c8b-111">Requirement</span></span> | <span data-ttu-id="49c8b-112">Wert</span><span class="sxs-lookup"><span data-stu-id="49c8b-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="49c8b-113">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="49c8b-113">Redistributable</span></span><br/> | <span data-ttu-id="49c8b-114">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="49c8b-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="49c8b-115">DLL</span><span class="sxs-lookup"><span data-stu-id="49c8b-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="49c8b-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49c8b-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49c8b-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="49c8b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49c8b-118">**Vorlage**</span><span class="sxs-lookup"><span data-stu-id="49c8b-118">**Template**</span></span>](template.md)
</dt> </dl>

 

 
