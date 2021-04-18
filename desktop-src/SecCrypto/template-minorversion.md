---
description: Ruft die neben Versionsnummer der Vorlage ab.
ms.assetid: 3fc51d43-9113-4b4b-88ab-27cf6e5c4fa0
title: Template. MinorVersion (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.MinorVersion
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2a1de0beb41cbe87ca86b443c5cc2145c2058073
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365545"
---
# <a name="templateminorversion-property"></a><span data-ttu-id="dd3e6-103">Template. MinorVersion (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="dd3e6-103">Template.MinorVersion property</span></span>

<span data-ttu-id="dd3e6-104">\[Die **MinorVersion** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="dd3e6-104">\[The **MinorVersion** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="dd3e6-105">Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace, indem Sie den Konstruktor aufrufen, der eine OID als Parameter annimmt, und verwenden Sie dann die OID für die Zertifikat Vorlage, um die Zertifikat Erweiterungs Vorlage abzurufen.\]</span><span class="sxs-lookup"><span data-stu-id="dd3e6-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Template to retrieve the certificate extension template.\]</span></span>

<span data-ttu-id="dd3e6-106">Die **MinorVersion** -Eigenschaft ruft die neben Versionsnummer der Vorlage ab.</span><span class="sxs-lookup"><span data-stu-id="dd3e6-106">The **MinorVersion** property retrieves the minor version number of the template.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd3e6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd3e6-107">Syntax</span></span>


```VB
Template.MinorVersion As Long
```



## <a name="property-value"></a><span data-ttu-id="dd3e6-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="dd3e6-108">Property value</span></span>

<span data-ttu-id="dd3e6-109">Die neben Versionsnummer der Vorlage.</span><span class="sxs-lookup"><span data-stu-id="dd3e6-109">The minor version number of the template.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd3e6-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dd3e6-110">Requirements</span></span>



| <span data-ttu-id="dd3e6-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dd3e6-111">Requirement</span></span> | <span data-ttu-id="dd3e6-112">Wert</span><span class="sxs-lookup"><span data-stu-id="dd3e6-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd3e6-113">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="dd3e6-113">Redistributable</span></span><br/> | <span data-ttu-id="dd3e6-114">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="dd3e6-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="dd3e6-115">DLL</span><span class="sxs-lookup"><span data-stu-id="dd3e6-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="dd3e6-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd3e6-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd3e6-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd3e6-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd3e6-118">**Vorlage**</span><span class="sxs-lookup"><span data-stu-id="dd3e6-118">**Template**</span></span>](template.md)
</dt> </dl>

 

 
