---
description: Ruft den Namen der dem Qualifizierer zugeordneten Organisation ab.
ms.assetid: 4ceb2c0f-903d-4fcd-8446-abf3175fe8e0
title: Qualifizierer. OrganizationName-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.OrganizationName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3b1e1ebb2b948d5a933b59e86c8753b6b68a3a94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368465"
---
# <a name="qualifierorganizationname-property"></a><span data-ttu-id="616c4-103">Qualifizierer. OrganizationName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="616c4-103">Qualifier.OrganizationName property</span></span>

<span data-ttu-id="616c4-104">\[Die Eigenschaft " **OrganizationName** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="616c4-104">\[The **OrganizationName** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="616c4-105">Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace, indem Sie den Konstruktor aufrufen, der eine OID als Parameter annimmt, und dann die OID für Zertifikat Richtlinien verwenden, um Qualifizierer zu verarbeiten, die Teil der Richtlinien Informationen in der Zertifikat Richtlinien Erweiterung sind.\]</span><span class="sxs-lookup"><span data-stu-id="616c4-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="616c4-106">Die **OrganizationName** -Eigenschaft ruft den Namen der Organisation ab, die dem Qualifizierer zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="616c4-106">The **OrganizationName** property retrieves the name of the organization associated with the qualifier.</span></span> <span data-ttu-id="616c4-107">Diese Eigenschaft ist möglicherweise leer.</span><span class="sxs-lookup"><span data-stu-id="616c4-107">This property may be empty.</span></span>

## <a name="syntax"></a><span data-ttu-id="616c4-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="616c4-108">Syntax</span></span>


```VB
Qualifier.OrganizationName As String
```



## <a name="property-value"></a><span data-ttu-id="616c4-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="616c4-109">Property value</span></span>

<span data-ttu-id="616c4-110">Der Name der Organisation, die dem Qualifizierer zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="616c4-110">The name of the organization associated with the qualifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="616c4-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="616c4-111">Requirements</span></span>



| <span data-ttu-id="616c4-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="616c4-112">Requirement</span></span> | <span data-ttu-id="616c4-113">Wert</span><span class="sxs-lookup"><span data-stu-id="616c4-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="616c4-114">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="616c4-114">Redistributable</span></span><br/> | <span data-ttu-id="616c4-115">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="616c4-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="616c4-116">DLL</span><span class="sxs-lookup"><span data-stu-id="616c4-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="616c4-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="616c4-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="616c4-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="616c4-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="616c4-119">**Qualifizierer**</span><span class="sxs-lookup"><span data-stu-id="616c4-119">**Qualifier**</span></span>](qualifier.md)
</dt> </dl>

 

 
