---
description: Stellt Eigenschaften und Methoden bereit, die Sie verwenden können, um Zertifikat Speicher und die Zertifikate in diesen speichern auszuwählen, zu verwalten und zu verwenden.
ms.assetid: de4eecf7-c03b-4733-ac29-d5b26b873dba
title: Store-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4e8a14fcecf0ded2e4e1a56e2b98e4ac4838b776
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355962"
---
# <a name="store-object"></a><span data-ttu-id="29a5a-103">Store-Objekt</span><span class="sxs-lookup"><span data-stu-id="29a5a-103">Store object</span></span>

<span data-ttu-id="29a5a-104">\[Das **Store** -Objekt ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="29a5a-104">\[The **Store** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="29a5a-105">Verwenden Sie stattdessen die [**X509Store-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="29a5a-105">Instead, use the [**X509Store Class**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="29a5a-106">Das **Store** -Objekt stellt Eigenschaften und Methoden bereit, die Sie verwenden können, um [*Zertifikat Speicher*](../secgloss/c-gly.md) und die Zertifikate in diesen speichern auszuwählen, zu verwalten und zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="29a5a-106">The **Store** object provides properties and methods that you can use to choose, manage, and use [*certificate stores*](../secgloss/c-gly.md) and the certificates in those stores.</span></span> <span data-ttu-id="29a5a-107">CAPICOM kann aktuelle Benutzer-, lokale Computer-, Speicher-und Active Directory Speicher verwenden.</span><span class="sxs-lookup"><span data-stu-id="29a5a-107">CAPICOM can use Current-User, Local-Machine, memory, and Active Directory stores.</span></span> <span data-ttu-id="29a5a-108">Speichert auch Smartcard – basierte Zertifikat Speicher.</span><span class="sxs-lookup"><span data-stu-id="29a5a-108">Also, stores support smart card–based certificate stores.</span></span> <span data-ttu-id="29a5a-109">Entwickler sollten sich bewusst sein, dass einige Methoden möglicherweise mit einigen speichern fehlschlagen, wenn versucht wird, einen Vorgang auszuführen, für den der Benutzer keine Rechte hat.</span><span class="sxs-lookup"><span data-stu-id="29a5a-109">Developers should be aware that some methods may fail with some stores if operations are attempted for which the user does not have rights.</span></span>

## <a name="members"></a><span data-ttu-id="29a5a-110">Member</span><span class="sxs-lookup"><span data-stu-id="29a5a-110">Members</span></span>

<span data-ttu-id="29a5a-111">Das **Store** -Objekt verfügt über folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="29a5a-111">The **Store** object has these types of members:</span></span>

-   [<span data-ttu-id="29a5a-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="29a5a-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="29a5a-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="29a5a-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="29a5a-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="29a5a-114">Methods</span></span>

<span data-ttu-id="29a5a-115">Das **Store** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="29a5a-115">The **Store** object has these methods.</span></span>



| <span data-ttu-id="29a5a-116">Methode</span><span class="sxs-lookup"><span data-stu-id="29a5a-116">Method</span></span>                         | <span data-ttu-id="29a5a-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="29a5a-117">Description</span></span>                                                                                                                                                                                                      |
|:-------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="29a5a-118">**Eren**</span><span class="sxs-lookup"><span data-stu-id="29a5a-118">**Add**</span></span>](store-add.md)       | <span data-ttu-id="29a5a-119">Fügt dem geöffneten Zertifikat Speicher ein [**Zertifikat**](certificate.md) Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="29a5a-119">Adds a [**Certificate**](certificate.md) object to the open certificate store.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="29a5a-120">**Schließen**</span><span class="sxs-lookup"><span data-stu-id="29a5a-120">**Close**</span></span>](store-close.md)   | <span data-ttu-id="29a5a-121">Schließt einen geöffneten Zertifikat Speicher.</span><span class="sxs-lookup"><span data-stu-id="29a5a-121">Closes an open certificate store.</span></span><br/> <span data-ttu-id="29a5a-122">**CAPICOM 2.0.0.3 und früher:** Die [**Close**](store-close.md) -Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="29a5a-122">**CAPICOM 2.0.0.3 and earlier:** The [**Close**](store-close.md) method is not supported.</span></span><br/>                                                               |
| [<span data-ttu-id="29a5a-123">**Lösch**</span><span class="sxs-lookup"><span data-stu-id="29a5a-123">**Delete**</span></span>](store-delete.md) | <span data-ttu-id="29a5a-124">Löscht den Zertifikat Speicher, der durch das aktuelle [**Speicher**](certificate.md) Objekt dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="29a5a-124">Deletes the certificate store represented by the current [**Store**](certificate.md) object.</span></span><br/> <span data-ttu-id="29a5a-125">**CAPICOM 2.0.0.3 und früher:** Die [**Delete**](store-delete.md) -Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="29a5a-125">**CAPICOM 2.0.0.3 and earlier:** The [**Delete**](store-delete.md) method is not supported.</span></span><br/> |
| [<span data-ttu-id="29a5a-126">**Exportieren**</span><span class="sxs-lookup"><span data-stu-id="29a5a-126">**Export**</span></span>](store-export.md) | <span data-ttu-id="29a5a-127">Exportiert den Speicher eines codierten [*BLOBs*](../secgloss/b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="29a5a-127">Exports the store of an encoded [*BLOB*](../secgloss/b-gly.md).</span></span><br/>                                                                                                       |
| [<span data-ttu-id="29a5a-128">**Importieren**</span><span class="sxs-lookup"><span data-stu-id="29a5a-128">**Import**</span></span>](store-import.md) | <span data-ttu-id="29a5a-129">Importiert einen zuvor exportierten Speicher.</span><span class="sxs-lookup"><span data-stu-id="29a5a-129">Imports a previously exported store.</span></span><br/>                                                                                                                                                                  |
| [<span data-ttu-id="29a5a-130">**Laden**</span><span class="sxs-lookup"><span data-stu-id="29a5a-130">**Load**</span></span>](store-load.md)     | <span data-ttu-id="29a5a-131">Importiert [**Zertifikat**](certificate.md) Objekte aus einer Datei in den Speicher.</span><span class="sxs-lookup"><span data-stu-id="29a5a-131">Imports [**Certificate**](certificate.md) objects from a file into the store.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="29a5a-132">**Eren**</span><span class="sxs-lookup"><span data-stu-id="29a5a-132">**Open**</span></span>](store-open.md)     | <span data-ttu-id="29a5a-133">Öffnet einen Zertifikat Speicher.</span><span class="sxs-lookup"><span data-stu-id="29a5a-133">Opens a certificate store.</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="29a5a-134">**Aufgeh**</span><span class="sxs-lookup"><span data-stu-id="29a5a-134">**Remove**</span></span>](store-remove.md) | <span data-ttu-id="29a5a-135">Entfernt ein [**Zertifikat**](certificate.md) Objekt aus einem geöffneten Speicher.</span><span class="sxs-lookup"><span data-stu-id="29a5a-135">Removes a [**Certificate**](certificate.md) object from an open store.</span></span><br/>                                                                                                                               |



 

### <a name="properties"></a><span data-ttu-id="29a5a-136">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="29a5a-136">Properties</span></span>

<span data-ttu-id="29a5a-137">Das **Store** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="29a5a-137">The **Store** object has these properties.</span></span>



| <span data-ttu-id="29a5a-138">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="29a5a-138">Property</span></span>                                              | <span data-ttu-id="29a5a-139">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="29a5a-139">Access type</span></span>          | <span data-ttu-id="29a5a-140">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="29a5a-140">Description</span></span>                                                                                                                                                                                           |
|:------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="29a5a-141">**Zertifikate**</span><span class="sxs-lookup"><span data-stu-id="29a5a-141">**Certificates**</span></span>](store-certificates.md)<br/> | <span data-ttu-id="29a5a-142">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="29a5a-142">Read-only</span></span><br/> | <span data-ttu-id="29a5a-143">Ruft die [**Zertifikats**](certificates.md) Sammlung des Stores ab.</span><span class="sxs-lookup"><span data-stu-id="29a5a-143">Retrieves the [**Certificates**](certificates.md) collection of the store.</span></span> <span data-ttu-id="29a5a-144">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="29a5a-144">This is the default property.</span></span><br/>                                                                                  |
| [<span data-ttu-id="29a5a-145">**Hotels**</span><span class="sxs-lookup"><span data-stu-id="29a5a-145">**Location**</span></span>](store-location.md)<br/>         | <span data-ttu-id="29a5a-146">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="29a5a-146">Read-only</span></span><br/> | <span data-ttu-id="29a5a-147">Ruft den Speicherort des Zertifikat Speicher ab, der von diesem-Objekt dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="29a5a-147">Retrieves the location of the certificate store that this object represents.</span></span><br/> <span data-ttu-id="29a5a-148">**CAPICOM 2.0.0.3 und früher:** Die [**Location**](store-location.md) -Eigenschaft wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="29a5a-148">**CAPICOM 2.0.0.3 and earlier:** The [**Location**](store-location.md) property is not supported.</span></span><br/> |
| [<span data-ttu-id="29a5a-149">**Name**</span><span class="sxs-lookup"><span data-stu-id="29a5a-149">**Name**</span></span>](store-name.md)<br/>                 | <span data-ttu-id="29a5a-150">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="29a5a-150">Read-only</span></span><br/> | <span data-ttu-id="29a5a-151">Ruft den Namen des Zertifikat Speicher ab, der von diesem-Objekt dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="29a5a-151">Retrieves the name of the certificate store that this object represents.</span></span><br/> <span data-ttu-id="29a5a-152">**CAPICOM 2.0.0.3 und früher:** Die [**Name**](store-name.md) -Eigenschaft wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="29a5a-152">**CAPICOM 2.0.0.3 and earlier:** The [**Name**](store-name.md) property is not supported.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="29a5a-153">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="29a5a-153">Remarks</span></span>

<span data-ttu-id="29a5a-154">Das **Store** -Objekt kann erstellt werden und ist für die Skripterstellung sicher.</span><span class="sxs-lookup"><span data-stu-id="29a5a-154">The **Store** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="29a5a-155">Die ProgID für das **Speicher** Objekt ist CAPICOM. Store. 2.</span><span class="sxs-lookup"><span data-stu-id="29a5a-155">The ProgID for the **Store** object is CAPICOM.Store.2.</span></span>

<span data-ttu-id="29a5a-156">**CAPICOM 1. *x*:** die ProgID für das **Speicher** Objekt ist CAPICOM. Store. 1.</span><span class="sxs-lookup"><span data-stu-id="29a5a-156">**CAPICOM 1.*x*:** The ProgID for the **Store** object is CAPICOM.Store.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="29a5a-157">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29a5a-157">Requirements</span></span>



| <span data-ttu-id="29a5a-158">Anforderung</span><span class="sxs-lookup"><span data-stu-id="29a5a-158">Requirement</span></span> | <span data-ttu-id="29a5a-159">Wert</span><span class="sxs-lookup"><span data-stu-id="29a5a-159">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="29a5a-160">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="29a5a-160">Redistributable</span></span><br/> | <span data-ttu-id="29a5a-161">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="29a5a-161">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="29a5a-162">DLL</span><span class="sxs-lookup"><span data-stu-id="29a5a-162">DLL</span></span><br/>             | <dl> <span data-ttu-id="29a5a-163"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29a5a-163"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29a5a-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29a5a-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29a5a-165">**Kryptografieobjekte**</span><span class="sxs-lookup"><span data-stu-id="29a5a-165">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
