---
description: Ruft die Hauptversionsnummer der Vorlage ab.
ms.assetid: efde3a7c-48e0-4bfe-9118-3098c7ef8771
title: Template. MajorVersion (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.MajorVersion
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a193a36ed7e914d1ed45d26c21008a7e59a5b8a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358663"
---
# <a name="templatemajorversion-property"></a><span data-ttu-id="affb8-103">Template. MajorVersion (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="affb8-103">Template.MajorVersion property</span></span>

<span data-ttu-id="affb8-104">\[Die **MajorVersion** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="affb8-104">\[The **MajorVersion** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="affb8-105">Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace, indem Sie den Konstruktor aufrufen, der eine OID als Parameter annimmt, und verwenden Sie dann die OID für die Zertifikat Vorlage, um die Zertifikat Erweiterungs Vorlage abzurufen.\]</span><span class="sxs-lookup"><span data-stu-id="affb8-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Template to retrieve the certificate extension template.\]</span></span>

<span data-ttu-id="affb8-106">Die **MajorVersion** -Eigenschaft ruft die Hauptversionsnummer der Vorlage ab.</span><span class="sxs-lookup"><span data-stu-id="affb8-106">The **MajorVersion** property retrieves the major version number of the template.</span></span>

## <a name="syntax"></a><span data-ttu-id="affb8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="affb8-107">Syntax</span></span>


```VB
Template.MajorVersion As Long
```



## <a name="property-value"></a><span data-ttu-id="affb8-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="affb8-108">Property value</span></span>

<span data-ttu-id="affb8-109">Die Hauptversionsnummer der Vorlage.</span><span class="sxs-lookup"><span data-stu-id="affb8-109">The major version number of the template.</span></span>

## <a name="requirements"></a><span data-ttu-id="affb8-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="affb8-110">Requirements</span></span>



| <span data-ttu-id="affb8-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="affb8-111">Requirement</span></span> | <span data-ttu-id="affb8-112">Wert</span><span class="sxs-lookup"><span data-stu-id="affb8-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="affb8-113">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="affb8-113">Redistributable</span></span><br/> | <span data-ttu-id="affb8-114">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="affb8-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="affb8-115">DLL</span><span class="sxs-lookup"><span data-stu-id="affb8-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="affb8-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="affb8-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="affb8-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="affb8-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="affb8-118">**Vorlage**</span><span class="sxs-lookup"><span data-stu-id="affb8-118">**Template**</span></span>](template.md)
</dt> </dl>

 

 
