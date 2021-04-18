---
description: Stellt die Zertifikat Erweiterungs Vorlage des Zertifikats dar.
ms.assetid: 1ae9220a-f6b3-47c5-bd08-a36ffd84e1f9
title: Vorlagen Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: fedd64979ad74ceac3f6d54af58c57d8d8b2b134
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371232"
---
# <a name="template-object"></a><span data-ttu-id="c9c26-103">Vorlagen Objekt</span><span class="sxs-lookup"><span data-stu-id="c9c26-103">Template object</span></span>

<span data-ttu-id="c9c26-104">\[Das **Vorlagen** Objekt ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="c9c26-104">\[The **Template** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c9c26-105">Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace, indem Sie den Konstruktor aufrufen, der eine OID als Parameter annimmt, und verwenden Sie dann die OID für die Zertifikat Vorlage, um die Zertifikat Erweiterungs Vorlage abzurufen.\]</span><span class="sxs-lookup"><span data-stu-id="c9c26-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Template to retrieve the certificate extension template.\]</span></span>

<span data-ttu-id="c9c26-106">Das **Vorlagen** Objekt stellt die Zertifikat Erweiterungs Vorlage des Zertifikats dar.</span><span class="sxs-lookup"><span data-stu-id="c9c26-106">The **Template** object represents the certificate extension template of the certificate.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="c9c26-107">Verwendung</span><span class="sxs-lookup"><span data-stu-id="c9c26-107">When to use</span></span>

<span data-ttu-id="c9c26-108">Das **Vorlagen** Objekt wird verwendet, um die folgenden Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="c9c26-108">The **Template** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="c9c26-109">Bestimmen Sie, ob die Vorlage als kritisch oder vorhanden markiert ist.</span><span class="sxs-lookup"><span data-stu-id="c9c26-109">Determine whether the template is marked critical or present.</span></span>
-   <span data-ttu-id="c9c26-110">Rufen Sie die [*Objekt Kennung*](../secgloss/o-gly.md) (OID) oder den Namen der Vorlage ab.</span><span class="sxs-lookup"><span data-stu-id="c9c26-110">Retrieve the [*object identifier*](../secgloss/o-gly.md) (OID) or name of the template.</span></span>
-   <span data-ttu-id="c9c26-111">Rufen Sie die neben Version oder die Hauptversion der Vorlage ab.</span><span class="sxs-lookup"><span data-stu-id="c9c26-111">Retrieve the minor or major version of the template.</span></span>

## <a name="members"></a><span data-ttu-id="c9c26-112">Member</span><span class="sxs-lookup"><span data-stu-id="c9c26-112">Members</span></span>

<span data-ttu-id="c9c26-113">Das **Vorlagen** Objekt enthält diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c9c26-113">The **Template** object has these types of members:</span></span>

-   [<span data-ttu-id="c9c26-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c9c26-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c9c26-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c9c26-115">Properties</span></span>

<span data-ttu-id="c9c26-116">Das **Vorlagen** Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c9c26-116">The **Template** object has these properties.</span></span>



| <span data-ttu-id="c9c26-117">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c9c26-117">Property</span></span>                                                 | <span data-ttu-id="c9c26-118">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="c9c26-118">Access type</span></span>          | <span data-ttu-id="c9c26-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c9c26-119">Description</span></span>                                                                                            |
|:---------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c9c26-120">**IsCritical**</span><span class="sxs-lookup"><span data-stu-id="c9c26-120">**IsCritical**</span></span>](template-iscritical.md)<br/>     | <span data-ttu-id="c9c26-121">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c9c26-121">Read-only</span></span><br/> | <span data-ttu-id="c9c26-122">Ruft einen booleschen Wert ab, der angibt, ob die Vorlagen Erweiterung als kritisch markiert ist.</span><span class="sxs-lookup"><span data-stu-id="c9c26-122">Retrieves a Boolean value that indicates whether the template extension is marked critical.</span></span><br/> |
| [<span data-ttu-id="c9c26-123">**IsPresent**</span><span class="sxs-lookup"><span data-stu-id="c9c26-123">**IsPresent**</span></span>](template-ispresent.md)<br/>       | <span data-ttu-id="c9c26-124">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c9c26-124">Read-only</span></span><br/> | <span data-ttu-id="c9c26-125">Ruft einen booleschen Wert ab, der angibt, ob die Vorlagen Erweiterung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c9c26-125">Retrieves a Boolean value that indicates whether the template extension is present.</span></span><br/>         |
| [<span data-ttu-id="c9c26-126">**MajorVersion**</span><span class="sxs-lookup"><span data-stu-id="c9c26-126">**MajorVersion**</span></span>](template-majorversion.md)<br/> | <span data-ttu-id="c9c26-127">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c9c26-127">Read-only</span></span><br/> | <span data-ttu-id="c9c26-128">Ruft die Hauptversionsnummer der Vorlage ab.</span><span class="sxs-lookup"><span data-stu-id="c9c26-128">Retrieves the major version number of the template.</span></span><br/>                                         |
| [<span data-ttu-id="c9c26-129">**MinorVersion**</span><span class="sxs-lookup"><span data-stu-id="c9c26-129">**MinorVersion**</span></span>](template-minorversion.md)<br/> | <span data-ttu-id="c9c26-130">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c9c26-130">Read-only</span></span><br/> | <span data-ttu-id="c9c26-131">Ruft die neben Versionsnummer der Vorlage ab.</span><span class="sxs-lookup"><span data-stu-id="c9c26-131">Retrieves the minor version number of the template.</span></span><br/>                                         |
| [<span data-ttu-id="c9c26-132">**Name**</span><span class="sxs-lookup"><span data-stu-id="c9c26-132">**Name**</span></span>](template-name.md)<br/>                 | <span data-ttu-id="c9c26-133">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c9c26-133">Read-only</span></span><br/> | <span data-ttu-id="c9c26-134">Ruft eine Zeichenfolge ab, die den Namen der Vorlage enthält.</span><span class="sxs-lookup"><span data-stu-id="c9c26-134">Retrieves a string that contains the name of the template.</span></span><br/>                                  |
| [<span data-ttu-id="c9c26-135">**OID**</span><span class="sxs-lookup"><span data-stu-id="c9c26-135">**OID**</span></span>](template-oid.md)<br/>                   | <span data-ttu-id="c9c26-136">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c9c26-136">Read-only</span></span><br/> | <span data-ttu-id="c9c26-137">Ruft ein [**OID**](oid.md) -Objekt ab, das das **Vorlagen** Objekt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c9c26-137">Retrieves an [**OID**](oid.md) object that identifies the **Template** object.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="c9c26-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c9c26-138">Remarks</span></span>

<span data-ttu-id="c9c26-139">Das **Vorlagen** Objekt kann nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c9c26-139">The **Template** object cannot be created.</span></span>

<span data-ttu-id="c9c26-140">Ein **Vorlagen** Objekt wird von der [**Certificate. Template**](certificate-template.md) -Methode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c9c26-140">A **Template** object is returned by the [**Certificate.Template**](certificate-template.md) method.</span></span>

<span data-ttu-id="c9c26-141">CAPICOM verwendet zwei unterschiedliche Versionen von Zertifikat Vorlagen.</span><span class="sxs-lookup"><span data-stu-id="c9c26-141">CAPICOM uses two different versions of certificate templates.</span></span> <span data-ttu-id="c9c26-142">In der folgenden Tabelle werden der Name und die OID für jede Zertifikat Vorlagen Version angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c9c26-142">The following table shows the name and OID for each certificate template version.</span></span>



| <span data-ttu-id="c9c26-143">Version</span><span class="sxs-lookup"><span data-stu-id="c9c26-143">Version</span></span> | <span data-ttu-id="c9c26-144">Name</span><span class="sxs-lookup"><span data-stu-id="c9c26-144">Name</span></span>                               | <span data-ttu-id="c9c26-145">OID</span><span class="sxs-lookup"><span data-stu-id="c9c26-145">OID</span></span>                    |
|---------|------------------------------------|------------------------|
| <span data-ttu-id="c9c26-146">V1</span><span class="sxs-lookup"><span data-stu-id="c9c26-146">V1</span></span>      | <span data-ttu-id="c9c26-147">szoid \_ ENROLL \_ certtype- \_ Erweiterung</span><span class="sxs-lookup"><span data-stu-id="c9c26-147">szOID\_ENROLL\_CERTTYPE\_EXTENSION</span></span> | <span data-ttu-id="c9c26-148">"1.3.6.1.4.1.311.20.2"</span><span class="sxs-lookup"><span data-stu-id="c9c26-148">"1.3.6.1.4.1.311.20.2"</span></span> |
| <span data-ttu-id="c9c26-149">V2</span><span class="sxs-lookup"><span data-stu-id="c9c26-149">V2</span></span>      | <span data-ttu-id="c9c26-150">szoid- \_ Zertifikat \_ Vorlage</span><span class="sxs-lookup"><span data-stu-id="c9c26-150">szOID\_CERTIFICATE\_TEMPLATE</span></span>       | <span data-ttu-id="c9c26-151">"1.3.6.1.4.1.311.21.7"</span><span class="sxs-lookup"><span data-stu-id="c9c26-151">"1.3.6.1.4.1.311.21.7"</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="c9c26-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c9c26-152">Requirements</span></span>



| <span data-ttu-id="c9c26-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c9c26-153">Requirement</span></span> | <span data-ttu-id="c9c26-154">Wert</span><span class="sxs-lookup"><span data-stu-id="c9c26-154">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9c26-155">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="c9c26-155">Redistributable</span></span><br/> | <span data-ttu-id="c9c26-156">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="c9c26-156">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c9c26-157">DLL</span><span class="sxs-lookup"><span data-stu-id="c9c26-157">DLL</span></span><br/>             | <dl> <span data-ttu-id="c9c26-158"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9c26-158"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
