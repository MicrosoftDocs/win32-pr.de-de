---
description: Ruft den Namen der Vorlage ab.
ms.assetid: f92346bc-89b6-4063-aa66-85e2fb88d67d
title: Template.Name-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 005a9cc961b1d7be0ebda0b8e76307b95d92a6d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369169"
---
# <a name="templatename-property"></a><span data-ttu-id="3ace7-103">Template.Name-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ace7-103">Template.Name property</span></span>

<span data-ttu-id="3ace7-104">\[Die **Name** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="3ace7-104">\[The **Name** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3ace7-105">Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace, indem Sie den Konstruktor aufrufen, der eine OID als Parameter annimmt, und verwenden Sie dann die OID für die Zertifikat Vorlage, um die Zertifikat Erweiterungs Vorlage abzurufen.\]</span><span class="sxs-lookup"><span data-stu-id="3ace7-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Template to retrieve the certificate extension template.\]</span></span>

<span data-ttu-id="3ace7-106">Die **Name** -Eigenschaft ruft den Namen der Vorlage ab.</span><span class="sxs-lookup"><span data-stu-id="3ace7-106">The **Name** property retrieves the name of the template.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ace7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3ace7-107">Syntax</span></span>


```VB
Template.Name As String
```



## <a name="property-value"></a><span data-ttu-id="3ace7-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="3ace7-108">Property value</span></span>

<span data-ttu-id="3ace7-109">Der Name der Vorlage.</span><span class="sxs-lookup"><span data-stu-id="3ace7-109">The name of the template.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ace7-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3ace7-110">Requirements</span></span>



| <span data-ttu-id="3ace7-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3ace7-111">Requirement</span></span> | <span data-ttu-id="3ace7-112">Wert</span><span class="sxs-lookup"><span data-stu-id="3ace7-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ace7-113">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="3ace7-113">Redistributable</span></span><br/> | <span data-ttu-id="3ace7-114">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="3ace7-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="3ace7-115">DLL</span><span class="sxs-lookup"><span data-stu-id="3ace7-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="3ace7-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ace7-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ace7-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3ace7-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ace7-118">**Vorlage**</span><span class="sxs-lookup"><span data-stu-id="3ace7-118">**Template**</span></span>](template.md)
</dt> </dl>

 

 
