---
description: Stellt einen CPS-Zeiger (Certification Practice Statement) oder einen Benutzer Hinweis Qualifizierer dar.
ms.assetid: 857af3d6-aa7b-429a-a056-72573232f72c
title: Qualifiziererobjekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3b1740e064cac53f93d9c81603477a1230c7fd7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358107"
---
# <a name="qualifier-object"></a><span data-ttu-id="3f9e0-103">Qualifiziererobjekt</span><span class="sxs-lookup"><span data-stu-id="3f9e0-103">Qualifier object</span></span>

<span data-ttu-id="3f9e0-104">\[Das **qualifiziererobjekt** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="3f9e0-104">\[The **Qualifier** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3f9e0-105">Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace, indem Sie den Konstruktor aufrufen, der eine OID als Parameter annimmt, und dann die OID für Zertifikat Richtlinien verwenden, um Qualifizierer zu verarbeiten, die Teil der Richtlinien Informationen in der Zertifikat Richtlinien Erweiterung sind.\]</span><span class="sxs-lookup"><span data-stu-id="3f9e0-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="3f9e0-106">Das **qualifiziererobjekt** stellt einen CPS-Zeiger (Certification Practice Statement) oder einen Benutzer Hinweis Qualifizierer dar.</span><span class="sxs-lookup"><span data-stu-id="3f9e0-106">The **Qualifier** object represents a Certification Practice Statement (CPS) pointer or user notice qualifier.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="3f9e0-107">Verwendung</span><span class="sxs-lookup"><span data-stu-id="3f9e0-107">When to use</span></span>

<span data-ttu-id="3f9e0-108">Das **qualifiziererobjekt** wird verwendet, um die folgenden Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="3f9e0-108">The **Qualifier** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="3f9e0-109">Ruft den Objekt Bezeichner des Qualifizierers ab.</span><span class="sxs-lookup"><span data-stu-id="3f9e0-109">Retrieve the object identifier of the qualifier.</span></span>
-   <span data-ttu-id="3f9e0-110">Rufen Sie die Uniform Resource Identifier (URI) ab, die auf eine von der Zertifizierungsstelle ( [*Certification Authority*](../secgloss/c-gly.md) , ca) veröffentlichte CPS verweist.</span><span class="sxs-lookup"><span data-stu-id="3f9e0-110">Retrieve the Uniform Resource Identifier (URI) that points to a CPS published by the [*certification authority*](../secgloss/c-gly.md) (CA).</span></span>
-   <span data-ttu-id="3f9e0-111">Ruft den Namen der dem Qualifizierer zugeordneten Organisation ab.</span><span class="sxs-lookup"><span data-stu-id="3f9e0-111">Retrieve the name of the organization associated with the qualifier.</span></span>
-   <span data-ttu-id="3f9e0-112">Rufen Sie den Namen und den Inhalt einer Benutzer Benachrichtigung ab.</span><span class="sxs-lookup"><span data-stu-id="3f9e0-112">Retrieve the name and content of a user notice.</span></span>

## <a name="members"></a><span data-ttu-id="3f9e0-113">Member</span><span class="sxs-lookup"><span data-stu-id="3f9e0-113">Members</span></span>

<span data-ttu-id="3f9e0-114">Das **qualifiziererobjekt** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="3f9e0-114">The **Qualifier** object has these types of members:</span></span>

-   [<span data-ttu-id="3f9e0-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3f9e0-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3f9e0-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3f9e0-116">Properties</span></span>

<span data-ttu-id="3f9e0-117">Das **qualifiziererobjekt** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3f9e0-117">The **Qualifier** object has these properties.</span></span>



| <span data-ttu-id="3f9e0-118">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3f9e0-118">Property</span></span>                                                          | <span data-ttu-id="3f9e0-119">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="3f9e0-119">Access type</span></span>          | <span data-ttu-id="3f9e0-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3f9e0-120">Description</span></span>                                                                                                                         |
|:------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3f9e0-121">**Cpspointer**</span><span class="sxs-lookup"><span data-stu-id="3f9e0-121">**CPSPointer**</span></span>](qualifier-cpspointer.md)<br/>             | <span data-ttu-id="3f9e0-122">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3f9e0-122">Read-only</span></span><br/> | <span data-ttu-id="3f9e0-123">Ruft eine Zeichenfolge ab, die den URI enthält, der auf ein von der Zertifizierungsstelle veröffentlichtes CPS verweist.</span><span class="sxs-lookup"><span data-stu-id="3f9e0-123">Retrieves a string that contains the URI that points to a CPS published by the CA.</span></span><br/>                                       |
| [<span data-ttu-id="3f9e0-124">**Explizertext**</span><span class="sxs-lookup"><span data-stu-id="3f9e0-124">**ExplicitText**</span></span>](qualifier-explicittext.md)<br/>         | <span data-ttu-id="3f9e0-125">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3f9e0-125">Read-only</span></span><br/> | <span data-ttu-id="3f9e0-126">Ruft eine Zeichenfolge ab, die den Inhalt der Benutzer Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="3f9e0-126">Retrieves a string that contains the content of the user notice.</span></span> <span data-ttu-id="3f9e0-127">Diese Eigenschaft ist möglicherweise leer.</span><span class="sxs-lookup"><span data-stu-id="3f9e0-127">This property may be empty.</span></span><br/>                             |
| [<span data-ttu-id="3f9e0-128">**Benachrichtifür Notierungen**</span><span class="sxs-lookup"><span data-stu-id="3f9e0-128">**NoticeNumbers**</span></span>](qualifier-noticenumbers.md)<br/>       | <span data-ttu-id="3f9e0-129">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3f9e0-129">Read-only</span></span><br/> | <span data-ttu-id="3f9e0-130">Ruft ein **noticenumbers** -Objekt ab, das die Auflistung der Benutzer Hinweis Nummern enthält.</span><span class="sxs-lookup"><span data-stu-id="3f9e0-130">Retrieves a **NoticeNumbers** object that contains the collection of user notice numbers.</span></span> <span data-ttu-id="3f9e0-131">Diese Eigenschaft ist möglicherweise leer.</span><span class="sxs-lookup"><span data-stu-id="3f9e0-131">This property may be empty.</span></span><br/>    |
| [<span data-ttu-id="3f9e0-132">**OID**</span><span class="sxs-lookup"><span data-stu-id="3f9e0-132">**OID**</span></span>](qualifier-oid.md)<br/>                           | <span data-ttu-id="3f9e0-133">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3f9e0-133">Read-only</span></span><br/> | <span data-ttu-id="3f9e0-134">Ruft ein [**OID**](oid.md) -Objekt ab, das den Qualifizierer identifiziert.</span><span class="sxs-lookup"><span data-stu-id="3f9e0-134">Retrieves an [**OID**](oid.md) object that identifies the qualifier.</span></span> <span data-ttu-id="3f9e0-135">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="3f9e0-135">This is the default property.</span></span><br/>                      |
| [<span data-ttu-id="3f9e0-136">**OrganizationName**</span><span class="sxs-lookup"><span data-stu-id="3f9e0-136">**OrganizationName**</span></span>](qualifier-organizationname.md)<br/> | <span data-ttu-id="3f9e0-137">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3f9e0-137">Read-only</span></span><br/> | <span data-ttu-id="3f9e0-138">Ruft eine Zeichenfolge ab, die den Namen der dem Qualifizierer zugeordneten Organisation enthält.</span><span class="sxs-lookup"><span data-stu-id="3f9e0-138">Retrieves a string that contains the name of the organization associated with the qualifier.</span></span> <span data-ttu-id="3f9e0-139">Diese Eigenschaft ist möglicherweise leer.</span><span class="sxs-lookup"><span data-stu-id="3f9e0-139">This property may be empty.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3f9e0-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3f9e0-140">Remarks</span></span>

<span data-ttu-id="3f9e0-141">Das **qualifiziererobjekt** kann nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="3f9e0-141">The **Qualifier** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f9e0-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3f9e0-142">Requirements</span></span>



| <span data-ttu-id="3f9e0-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3f9e0-143">Requirement</span></span> | <span data-ttu-id="3f9e0-144">Wert</span><span class="sxs-lookup"><span data-stu-id="3f9e0-144">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f9e0-145">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="3f9e0-145">Redistributable</span></span><br/> | <span data-ttu-id="3f9e0-146">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="3f9e0-146">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="3f9e0-147">DLL</span><span class="sxs-lookup"><span data-stu-id="3f9e0-147">DLL</span></span><br/>             | <dl> <span data-ttu-id="3f9e0-148"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f9e0-148"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
