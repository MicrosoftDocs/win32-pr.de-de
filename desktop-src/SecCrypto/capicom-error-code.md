---
description: Definiert Fehlercodes, die von CAPICOM zurückgegeben werden.
ms.assetid: e72b8290-b482-4629-8b87-5a15677865a6
title: CAPICOM_ERROR_CODE-Enumeration (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ERROR_CODE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: ccd4963c83f1ad7ce3bc686b7736ce47d699ce30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361970"
---
# <a name="capicom_error_code-enumeration"></a><span data-ttu-id="89e27-103">CAPICOM- \_ Fehler \_ Code-Enumeration</span><span class="sxs-lookup"><span data-stu-id="89e27-103">CAPICOM\_ERROR\_CODE enumeration</span></span>

<span data-ttu-id="89e27-104">Der-Enumerationstyp " **CAPICOM- \_ Fehler \_ Code** " definiert Fehlercodes, die von CAPICOM zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="89e27-104">The **CAPICOM\_ERROR\_CODE** enumeration type defines error codes that are returned by CAPICOM.</span></span>

> [!Note]  
> <span data-ttu-id="89e27-105">Visual Basic Scripting Edition Fehler geben einen **Err. Number** -Wert größer als 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="89e27-105">Visual Basic Scripting Edition errors return an **Err.number** value greater than zero.</span></span> <span data-ttu-id="89e27-106">Für diese Fehler enthalten **Err. Description** -Werte Informationen zur Ursache des Fehlers.</span><span class="sxs-lookup"><span data-stu-id="89e27-106">For those errors, **Err.Description** values provide information about the cause of the error.</span></span> <span data-ttu-id="89e27-107">Zusätzlich zu Visual Basic Scripting Edition Fehlern geben CAPICOM-Fehler die vom **CAPICOM- \_ Fehler \_ Code** definierten Codes zurück.</span><span class="sxs-lookup"><span data-stu-id="89e27-107">In addition to Visual Basic Scripting Edition errors, CAPICOM errors return the codes defined by **CAPICOM\_ERROR\_CODE**.</span></span>

 

## <a name="members"></a><span data-ttu-id="89e27-108">Member</span><span class="sxs-lookup"><span data-stu-id="89e27-108">Members</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="89e27-109">Member</span><span class="sxs-lookup"><span data-stu-id="89e27-109">Member</span></span></th>
<th><span data-ttu-id="89e27-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="89e27-110">Description</span></span></th>
<th><span data-ttu-id="89e27-111">Wert</span><span class="sxs-lookup"><span data-stu-id="89e27-111">Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="89e27-112"><strong>CAPICOM_E_ENCODE_INVALID_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-112"><strong>CAPICOM_E_ENCODE_INVALID_TYPE</strong></span></span></td>
<td><span data-ttu-id="89e27-113">Es wurde ein ungültiger Codierungstyp verwendet.</span><span class="sxs-lookup"><span data-stu-id="89e27-113">An encoding type that is not valid was used.</span></span><br/> <span data-ttu-id="89e27-114">In der folgenden Liste werden die gültigen Codierungs Typen angezeigt:</span><span class="sxs-lookup"><span data-stu-id="89e27-114">The following list shows the valid encoding types:</span></span>
<ul>
<li><span data-ttu-id="89e27-115">CAPICOM_ENCODE_ANY</span><span class="sxs-lookup"><span data-stu-id="89e27-115">CAPICOM_ENCODE_ANY</span></span></li>
<li><span data-ttu-id="89e27-116">CAPICOM_ENCODE_BASE64</span><span class="sxs-lookup"><span data-stu-id="89e27-116">CAPICOM_ENCODE_BASE64</span></span></li>
<li><span data-ttu-id="89e27-117">CAPICOM_ENCODE_BINARY</span><span class="sxs-lookup"><span data-stu-id="89e27-117">CAPICOM_ENCODE_BINARY</span></span></li>
</ul>
<br/></td>
<td><span data-ttu-id="89e27-118">0x80880100</span><span class="sxs-lookup"><span data-stu-id="89e27-118">0x80880100</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89e27-119"><strong>CAPICOM_E_EKU_INVALID_OID</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-119"><strong>CAPICOM_E_EKU_INVALID_OID</strong></span></span></td>
<td><span data-ttu-id="89e27-120">Die <a href="eku-oid.md"><strong>OID</strong></a> -Eigenschaft des <a href="eku.md"><strong>EKU</strong></a> -Objekts kann nicht festgelegt werden, da die <a href="eku-name.md"><strong>Name</strong></a> -Eigenschaft nicht auf CAPICOM_EKU_OTHER festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="89e27-120">The <a href="eku-oid.md"><strong>OID</strong></a> property of the <a href="eku.md"><strong>EKU</strong></a> object cannot be set because the <a href="eku-name.md"><strong>Name</strong></a> property is not set to CAPICOM_EKU_OTHER.</span></span><br/> <span data-ttu-id="89e27-121">Legen Sie die <a href="eku-name.md"><strong>Name</strong></a> -Eigenschaft auf CAPICOM_EKU_OTHER fest, bevor Sie die <a href="eku-oid.md"><strong>OID</strong></a> -Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="89e27-121">Set the <a href="eku-name.md"><strong>Name</strong></a> property to CAPICOM_EKU_OTHER before setting the <a href="eku-oid.md"><strong>OID</strong></a> property.</span></span><br/></td>
<td><span data-ttu-id="89e27-122">0x80880200</span><span class="sxs-lookup"><span data-stu-id="89e27-122">0x80880200</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89e27-123"><strong>CAPICOM_E_EKU_OID_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-123"><strong>CAPICOM_E_EKU_OID_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="89e27-124">Die <a href="eku-oid.md"><strong>OID</strong></a> -Eigenschaft des <a href="eku.md"><strong>EKU</strong></a> -Objekts wurde nicht initialisiert.</span><span class="sxs-lookup"><span data-stu-id="89e27-124">The <a href="eku-oid.md"><strong>OID</strong></a> property of the <a href="eku.md"><strong>EKU</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="89e27-125">Legen Sie die <a href="eku-name.md"><strong>Name</strong></a> -Eigenschaft entweder auf einen anderen Wert als CAPICOM_EKU_OTHER fest, oder legen Sie die <strong>Name</strong> -Eigenschaft auf CAPICOM_EKU_OTHER und die <a href="eku-oid.md"><strong>OID</strong></a> -Eigenschaft auf einen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="89e27-125">Either set the <a href="eku-name.md"><strong>Name</strong></a> property to anything other than CAPICOM_EKU_OTHER, or set the <strong>Name</strong> property to CAPICOM_EKU_OTHER and the <a href="eku-oid.md"><strong>OID</strong></a> property to a value.</span></span><br/></td>
<td><span data-ttu-id="89e27-126">0x80880201</span><span class="sxs-lookup"><span data-stu-id="89e27-126">0x80880201</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89e27-127"><strong>CAPICOM_E_CERTIFICATE_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-127"><strong>CAPICOM_E_CERTIFICATE_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="89e27-128">Das <a href="certificate.md"><strong>Zertifikat</strong></a> Objekt wurde nicht initialisiert.</span><span class="sxs-lookup"><span data-stu-id="89e27-128">The <a href="certificate.md"><strong>Certificate</strong></a> object has not been initialized.</span></span><br/> <span data-ttu-id="89e27-129">Normalerweise wird dieser Fehlercode zurückgegeben, wenn ein <a href="certificate.md"><strong>Zertifikat</strong></a> Objekt instanziiert, aber keinem digitalen Zertifikat zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="89e27-129">Usually, this error code is returned when a <a href="certificate.md"><strong>Certificate</strong></a> object is instantiated but not associated with a digital certificate.</span></span> <span data-ttu-id="89e27-130">Um das Objekt einem digitalen Zertifikat zuzuordnen, weisen Sie es entweder einem vorhandenen <strong>Zertifikat</strong> Objekt zu, oder wenden Sie die <a href="certificate-import.md"><strong>Import</strong></a> Methode an.</span><span class="sxs-lookup"><span data-stu-id="89e27-130">To associate the object with a digital certificate, either assign it to an existing <strong>Certificate</strong> object or call the <a href="certificate-import.md"><strong>Import</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="89e27-131">0x80880210</span><span class="sxs-lookup"><span data-stu-id="89e27-131">0x80880210</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89e27-132"><strong>CAPICOM_E_CERTIFICATE_NO_PRIVATE_KEY</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-132"><strong>CAPICOM_E_CERTIFICATE_NO_PRIVATE_KEY</strong></span></span></td>
<td><span data-ttu-id="89e27-133">Dem <a href="certificate.md"><strong>Zertifikat</strong></a> Objekt ist kein privater Schlüssel zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="89e27-133">The <a href="certificate.md"><strong>Certificate</strong></a> object does not have an associated private key.</span></span><br/> <span data-ttu-id="89e27-134">Dieser Fehlercode wird zurückgegeben, wenn versucht wird, Daten mit dem privaten Schlüssel des Signatur Gebers zu signieren, aber das <a href="certificate.md"><strong>Zertifikat</strong></a> Objekt, das dem <a href="signer.md"><strong>Signatur</strong></a> Geber Objekt zugeordnet ist, kann nicht für den Signier Vorgang verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="89e27-134">This error code is returned when an attempt is made to sign data using the signer's private key, but the <a href="certificate.md"><strong>Certificate</strong></a> object that is associated with the <a href="signer.md"><strong>Signer</strong></a> object cannot be used for the signing operation.</span></span><br/></td>
<td><span data-ttu-id="89e27-135">0x80880211</span><span class="sxs-lookup"><span data-stu-id="89e27-135">0x80880211</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89e27-136"><strong>CAPICOM_E_CHAIN_NOT_BUILT</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-136"><strong>CAPICOM_E_CHAIN_NOT_BUILT</strong></span></span></td>
<td><span data-ttu-id="89e27-137">Das <a href="chain.md"><strong>Ketten</strong></a> Objekt wurde nicht initialisiert.</span><span class="sxs-lookup"><span data-stu-id="89e27-137">The <a href="chain.md"><strong>Chain</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="89e27-138">Um das <a href="chain.md"><strong>Ketten</strong></a> Objekt zu initialisieren, müssen Sie die Buildmethode aufzurufen. <a href="chain-build.md"><strong></strong></a></span><span class="sxs-lookup"><span data-stu-id="89e27-138">To initialize the <a href="chain.md"><strong>Chain</strong></a> object, call the <a href="chain-build.md"><strong>Build</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="89e27-139">0x80880220</span><span class="sxs-lookup"><span data-stu-id="89e27-139">0x80880220</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89e27-140"><strong>CAPICOM_E_STORE_NOT_OPENED</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-140"><strong>CAPICOM_E_STORE_NOT_OPENED</strong></span></span></td>
<td><span data-ttu-id="89e27-141">Das <a href="store.md"><strong>Speicher</strong></a> Objekt wurde nicht initialisiert.</span><span class="sxs-lookup"><span data-stu-id="89e27-141">The <a href="store.md"><strong>Store</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="89e27-142">Um das <a href="store.md"><strong>Speicher</strong></a> Objekt zu initialisieren, nennen Sie die <a href="store-open.md"><strong>Open</strong></a> -Methode.</span><span class="sxs-lookup"><span data-stu-id="89e27-142">To initialize the <a href="store.md"><strong>Store</strong></a> object, call the <a href="store-open.md"><strong>Open</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="89e27-143">0x80880230</span><span class="sxs-lookup"><span data-stu-id="89e27-143">0x80880230</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89e27-144"><strong>CAPICOM_E_STORE_EMPTY</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-144"><strong>CAPICOM_E_STORE_EMPTY</strong></span></span></td>
<td><span data-ttu-id="89e27-145">Das <a href="store.md"><strong>Store</strong></a> -Objekt enthält keine <a href="certificate.md"><strong>Zertifikat</strong></a> Objekte.</span><span class="sxs-lookup"><span data-stu-id="89e27-145">The <a href="store.md"><strong>Store</strong></a> object does not contain any <a href="certificate.md"><strong>Certificate</strong></a> objects.</span></span><br/></td>
<td><span data-ttu-id="89e27-146">0x80880231</span><span class="sxs-lookup"><span data-stu-id="89e27-146">0x80880231</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89e27-147"><strong>CAPICOM_E_STORE_INVALID_OPEN_MODE</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-147"><strong>CAPICOM_E_STORE_INVALID_OPEN_MODE</strong></span></span></td>
<td><span data-ttu-id="89e27-148">Der <em>OpenMode</em> -Parameter der <a href="store-open.md"><strong>Store. Open</strong></a> -Methode enthält keinen gültigen Wert CAPICOM_STORE_OPEN_MODE.</span><span class="sxs-lookup"><span data-stu-id="89e27-148">The <em>OpenMode</em> parameter of the <a href="store-open.md"><strong>Store.Open</strong></a> method does not contain a valid value of CAPICOM_STORE_OPEN_MODE.</span></span><br/> <span data-ttu-id="89e27-149">In der folgenden Liste werden die gültigen Werte CAPICOM_STORE_OPEN_MODE angezeigt:</span><span class="sxs-lookup"><span data-stu-id="89e27-149">The following list shows the valid values of CAPICOM_STORE_OPEN_MODE:</span></span>
<ul>
<li><span data-ttu-id="89e27-150">CAPICOM_STORE_OPEN_READ_ONLY</span><span class="sxs-lookup"><span data-stu-id="89e27-150">CAPICOM_STORE_OPEN_READ_ONLY</span></span></li>
<li><span data-ttu-id="89e27-151">CAPICOM_STORE_OPEN_READ_WRITE</span><span class="sxs-lookup"><span data-stu-id="89e27-151">CAPICOM_STORE_OPEN_READ_WRITE</span></span></li>
<li><span data-ttu-id="89e27-152">CAPICOM_STORE_OPEN_MAXIMUM_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="89e27-152">CAPICOM_STORE_OPEN_MAXIMUM_ALLOWED</span></span></li>
<li><span data-ttu-id="89e27-153">CAPICOM_STORE_OPEN_EXISTING_ONLY</span><span class="sxs-lookup"><span data-stu-id="89e27-153">CAPICOM_STORE_OPEN_EXISTING_ONLY</span></span></li>
<li><span data-ttu-id="89e27-154">CAPICOM_STORE_OPEN_INCLUDE_ARCHIVED</span><span class="sxs-lookup"><span data-stu-id="89e27-154">CAPICOM_STORE_OPEN_INCLUDE_ARCHIVED</span></span></li>
</ul>
<br/></td>
<td><span data-ttu-id="89e27-155">0x80880232</span><span class="sxs-lookup"><span data-stu-id="89e27-155">0x80880232</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89e27-156"><strong>CAPICOM_E_STORE_INVALID_SAVE_AS_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-156"><strong>CAPICOM_E_STORE_INVALID_SAVE_AS_TYPE</strong></span></span></td>
<td><span data-ttu-id="89e27-157">Der an die <a href="store-export.md"><strong>Export</strong></a> -Methode des <a href="store.md"><strong>Speicher</strong></a> Objekts über gegebene <em>SaveAs</em> -Wert war ungültig.</span><span class="sxs-lookup"><span data-stu-id="89e27-157">The <em>SaveAs</em> value passed to the <a href="store-export.md"><strong>Export</strong></a> method of the <a href="store.md"><strong>Store</strong></a> object was not valid.</span></span> <br/> <span data-ttu-id="89e27-158">In der folgenden Liste werden die gültigen <em>SaveAs</em> -Werte angezeigt:</span><span class="sxs-lookup"><span data-stu-id="89e27-158">The following list shows the valid <em>SaveAs</em> values:</span></span>
<ul>
<li><span data-ttu-id="89e27-159">CAPICOM_STORE_SAVE_AS_SERIALIZED</span><span class="sxs-lookup"><span data-stu-id="89e27-159">CAPICOM_STORE_SAVE_AS_SERIALIZED</span></span></li>
<li><span data-ttu-id="89e27-160">CAPICOM_STORE_SAVE_AS_PKCS7</span><span class="sxs-lookup"><span data-stu-id="89e27-160">CAPICOM_STORE_SAVE_AS_PKCS7</span></span></li>
</ul>
<br/></td>
<td><span data-ttu-id="89e27-161">0x80880233</span><span class="sxs-lookup"><span data-stu-id="89e27-161">0x80880233</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89e27-162"><strong>CAPICOM_E_ATTRIBUTE_NAME_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-162"><strong>CAPICOM_E_ATTRIBUTE_NAME_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="89e27-163">Die <a href="attribute-name.md"><strong>Name</strong></a> -Eigenschaft des <a href="attribute.md"><strong>Attribut</strong></a> Objekts wurde nicht initialisiert.</span><span class="sxs-lookup"><span data-stu-id="89e27-163">The <a href="attribute-name.md"><strong>Name</strong></a> property of the <a href="attribute.md"><strong>Attribute</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="89e27-164">Legen Sie die <a href="attribute-name.md"><strong>Name</strong></a> -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="89e27-164">Set the <a href="attribute-name.md"><strong>Name</strong></a> property.</span></span><br/></td>
<td><span data-ttu-id="89e27-165">0x80880240</span><span class="sxs-lookup"><span data-stu-id="89e27-165">0x80880240</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89e27-166"><strong>CAPICOM_E_ATTRIBUTE_VALUE_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-166"><strong>CAPICOM_E_ATTRIBUTE_VALUE_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="89e27-167">Die <a href="attribute-value.md"><strong>value</strong></a> -Eigenschaft des <a href="attribute.md"><strong>Attribut</strong></a> Objekts wurde nicht initialisiert.</span><span class="sxs-lookup"><span data-stu-id="89e27-167">The <a href="attribute-value.md"><strong>Value</strong></a> property of the <a href="attribute.md"><strong>Attribute</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="89e27-168">Legen Sie die <a href="attribute-value.md"><strong>value</strong></a> -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="89e27-168">Set the <a href="attribute-value.md"><strong>Value</strong></a> property.</span></span><br/></td>
<td><span data-ttu-id="89e27-169">0x80880241</span><span class="sxs-lookup"><span data-stu-id="89e27-169">0x80880241</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89e27-170"><strong>CAPICOM_E_ATTRIBUTE_INVALID_NAME</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-170"><strong>CAPICOM_E_ATTRIBUTE_INVALID_NAME</strong></span></span></td>
<td><span data-ttu-id="89e27-171">Die <a href="attribute-name.md"><strong>Name</strong></a> -Eigenschaft des <a href="attribute.md"><strong>Attribut</strong></a> Objekts ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="89e27-171">The <a href="attribute-name.md"><strong>Name</strong></a> property of the <a href="attribute.md"><strong>Attribute</strong></a> object is not valid.</span></span> <br/> <span data-ttu-id="89e27-172">In der folgenden Liste werden die gültigen Attributnamen angezeigt:</span><span class="sxs-lookup"><span data-stu-id="89e27-172">The following list shows the valid attribute names:</span></span>
<ul>
<li><span data-ttu-id="89e27-173">CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME</span><span class="sxs-lookup"><span data-stu-id="89e27-173">CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME</span></span></li>
<li><span data-ttu-id="89e27-174">CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_NAME</span><span class="sxs-lookup"><span data-stu-id="89e27-174">CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_NAME</span></span></li>
<li><span data-ttu-id="89e27-175">CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="89e27-175">CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_DESCRIPTION</span></span></li>
</ul>
<br/></td>
<td><span data-ttu-id="89e27-176">0x80880242</span><span class="sxs-lookup"><span data-stu-id="89e27-176">0x80880242</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89e27-177"><strong>CAPICOM_E_ATTRIBUTE_INVALID_VALUE</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-177"><strong>CAPICOM_E_ATTRIBUTE_INVALID_VALUE</strong></span></span></td>
<td><span data-ttu-id="89e27-178">Die <a href="attribute-value.md"><strong>value</strong></a> -Eigenschaft des <a href="attribute.md"><strong>Attribut</strong></a> Objekts ist ungültig, da der Datentyp nicht mit dem Datentyp identisch ist, der durch die <strong>Name</strong> -Eigenschaft angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="89e27-178">The <a href="attribute-value.md"><strong>Value</strong></a> property of the <a href="attribute.md"><strong>Attribute</strong></a> object is not valid because the data type does not match the data type indicated by the <strong>Name</strong> property.</span></span> <br/> <span data-ttu-id="89e27-179">Wenn die <a href="attribute-value.md"><strong>Name</strong></a> -Eigenschaft beispielsweise auf CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME festgelegt ist, muss der Datentyp " <strong>Date</strong>" lauten.</span><span class="sxs-lookup"><span data-stu-id="89e27-179">For example, if the <a href="attribute-value.md"><strong>Name</strong></a> property is set to CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME, the data type must be <strong>DATE</strong>.</span></span><br/></td>
<td><span data-ttu-id="89e27-180">0x80880243</span><span class="sxs-lookup"><span data-stu-id="89e27-180">0x80880243</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89e27-181"><strong>CAPICOM_E_SIGNER_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-181"><strong>CAPICOM_E_SIGNER_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="89e27-182">Das <a href="signer.md"><strong>Signatur</strong></a> Geber Objekt wurde nicht initialisiert.</span><span class="sxs-lookup"><span data-stu-id="89e27-182">The <a href="signer.md"><strong>Signer</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="89e27-183">Um das <a href="signer.md"><strong>Signatur</strong></a> Geber Objekt zu initialisieren, legen Sie die Eigenschaft <a href="signer-certificate.md"><strong>Zertifikat</strong></a> fest.</span><span class="sxs-lookup"><span data-stu-id="89e27-183">To initialize the <a href="signer.md"><strong>Signer</strong></a> object, set the <a href="signer-certificate.md"><strong>Certificate</strong></a> property.</span></span><br/></td>
<td><span data-ttu-id="89e27-184">0x80880250</span><span class="sxs-lookup"><span data-stu-id="89e27-184">0x80880250</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89e27-185"><strong>CAPICOM_E_SIGNER_NOT_FOUND</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-185"><strong>CAPICOM_E_SIGNER_NOT_FOUND</strong></span></span></td>
<td><span data-ttu-id="89e27-186">Der Signatur Geber wurde im <a href="signeddata.md"><strong>SignedData</strong></a> -Objekt nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="89e27-186">The signer cannot be found in the <a href="signeddata.md"><strong>SignedData</strong></a> object.</span></span> <br/> <span data-ttu-id="89e27-187">Dies geschieht in der Regel nicht mit einem <a href="signeddata.md"><strong>SignedData</strong></a> -Objekt, das von CAPICOM erstellt wurde. Wenn das <strong>SignedData</strong> -Objekt jedoch von einem Drittanbieter Produkt erstellt wurde, ist das Zertifikat des Signatur Gebers möglicherweise nicht in der PKCS-#7 Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="89e27-187">Usually, this does not happen with a <a href="signeddata.md"><strong>SignedData</strong></a> object that was created by CAPICOM; however, if the <strong>SignedData</strong> object was created by a third-party product, the signer's certificate may not be included in the PKCS #7 structure.</span></span><br/></td>
<td><span data-ttu-id="89e27-188">0x80880251</span><span class="sxs-lookup"><span data-stu-id="89e27-188">0x80880251</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89e27-189"><strong>CAPICOM_E_SIGNER_NO_CHAIN</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-189"><strong>CAPICOM_E_SIGNER_NO_CHAIN</strong></span></span></td>
<td><span data-ttu-id="89e27-190">Ein <a href="chain.md"><strong>Ketten</strong></a> Objekt wurde im <a href="signer.md"><strong>Signatur</strong></a> Geber Objekt nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="89e27-190">A <a href="chain.md"><strong>Chain</strong></a> object cannot be found in the <a href="signer.md"><strong>Signer</strong></a> object.</span></span><br/></td>
<td><span data-ttu-id="89e27-191">0x80880252//v 2.0</span><span class="sxs-lookup"><span data-stu-id="89e27-191">0x80880252 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89e27-192"><strong>CAPICOM_E_SIGNER_INVALID_USAGE</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-192"><strong>CAPICOM_E_SIGNER_INVALID_USAGE</strong></span></span></td>
<td><span data-ttu-id="89e27-193">Es wurde versucht, den Signatur Geber auf eine ungültige Weise zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="89e27-193">An attempt is made to use the signer in a way that is not valid.</span></span><br/></td>
<td><span data-ttu-id="89e27-194">hat folgenden//v2.0</span><span class="sxs-lookup"><span data-stu-id="89e27-194">0x80880253 //v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89e27-195"><strong>CAPICOM_E_SIGN_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-195"><strong>CAPICOM_E_SIGN_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="89e27-196">Das <a href="signeddata.md"><strong>SignedData</strong></a> -Objekt wurde nicht initialisiert.</span><span class="sxs-lookup"><span data-stu-id="89e27-196">The <a href="signeddata.md"><strong>SignedData</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="89e27-197">Um das <a href="signeddata.md"><strong>SignedData</strong></a> -Objekt zu initialisieren, legen Sie die <a href="signeddata-content.md"><strong>Content</strong></a> -Eigenschaft fest, oder nennen Sie die <a href="signeddata-verify.md"><strong>Verify</strong></a> -Methode.</span><span class="sxs-lookup"><span data-stu-id="89e27-197">To initialize the <a href="signeddata.md"><strong>SignedData</strong></a> object, set the <a href="signeddata-content.md"><strong>Content</strong></a> property or call the <a href="signeddata-verify.md"><strong>Verify</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="89e27-198">0x80880260</span><span class="sxs-lookup"><span data-stu-id="89e27-198">0x80880260</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89e27-199"><strong>CAPICOM_E_SIGN_INVALID_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-199"><strong>CAPICOM_E_SIGN_INVALID_TYPE</strong></span></span></td>
<td><span data-ttu-id="89e27-200">Das <a href="signeddata.md"><strong>SignedData</strong></a> -Objekt enthält einen ungültigen Typ.</span><span class="sxs-lookup"><span data-stu-id="89e27-200">The <a href="signeddata.md"><strong>SignedData</strong></a> object contains a type that is not valid.</span></span> <br/> <span data-ttu-id="89e27-201">Dies geschieht normalerweise, wenn versucht wird, eine eingeschlossene Nachricht mit einem <a href="signeddata.md"><strong>SignedData</strong></a> -Objekt zu überprüfen, oder umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="89e27-201">Usually, this happens when an attempt is made to verify an enveloped message with a <a href="signeddata.md"><strong>SignedData</strong></a> object or vice versa.</span></span><br/></td>
<td><span data-ttu-id="89e27-202">0x80880261</span><span class="sxs-lookup"><span data-stu-id="89e27-202">0x80880261</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89e27-203"><strong>CAPICOM_E_SIGN_NOT_SIGNED</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-203"><strong>CAPICOM_E_SIGN_NOT_SIGNED</strong></span></span></td>
<td><span data-ttu-id="89e27-204">Das <a href="signeddata.md"><strong>SignedData</strong></a> -Objekt wurde nicht signiert.</span><span class="sxs-lookup"><span data-stu-id="89e27-204">The <a href="signeddata.md"><strong>SignedData</strong></a> object has not been signed.</span></span> <br/> <span data-ttu-id="89e27-205">Um das <a href="signeddata.md"><strong>SignedData</strong></a> -Objekt zu signieren, nennen Sie die <a href="signeddata-sign.md"><strong>Sign</strong></a> -Methode.</span><span class="sxs-lookup"><span data-stu-id="89e27-205">To sign the <a href="signeddata.md"><strong>SignedData</strong></a> object, call the <a href="signeddata-sign.md"><strong>Sign</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="89e27-206">0x80880262</span><span class="sxs-lookup"><span data-stu-id="89e27-206">0x80880262</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89e27-207"><strong>CAPICOM_E_INVALID_ALGORITHM</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-207"><strong>CAPICOM_E_INVALID_ALGORITHM</strong></span></span></td>
<td><span data-ttu-id="89e27-208">Der Algorithmuswert für die <a href="algorithm-name.md"><strong>Name</strong></a> -Eigenschaft des <a href="algorithm.md"><strong>Algorithmusobjekts</strong></a> ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="89e27-208">The algorithm value for the <a href="algorithm-name.md"><strong>Name</strong></a> property of the <a href="algorithm.md"><strong>Algorithm</strong></a> object is not valid.</span></span> <br/> <span data-ttu-id="89e27-209">In der folgenden Liste werden die gültigen algorithmuswerte für die <a href="algorithm-name.md"><strong>Name</strong></a> -Eigenschaft angezeigt:</span><span class="sxs-lookup"><span data-stu-id="89e27-209">The following list shows the valid algorithm values for the <a href="algorithm-name.md"><strong>Name</strong></a> property:</span></span>
<ul>
<li><span data-ttu-id="89e27-210">CAPICOM_ENCRYPTION_ALGORITHM_RC2</span><span class="sxs-lookup"><span data-stu-id="89e27-210">CAPICOM_ENCRYPTION_ALGORITHM_RC2</span></span></li>
<li><span data-ttu-id="89e27-211">CAPICOM_ENCRYPTION_ALGORITHM_RC4</span><span class="sxs-lookup"><span data-stu-id="89e27-211">CAPICOM_ENCRYPTION_ALGORITHM_RC4</span></span></li>
<li><span data-ttu-id="89e27-212">CAPICOM_ENCRYPTION_ALGORITHM_DES</span><span class="sxs-lookup"><span data-stu-id="89e27-212">CAPICOM_ENCRYPTION_ALGORITHM_DES</span></span></li>
<li><span data-ttu-id="89e27-213">CAPICOM_ENCRYPTION_ALGORITHM_3DES</span><span class="sxs-lookup"><span data-stu-id="89e27-213">CAPICOM_ENCRYPTION_ALGORITHM_3DES</span></span></li>
</ul>
<br/></td>
<td><span data-ttu-id="89e27-214">0x80880270</span><span class="sxs-lookup"><span data-stu-id="89e27-214">0x80880270</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89e27-215"><strong>CAPICOM_E_INVALID_KEY_LENGTH</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-215"><strong>CAPICOM_E_INVALID_KEY_LENGTH</strong></span></span></td>
<td><span data-ttu-id="89e27-216">Der Wert für die Schlüssellänge der <a href="algorithm-keylength.md"><strong>keylength</strong></a> -Eigenschaft des <a href="algorithm.md"><strong>Algorithmusobjekts</strong></a> ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="89e27-216">The key length value for the <a href="algorithm-keylength.md"><strong>KeyLength</strong></a> property of the <a href="algorithm.md"><strong>Algorithm</strong></a> object is not valid.</span></span> <br/> <span data-ttu-id="89e27-217">In der folgenden Liste werden die gültigen Schlüssellängen Werte für die <a href="algorithm-keylength.md"><strong>keylength</strong></a> -Eigenschaft angezeigt:</span><span class="sxs-lookup"><span data-stu-id="89e27-217">The following list shows the valid key length values for the <a href="algorithm-keylength.md"><strong>KeyLength</strong></a> property:</span></span>
<ul>
<li><span data-ttu-id="89e27-218">CAPICOM_ENCRYPTION_KEY_LENGTH_MAXIMUM</span><span class="sxs-lookup"><span data-stu-id="89e27-218">CAPICOM_ENCRYPTION_KEY_LENGTH_MAXIMUM</span></span></li>
<li><span data-ttu-id="89e27-219">CAPICOM_ENCRYPTION_KEY_LENGTH_40_BITS</span><span class="sxs-lookup"><span data-stu-id="89e27-219">CAPICOM_ENCRYPTION_KEY_LENGTH_40_BITS</span></span></li>
<li><span data-ttu-id="89e27-220">CAPICOM_ENCRYPTION_KEY_LENGTH_56_BITS</span><span class="sxs-lookup"><span data-stu-id="89e27-220">CAPICOM_ENCRYPTION_KEY_LENGTH_56_BITS</span></span></li>
<li><span data-ttu-id="89e27-221">CAPICOM_ENCRYPTION_KEY_LENGTH_128_BITS</span><span class="sxs-lookup"><span data-stu-id="89e27-221">CAPICOM_ENCRYPTION_KEY_LENGTH_128_BITS</span></span></li>
</ul>
<br/></td>
<td><span data-ttu-id="89e27-222">0x80880271</span><span class="sxs-lookup"><span data-stu-id="89e27-222">0x80880271</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89e27-223"><strong>CAPICOM_E_ENVELOP_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-223"><strong>CAPICOM_E_ENVELOP_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="89e27-224">Das <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> -Objekt wurde nicht initialisiert.</span><span class="sxs-lookup"><span data-stu-id="89e27-224">The <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="89e27-225">Um das <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> -Objekt zu initialisieren, legen Sie entweder die <a href="envelopeddata-content.md"><strong>Content</strong></a> -Eigenschaft fest, oder nennen Sie die <a href="envelopeddata-decrypt.md"><strong>Entschlüsselungsmethode</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="89e27-225">To initialize the <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object, either set the <a href="envelopeddata-content.md"><strong>Content</strong></a> property or call the <a href="envelopeddata-decrypt.md"><strong>Decrypt</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="89e27-226">0x80880280</span><span class="sxs-lookup"><span data-stu-id="89e27-226">0x80880280</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89e27-227"><strong>CAPICOM_E_ENVELOP_INVALID_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-227"><strong>CAPICOM_E_ENVELOP_INVALID_TYPE</strong></span></span></td>
<td><span data-ttu-id="89e27-228">Das <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> -Objekt enthält einen ungültigen Typ.</span><span class="sxs-lookup"><span data-stu-id="89e27-228">The <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object contains a type that is not valid.</span></span> <br/> <span data-ttu-id="89e27-229">Dies geschieht normalerweise, wenn versucht wird, eine signierte Nachricht mit einem <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> -Objekt zu überprüfen, oder umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="89e27-229">Usually, this happens when an attempt is made to verify a signed message with an <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object or vice versa.</span></span><br/></td>
<td><span data-ttu-id="89e27-230">0x80880281</span><span class="sxs-lookup"><span data-stu-id="89e27-230">0x80880281</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89e27-231"><strong>CAPICOM_E_ENVELOP_NO_RECIPIENT</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-231"><strong>CAPICOM_E_ENVELOP_NO_RECIPIENT</strong></span></span></td>
<td><span data-ttu-id="89e27-232">Im <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> -Objekt ist kein Empfänger angegeben, wenn die <a href="envelopeddata-encrypt.md"><strong>Verschlüsselungs</strong></a> Methode eines <strong>EnvelopedData</strong> -Objekts aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="89e27-232">There is no recipient specified in the <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object when the <a href="envelopeddata-encrypt.md"><strong>Encrypt</strong></a> method of an <strong>EnvelopedData</strong> object is called.</span></span> <br/> <span data-ttu-id="89e27-233">Um einen Empfänger hinzuzufügen, müssen Sie die Methode " <a href="recipients-add.md"><strong>Empfängers. Add</strong></a> " aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="89e27-233">To add a recipient, call the <a href="recipients-add.md"><strong>Recipients.Add</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="89e27-234">0x80880282</span><span class="sxs-lookup"><span data-stu-id="89e27-234">0x80880282</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89e27-235"><strong>CAPICOM_E_ENVELOP_RECIPIENT_NOT_FOUND</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-235"><strong>CAPICOM_E_ENVELOP_RECIPIENT_NOT_FOUND</strong></span></span></td>
<td><span data-ttu-id="89e27-236">Der Empfänger kann nicht im <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> -Objekt gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="89e27-236">The recipient cannot be found in the <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object.</span></span> <br/> <span data-ttu-id="89e27-237">Dies geschieht in der Regel nicht mit einem <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> -Objekt, das von CAPICOM erstellt wurde. Wenn das <strong>EnvelopedData</strong> -Objekt jedoch von einem Drittanbieter Produkt erstellt wurde, ist das Zertifikat des Empfängers möglicherweise nicht in der PKCS-#7 Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="89e27-237">Usually, this does not happen with an <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object that was created by CAPICOM; however, if the <strong>EnvelopedData</strong> object was created by a third-party product, the recipient's certificate may not be included in the PKCS #7 structure.</span></span><br/></td>
<td><span data-ttu-id="89e27-238">0x80880283</span><span class="sxs-lookup"><span data-stu-id="89e27-238">0x80880283</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89e27-239"><strong>CAPICOM_E_ENCRYPT_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-239"><strong>CAPICOM_E_ENCRYPT_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="89e27-240">Das " <a href="encrypteddata.md"><strong>verschlüsselteddata</strong></a> "-Objekt wurde nicht initialisiert.</span><span class="sxs-lookup"><span data-stu-id="89e27-240">The <a href="encrypteddata.md"><strong>EncryptedData</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="89e27-241">Um das <a href="encrypteddata.md"><strong>verschlüsselteddata</strong></a> -Objekt zu initialisieren, legen Sie entweder die <a href="encrypteddata-content.md"><strong>Content</strong></a> -Eigenschaft fest, oder nennen Sie die <a href="encrypteddata-decrypt.md"><strong>Entschlüsselungsmethode</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="89e27-241">To initialize the <a href="encrypteddata.md"><strong>EncryptedData</strong></a> object, either set the <a href="encrypteddata-content.md"><strong>Content</strong></a> property or call the <a href="encrypteddata-decrypt.md"><strong>Decrypt</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="89e27-242">0x80880290</span><span class="sxs-lookup"><span data-stu-id="89e27-242">0x80880290</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89e27-243"><strong>CAPICOM_E_ENCRYPT_INVALID_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-243"><strong>CAPICOM_E_ENCRYPT_INVALID_TYPE</strong></span></span></td>
<td><span data-ttu-id="89e27-244">Das <a href="encrypteddata.md"><strong>verschlüsselteddata</strong></a> -Objekt ist kein gültiger Typ.</span><span class="sxs-lookup"><span data-stu-id="89e27-244">The <a href="encrypteddata.md"><strong>EncryptedData</strong></a> object is not a valid type.</span></span> <br/> <span data-ttu-id="89e27-245">In der Regel bedeutet dies, dass die Daten beschädigt sind.</span><span class="sxs-lookup"><span data-stu-id="89e27-245">Usually, this means the data is corrupted.</span></span><br/></td>
<td><span data-ttu-id="89e27-246">0x80880291</span><span class="sxs-lookup"><span data-stu-id="89e27-246">0x80880291</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89e27-247"><strong>CAPICOM_E_ENCRYPT_NO_SECRET</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-247"><strong>CAPICOM_E_ENCRYPT_NO_SECRET</strong></span></span></td>
<td><span data-ttu-id="89e27-248">Das Geheimnis eines <a href="encrypteddata.md"><strong>verschlüsselteddata</strong></a> -Objekts wurde nicht initialisiert.</span><span class="sxs-lookup"><span data-stu-id="89e27-248">The secret of an <a href="encrypteddata.md"><strong>EncryptedData</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="89e27-249">Um das Geheimnis eines <a href="encrypteddata.md"><strong>verschlüsselteddata</strong></a> -Objekts zu initialisieren, müssen Sie die <a href="encrypteddata-setsecret.md"><strong>setsecret</strong></a> -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="89e27-249">To initialize the secret of an <a href="encrypteddata.md"><strong>EncryptedData</strong></a> object, call the <a href="encrypteddata-setsecret.md"><strong>SetSecret</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="89e27-250">0x80880292</span><span class="sxs-lookup"><span data-stu-id="89e27-250">0x80880292</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89e27-251"><strong>CAPICOM_E_PRIVATE_KEY_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-251"><strong>CAPICOM_E_PRIVATE_KEY_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="89e27-252">Das <a href="privatekey.md"><strong>PrivateKey</strong></a> -Objekt wurde nicht initialisiert.</span><span class="sxs-lookup"><span data-stu-id="89e27-252">The <a href="privatekey.md"><strong>PrivateKey</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="89e27-253">0x80880300//v 2.0</span><span class="sxs-lookup"><span data-stu-id="89e27-253">0x80880300 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89e27-254"><strong>CAPICOM_E_PRIVATE_KEY_NOT_EXPORTABLE</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-254"><strong>CAPICOM_E_PRIVATE_KEY_NOT_EXPORTABLE</strong></span></span></td>
<td><span data-ttu-id="89e27-255">Das <a href="privatekey.md"><strong>PrivateKey</strong></a> -Objekt kann nicht exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="89e27-255">The <a href="privatekey.md"><strong>PrivateKey</strong></a> object cannot be exported.</span></span><br/></td>
<td><span data-ttu-id="89e27-256">0x80880301//v 2.0</span><span class="sxs-lookup"><span data-stu-id="89e27-256">0x80880301 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89e27-257"><strong>CAPICOM_E_ENCODE_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-257"><strong>CAPICOM_E_ENCODE_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="89e27-258">Das <a href="encodeddata.md"><strong>encoddata</strong></a> -Objekt wurde nicht initialisiert.</span><span class="sxs-lookup"><span data-stu-id="89e27-258">The <a href="encodeddata.md"><strong>EncodedData</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="89e27-259">0x80880320//v 2.0</span><span class="sxs-lookup"><span data-stu-id="89e27-259">0x80880320 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89e27-260"><strong>CAPICOM_E_EXTENSION_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-260"><strong>CAPICOM_E_EXTENSION_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="89e27-261">Das <a href="extension.md"><strong>Erweiterungs</strong></a> Objekt wurde nicht initialisiert.</span><span class="sxs-lookup"><span data-stu-id="89e27-261">The <a href="extension.md"><strong>Extension</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="89e27-262">0x80880330//v 2.0</span><span class="sxs-lookup"><span data-stu-id="89e27-262">0x80880330 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89e27-263"><strong>CAPICOM_E_PROPERTY_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-263"><strong>CAPICOM_E_PROPERTY_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="89e27-264">Die <a href="extendedproperty-propid.md"><strong>PROPID</strong></a> -Eigenschaft des <a href="extendedproperty.md"><strong>ExtendedProperty</strong></a> -Objekts wurde nicht initialisiert.</span><span class="sxs-lookup"><span data-stu-id="89e27-264">The <a href="extendedproperty-propid.md"><strong>PropID</strong></a> property of the <a href="extendedproperty.md"><strong>ExtendedProperty</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="89e27-265">0x80880340//v 2.0</span><span class="sxs-lookup"><span data-stu-id="89e27-265">0x80880340 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89e27-266"><strong>CAPICOM_E_FIND_INVALID_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-266"><strong>CAPICOM_E_FIND_INVALID_TYPE</strong></span></span></td>
<td><span data-ttu-id="89e27-267">Der <em>FindType</em> -Parameter der " <a href="certificates-find.md"><strong>Zertifikate. Find</strong></a> "-Methode ist kein Wert der <a href="capicom-certificate-find-type.md"><strong>CAPICOM_CERTIFICATE_FIND_TYPE</strong></a> -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="89e27-267">The <em>FindType</em> parameter of the <a href="certificates-find.md"><strong>Certificates.Find</strong></a> method is not a value of the <a href="capicom-certificate-find-type.md"><strong>CAPICOM_CERTIFICATE_FIND_TYPE</strong></a> enumeration.</span></span><br/></td>
<td><span data-ttu-id="89e27-268">0x80880350//v 2.0</span><span class="sxs-lookup"><span data-stu-id="89e27-268">0x80880350 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89e27-269"><strong>CAPICOM_E_FIND_INVALID_PREDEFINED_POLICY</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-269"><strong>CAPICOM_E_FIND_INVALID_PREDEFINED_POLICY</strong></span></span></td>
<td><span data-ttu-id="89e27-270">Die angegebene vordefinierte Richtlinie für den Suchvorgang ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="89e27-270">The specified predefined policy for the find operation is not valid.</span></span><br/></td>
<td><span data-ttu-id="89e27-271">0x80880351//v 2.0</span><span class="sxs-lookup"><span data-stu-id="89e27-271">0x80880351 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89e27-272"><strong>CAPICOM_E_CODE_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-272"><strong>CAPICOM_E_CODE_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="89e27-273">Das <a href="signedcode.md"><strong>signedcode</strong></a> -Objekt wurde nicht initialisiert.</span><span class="sxs-lookup"><span data-stu-id="89e27-273">The <a href="signedcode.md"><strong>SignedCode</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="89e27-274">0x80880360//v 2.0</span><span class="sxs-lookup"><span data-stu-id="89e27-274">0x80880360 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89e27-275"><strong>CAPICOM_E_CODE_NOT_SIGNED</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-275"><strong>CAPICOM_E_CODE_NOT_SIGNED</strong></span></span></td>
<td><span data-ttu-id="89e27-276">Das <a href="signedcode.md"><strong>signedcode</strong></a> -Objekt wurde nicht signiert.</span><span class="sxs-lookup"><span data-stu-id="89e27-276">The <a href="signedcode.md"><strong>SignedCode</strong></a> object has not been signed.</span></span><br/> <span data-ttu-id="89e27-277">Um das <a href="signedcode.md"><strong>signedcode</strong></a> -Objekt zu signieren, nennen Sie die <a href="signedcode-sign.md"><strong>Sign</strong></a> -Methode.</span><span class="sxs-lookup"><span data-stu-id="89e27-277">To sign the <a href="signedcode.md"><strong>SignedCode</strong></a> object, call the <a href="signedcode-sign.md"><strong>Sign</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="89e27-278">0x80880361//v 2.0</span><span class="sxs-lookup"><span data-stu-id="89e27-278">0x80880361 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89e27-279"><strong>CAPICOM_E_CODE_DESCRIPTION_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-279"><strong>CAPICOM_E_CODE_DESCRIPTION_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="89e27-280">Die <a href="signedcode-description.md"><strong>Description</strong></a> -Eigenschaft des <a href="signedcode.md"><strong>signedcode</strong></a> -Objekts wurde nicht initialisiert.</span><span class="sxs-lookup"><span data-stu-id="89e27-280">The <a href="signedcode-description.md"><strong>Description</strong></a> property of the <a href="signedcode.md"><strong>SignedCode</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="89e27-281">0x80880362//v 2.0</span><span class="sxs-lookup"><span data-stu-id="89e27-281">0x80880362 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89e27-282"><strong>CAPICOM_E_CODE_DESCRIPTION_URL_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-282"><strong>CAPICOM_E_CODE_DESCRIPTION_URL_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="89e27-283">Die <a href="signedcode-descriptionurl.md"><strong>DescriptionUrl</strong></a> -Eigenschaft des <a href="signedcode.md"><strong>signedcode</strong></a> -Objekts wurde nicht initialisiert.</span><span class="sxs-lookup"><span data-stu-id="89e27-283">The <a href="signedcode-descriptionurl.md"><strong>DescriptionURL</strong></a> property of the <a href="signedcode.md"><strong>SignedCode</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="89e27-284">0x80880363//v 2.0</span><span class="sxs-lookup"><span data-stu-id="89e27-284">0x80880363 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89e27-285"><strong>CAPICOM_E_CODE_INVALID_TIMESTAMP_URL</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-285"><strong>CAPICOM_E_CODE_INVALID_TIMESTAMP_URL</strong></span></span></td>
<td><span data-ttu-id="89e27-286">Der <em>URL</em> -Parameter der <a href="signedcode-timestamp.md"><strong>signedcode. Timestamp</strong></a> -Methode ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="89e27-286">The <em>URL</em> parameter of the <a href="signedcode-timestamp.md"><strong>SignedCode.Timestamp</strong></a> method is not valid.</span></span><br/></td>
<td><span data-ttu-id="89e27-287">0x80880364//v 2.0</span><span class="sxs-lookup"><span data-stu-id="89e27-287">0x80880364 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89e27-288"><strong>CAPICOM_E_HASH_NO_DATA</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-288"><strong>CAPICOM_E_HASH_NO_DATA</strong></span></span></td>
<td><span data-ttu-id="89e27-289">Das <a href="hasheddata.md"><strong>hashedData</strong></a> -Objekt enthält keine Daten.</span><span class="sxs-lookup"><span data-stu-id="89e27-289">The <a href="hasheddata.md"><strong>HashedData</strong></a> object does not contain any data.</span></span><br/></td>
<td><span data-ttu-id="89e27-290">0x80880370//v 2.0</span><span class="sxs-lookup"><span data-stu-id="89e27-290">0x80880370 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89e27-291"><strong>CAPICOM_E_INVALID_CONVERT_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-291"><strong>CAPICOM_E_INVALID_CONVERT_TYPE</strong></span></span></td>
<td><span data-ttu-id="89e27-292">Der Typ "Convert" ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="89e27-292">The convert type is not valid.</span></span><br/></td>
<td><span data-ttu-id="89e27-293">0x80880380//v 2.0</span><span class="sxs-lookup"><span data-stu-id="89e27-293">0x80880380 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89e27-294"><strong>CAPICOM_E_NOT_SUPPORTED</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-294"><strong>CAPICOM_E_NOT_SUPPORTED</strong></span></span></td>
<td><span data-ttu-id="89e27-295">Der angeforderte Vorgang wird von der aktuellen Plattform nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="89e27-295">The requested operation is not supported in the current platform.</span></span> <br/></td>
<td><span data-ttu-id="89e27-296">0x80880900</span><span class="sxs-lookup"><span data-stu-id="89e27-296">0x80880900</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89e27-297"><strong>CAPICOM_E_UI_DISABLED</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-297"><strong>CAPICOM_E_UI_DISABLED</strong></span></span></td>
<td><span data-ttu-id="89e27-298">Beim Signieren wurde die <a href="signer-certificate.md"><strong>Certificate</strong></a> -Eigenschaft des <a href="signer.md"><strong>Signatur</strong></a> Geber Objekts nicht festgelegt, aber die Eingabeaufforderung für das Benutzerzertifikat wurde deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="89e27-298">When signing, the <a href="signer-certificate.md"><strong>Certificate</strong></a> property of the <a href="signer.md"><strong>Signer</strong></a> object has not been set, but the prompt for the user certificate has been disabled.</span></span> <br/> <span data-ttu-id="89e27-299">Aktivieren Sie entweder die Eingabeaufforderung, indem Sie die <a href="settings-enablepromptforcertificateui.md"><strong>enablepromptforcertifitoreui</strong></a> -Eigenschaft des <a href="settings.md"><strong>Settings</strong></a> -Objekts festlegen, oder legen Sie die <a href="signer-certificate.md"><strong>Certificate</strong></a> -Eigenschaft des <a href="signer.md"><strong>Signatur</strong></a> Geber Objekts fest.</span><span class="sxs-lookup"><span data-stu-id="89e27-299">Either enable the prompt by setting the <a href="settings-enablepromptforcertificateui.md"><strong>EnablePromptForCertificateUI</strong></a> property of the <a href="settings.md"><strong>Settings</strong></a> object, or set the <a href="signer-certificate.md"><strong>Certificate</strong></a> property of the <a href="signer.md"><strong>Signer</strong></a> object.</span></span><br/></td>
<td><span data-ttu-id="89e27-300">0x80880901</span><span class="sxs-lookup"><span data-stu-id="89e27-300">0x80880901</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89e27-301"><strong>CAPICOM_E_CANCELLED</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-301"><strong>CAPICOM_E_CANCELLED</strong></span></span></td>
<td><span data-ttu-id="89e27-302">Der Vorgang wurde vom Benutzer abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="89e27-302">The operation has been canceled by the user.</span></span> <br/> <span data-ttu-id="89e27-303">Dies geschieht, wenn der Benutzer aufgefordert wird, eine Berechtigung zum Ausführen eines bestimmten Vorgangs zu erhalten, z. b. den Zugriff auf den privaten Schlüssel, und der Benutzer den Vorgang abbricht.</span><span class="sxs-lookup"><span data-stu-id="89e27-303">This happens when the user is prompted for permission to carry out a certain operation, such as accessing the private key, and the user cancels the operation.</span></span><br/></td>
<td><span data-ttu-id="89e27-304">0x80880902</span><span class="sxs-lookup"><span data-stu-id="89e27-304">0x80880902</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89e27-305"><strong>CAPICOM_E_NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-305"><strong>CAPICOM_E_NOT_ALLOWED</strong></span></span></td>
<td><span data-ttu-id="89e27-306">Der versuchte Vorgang ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="89e27-306">The attempted operation is not allowed.</span></span><br/> <span data-ttu-id="89e27-307">Beispielsweise ist das Ändern der <a href="extendedproperty-propid.md"><strong>PROPID</strong></a> -Eigenschaft eines <a href="extendedproperty.md"><strong>ExtendedProperty</strong></a> -Objekts nicht zulässig, wenn das Objekt an ein Zertifikat angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="89e27-307">For example, changing the <a href="extendedproperty-propid.md"><strong>PropID</strong></a> property of an <a href="extendedproperty.md"><strong>ExtendedProperty</strong></a> object is not allowed if the object is attached to a certificate.</span></span><br/></td>
<td><span data-ttu-id="89e27-308">0x80880903//v 2.0</span><span class="sxs-lookup"><span data-stu-id="89e27-308">0x80880903 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89e27-309"><strong>CAPICOM_E_OUT_OF_RESOURCE</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-309"><strong>CAPICOM_E_OUT_OF_RESOURCE</strong></span></span></td>
<td><span data-ttu-id="89e27-310">Für CAPICOM steht eine Ressource aus.</span><span class="sxs-lookup"><span data-stu-id="89e27-310">CAPICOM has run out of a resource.</span></span><br/></td>
<td><span data-ttu-id="89e27-311">0x80880904//v 2.0</span><span class="sxs-lookup"><span data-stu-id="89e27-311">0x80880904 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89e27-312"><strong>CAPICOM_E_INTERNAL</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-312"><strong>CAPICOM_E_INTERNAL</strong></span></span></td>
<td><span data-ttu-id="89e27-313">Ein interner Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="89e27-313">An internal error has occurred.</span></span> <br/> <span data-ttu-id="89e27-314">Wenden Sie sich an den technischen Support von Microsoft.</span><span class="sxs-lookup"><span data-stu-id="89e27-314">Contact Microsoft Technical Support for assistance.</span></span><br/></td>
<td><span data-ttu-id="89e27-315">0x80880911</span><span class="sxs-lookup"><span data-stu-id="89e27-315">0x80880911</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89e27-316"><strong>CAPICOM_E_UNKNOWN</strong></span><span class="sxs-lookup"><span data-stu-id="89e27-316"><strong>CAPICOM_E_UNKNOWN</strong></span></span></td>
<td><span data-ttu-id="89e27-317">Ein unbekannter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="89e27-317">An unknown error has occurred.</span></span> <br/> <span data-ttu-id="89e27-318">Sammeln Sie so viele Informationen wie möglich, und wenden Sie sich an den Hersteller.</span><span class="sxs-lookup"><span data-stu-id="89e27-318">Collect as much information as possible, and contact your vendor.</span></span><br/></td>
<td><span data-ttu-id="89e27-319">0x80880999</span><span class="sxs-lookup"><span data-stu-id="89e27-319">0x80880999</span></span></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="89e27-320">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="89e27-320">Requirements</span></span>



| <span data-ttu-id="89e27-321">Anforderung</span><span class="sxs-lookup"><span data-stu-id="89e27-321">Requirement</span></span> | <span data-ttu-id="89e27-322">Wert</span><span class="sxs-lookup"><span data-stu-id="89e27-322">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="89e27-323">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="89e27-323">Redistributable</span></span><br/> | <span data-ttu-id="89e27-324">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="89e27-324">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="89e27-325">Header</span><span class="sxs-lookup"><span data-stu-id="89e27-325">Header</span></span><br/>          | <dl> <span data-ttu-id="89e27-326"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="89e27-326"><dt>Capicom.h</dt></span></span> </dl> |



 

 




