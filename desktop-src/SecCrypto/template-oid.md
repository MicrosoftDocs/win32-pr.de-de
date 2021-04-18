---
description: Ruft ein Oid-Objekt ab, das das Vorlagen Objekt identifiziert.
ms.assetid: bdd9d401-e9c4-4307-9817-7dcb55c539f8
title: Template. Oid (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4a8599ac999c7d6a3e3403d94ff2c6daf0eba48b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352036"
---
# <a name="templateoid-property"></a><span data-ttu-id="3bc1c-103">Template. Oid (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3bc1c-103">Template.OID property</span></span>

<span data-ttu-id="3bc1c-104">\[Die **OID** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="3bc1c-104">\[The **OID** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3bc1c-105">Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace, indem Sie den Konstruktor aufrufen, der eine OID als Parameter annimmt, und verwenden Sie dann die OID für die Zertifikat Vorlage, um die Zertifikat Erweiterungs Vorlage abzurufen.\]</span><span class="sxs-lookup"><span data-stu-id="3bc1c-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Template to retrieve the certificate extension template.\]</span></span>

<span data-ttu-id="3bc1c-106">Die **OID** -Eigenschaft ruft ein [**OID**](oid.md) -Objekt ab, das das [**Vorlagen**](template.md) Objekt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="3bc1c-106">The **OID** property retrieves an [**OID**](oid.md) object that identifies the [**Template**](template.md) object.</span></span>

<span data-ttu-id="3bc1c-107">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="3bc1c-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bc1c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3bc1c-108">Syntax</span></span>


```VB
Template.OID As OID
```



## <a name="property-value"></a><span data-ttu-id="3bc1c-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="3bc1c-109">Property value</span></span>

<span data-ttu-id="3bc1c-110">Ein [**OID**](oid.md) -Objekt, das das [**Vorlagen**](template.md) Objekt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="3bc1c-110">An [**OID**](oid.md) object that identifies the [**Template**](template.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bc1c-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3bc1c-111">Requirements</span></span>



| <span data-ttu-id="3bc1c-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3bc1c-112">Requirement</span></span> | <span data-ttu-id="3bc1c-113">Wert</span><span class="sxs-lookup"><span data-stu-id="3bc1c-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3bc1c-114">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="3bc1c-114">Redistributable</span></span><br/> | <span data-ttu-id="3bc1c-115">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="3bc1c-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="3bc1c-116">DLL</span><span class="sxs-lookup"><span data-stu-id="3bc1c-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="3bc1c-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3bc1c-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bc1c-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3bc1c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bc1c-119">**Vorlage**</span><span class="sxs-lookup"><span data-stu-id="3bc1c-119">**Template**</span></span>](template.md)
</dt> </dl>

 

 
