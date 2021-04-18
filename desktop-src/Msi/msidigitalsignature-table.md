---
description: Die msidigitalsignature-Tabelle enthält die Signatur Informationen für jedes Digital signierte Objekt in der Installations Datenbank.
ms.assetid: 63d62152-4f01-454f-bdea-550f2a9f6b14
title: Msidigitalsignature-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0ec22b9a399b6248fd3b2781e1ac8d7ae14324
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368245"
---
# <a name="msidigitalsignature-table"></a><span data-ttu-id="8a27b-103">Msidigitalsignature-Tabelle</span><span class="sxs-lookup"><span data-stu-id="8a27b-103">MsiDigitalSignature Table</span></span>

<span data-ttu-id="8a27b-104">Die msidigitalsignature-Tabelle enthält die Signatur Informationen für jedes Digital signierte Objekt in der Installations Datenbank.</span><span class="sxs-lookup"><span data-stu-id="8a27b-104">The MsiDigitalSignature table contains the signature information for every digitally signed object in the installation database.</span></span>

<span data-ttu-id="8a27b-105">Die Tabellen msidigitalsignature und [msidigitalcertificate](msidigitalcertificate-table.md) sind ab Windows Installer Version 2,0 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8a27b-105">The MsiDigitalSignature and [MsiDigitalCertificate](msidigitalcertificate-table.md) tables are available starting with Windows Installer version 2.0.</span></span>

<span data-ttu-id="8a27b-106">Windows Installer Version kann digitale Signaturen als Mittel zum erkennen beschädigter Ressourcen verwenden.</span><span class="sxs-lookup"><span data-stu-id="8a27b-106">Windows Installer version can use digital signatures as a means to detect corrupted resources.</span></span> <span data-ttu-id="8a27b-107">In Windows Installer 2,0 können nur die digitalen Signaturen externer Schränke und nur die Verwendung der Tabellen msidigitalsignature und [msidigitalcertificate](msidigitalcertificate-table.md) überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="8a27b-107">Windows Installer 2.0 can only verify the digital signatures of external cabinets, and only by the use of the MsiDigitalSignature and [MsiDigitalCertificate](msidigitalcertificate-table.md) tables.</span></span>

<span data-ttu-id="8a27b-108">Ab Windows Installer 3,0 kann der Windows Installer die digitalen Signaturen von Patches (MSP-Dateien) mithilfe der [MsiPatchCertificate](msipatchcertificate-table.md) -und msidigitalcertificate-Tabellen überprüfen.</span><span class="sxs-lookup"><span data-stu-id="8a27b-108">Beginning with Windows Installer 3.0, the Windows Installer can verify the digital signatures of patches (.msp files) by using the [MsiPatchCertificate](msipatchcertificate-table.md) and MsiDigitalCertificate tables.</span></span> <span data-ttu-id="8a27b-109">Weitere Informationen finden Sie unter [Richtlinien zum Erstellen von sicheren Installationen](guidelines-for-authoring-secure-installations.md) und zum [Patchen von Benutzerkontensteuerung (User Account Control, UAC)](user-account-control--uac--patching.md).</span><span class="sxs-lookup"><span data-stu-id="8a27b-109">For more information, see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and [User Account Control (UAC) Patching](user-account-control--uac--patching.md).</span></span>

<span data-ttu-id="8a27b-110">Die msidigitalsignature-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="8a27b-110">The MsiDigitalSignature table has the following columns.</span></span>



| <span data-ttu-id="8a27b-111">Spalte</span><span class="sxs-lookup"><span data-stu-id="8a27b-111">Column</span></span>               | <span data-ttu-id="8a27b-112">Typ</span><span class="sxs-lookup"><span data-stu-id="8a27b-112">Type</span></span>                         | <span data-ttu-id="8a27b-113">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="8a27b-113">Key</span></span> | <span data-ttu-id="8a27b-114">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="8a27b-114">Nullable</span></span> |
|----------------------|------------------------------|-----|----------|
| <span data-ttu-id="8a27b-115">Tabelle</span><span class="sxs-lookup"><span data-stu-id="8a27b-115">Table</span></span>                | [<span data-ttu-id="8a27b-116">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="8a27b-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="8a27b-117">J</span><span class="sxs-lookup"><span data-stu-id="8a27b-117">Y</span></span>   | <span data-ttu-id="8a27b-118">N</span><span class="sxs-lookup"><span data-stu-id="8a27b-118">N</span></span>        |
| <span data-ttu-id="8a27b-119">Signobject</span><span class="sxs-lookup"><span data-stu-id="8a27b-119">SignObject</span></span>           | [<span data-ttu-id="8a27b-120">Text</span><span class="sxs-lookup"><span data-stu-id="8a27b-120">Text</span></span>](text.md)             | <span data-ttu-id="8a27b-121">J</span><span class="sxs-lookup"><span data-stu-id="8a27b-121">Y</span></span>   | <span data-ttu-id="8a27b-122">N</span><span class="sxs-lookup"><span data-stu-id="8a27b-122">N</span></span>        |
| <span data-ttu-id="8a27b-123">Digitalcertificate\_</span><span class="sxs-lookup"><span data-stu-id="8a27b-123">DigitalCertificate\_</span></span> | [<span data-ttu-id="8a27b-124">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="8a27b-124">Identifier</span></span>](identifier.md) | <span data-ttu-id="8a27b-125">N</span><span class="sxs-lookup"><span data-stu-id="8a27b-125">N</span></span>   | <span data-ttu-id="8a27b-126">N</span><span class="sxs-lookup"><span data-stu-id="8a27b-126">N</span></span>        |
| <span data-ttu-id="8a27b-127">Hash</span><span class="sxs-lookup"><span data-stu-id="8a27b-127">Hash</span></span>                 | [<span data-ttu-id="8a27b-128">Binär (Binary)</span><span class="sxs-lookup"><span data-stu-id="8a27b-128">Binary</span></span>](binary.md)         | <span data-ttu-id="8a27b-129">N</span><span class="sxs-lookup"><span data-stu-id="8a27b-129">N</span></span>   | <span data-ttu-id="8a27b-130">J</span><span class="sxs-lookup"><span data-stu-id="8a27b-130">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="8a27b-131">Spalten</span><span class="sxs-lookup"><span data-stu-id="8a27b-131">Columns</span></span>

<dl> <dt>

<span data-ttu-id="8a27b-132"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Glaub</span><span class="sxs-lookup"><span data-stu-id="8a27b-132"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="8a27b-133">Bei der Windows Installer Version 2,0 muss der Eintrag in diesem Feld für die [Medien Tabelle](media-table.md)"Media" lauten.</span><span class="sxs-lookup"><span data-stu-id="8a27b-133">With the Windows Installer version 2.0, the entry in this field must be "Media" for the [Media table](media-table.md).</span></span> <span data-ttu-id="8a27b-134">Das Installationsprogramm überprüft nur die digitalen Signaturen auf externen CAB-Medien Einträgen.</span><span class="sxs-lookup"><span data-stu-id="8a27b-134">The installer only verifies the digital signatures on external cabinet media entries.</span></span> <span data-ttu-id="8a27b-135">Diese Spalte und die signobject-Spalte geben die Ressource an, die digital signiert ist.</span><span class="sxs-lookup"><span data-stu-id="8a27b-135">This column and the SignObject column together specify the resource that is digitally signed.</span></span>

</dd> <dt>

<span data-ttu-id="8a27b-136"><span id="SignObject"></span><span id="signobject"></span><span id="SIGNOBJECT"></span>Signobject</span><span class="sxs-lookup"><span data-stu-id="8a27b-136"><span id="SignObject"></span><span id="signobject"></span><span id="SIGNOBJECT"></span>SignObject</span></span>
</dt> <dd>

<span data-ttu-id="8a27b-137">Ein Fremdschlüssel in den Primärschlüssel der Tabelle, der in der Tabellenspalte angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="8a27b-137">A foreign key into the primary key of the table specified by the Table column.</span></span> <span data-ttu-id="8a27b-138">In dieser Spalte und der Tabellenspalte wird die Ressource, die digital signiert ist, in der Spalte angegeben.</span><span class="sxs-lookup"><span data-stu-id="8a27b-138">This column and the Table column together specify the resource that is digitally signed.</span></span>

</dd> <dt>

<span data-ttu-id="8a27b-139"><span id="DigitalCertificate_"></span><span id="digitalcertificate_"></span><span id="DIGITALCERTIFICATE_"></span>Digitalcertificate\_</span><span class="sxs-lookup"><span data-stu-id="8a27b-139"><span id="DigitalCertificate_"></span><span id="digitalcertificate_"></span><span id="DIGITALCERTIFICATE_"></span>DigitalCertificate\_</span></span>
</dt> <dd>

<span data-ttu-id="8a27b-140">Ein Fremdschlüssel in die [msidigitalcertificate-Tabelle](msidigitalcertificate-table.md).</span><span class="sxs-lookup"><span data-stu-id="8a27b-140">A foreign key into the [MsiDigitalCertificate table](msidigitalcertificate-table.md).</span></span> <span data-ttu-id="8a27b-141">Dadurch wird das Zertifikat identifiziert, das in der Datei vorhanden sein muss, damit die zugeordnete Aktion erfolgreich ausgeführt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="8a27b-141">This identifies the certificate that must exist on the file for the associated action to succeed.</span></span> <span data-ttu-id="8a27b-142">Die Ressource (oder das Objekt) muss immer mit diesem Zertifikat in der Tabelle "msidigitalcertificate" abgeglichen werden.</span><span class="sxs-lookup"><span data-stu-id="8a27b-142">The resource (or object) is always required to match this certificate in the MsiDigitalCertificate table.</span></span>

</dd> <dt>

<span data-ttu-id="8a27b-143"><span id="Hash"></span><span id="hash"></span><span id="HASH"></span>Hash</span><span class="sxs-lookup"><span data-stu-id="8a27b-143"><span id="Hash"></span><span id="hash"></span><span id="HASH"></span>Hash</span></span>
</dt> <dd>

<span data-ttu-id="8a27b-144">Geben Sie in diesem Feld den Verweis Hash der Ressource (oder des Objekts) ein, die mit dem tatsächlichen Hash der Ressource (oder des Objekts) überprüft werden soll, die zur Laufzeit abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="8a27b-144">In this field enter the reference hash of the resource (or object) that is to be checked against the actual hash of the resource (or object) obtained at run-time.</span></span> <span data-ttu-id="8a27b-145">Wenn nur das Zertifikat überprüft werden muss, ist das hashfeld möglicherweise NULL.</span><span class="sxs-lookup"><span data-stu-id="8a27b-145">If only the certificate needs to be verified, the Hash field may be null.</span></span> <span data-ttu-id="8a27b-146">Beachten Sie, dass das Format des Hashs abhängig vom Typ der zu Signier enden Ressource (oder des Objekts) ist.</span><span class="sxs-lookup"><span data-stu-id="8a27b-146">Note that the format of the hash depends on the type of the resource (or object) being signed.</span></span>

<span data-ttu-id="8a27b-147">Die Hash Spalte enthält die binäre Darstellung des Hashs.</span><span class="sxs-lookup"><span data-stu-id="8a27b-147">The Hash column contains the binary representation of the hash.</span></span> <span data-ttu-id="8a27b-148">Der tatsächliche Inhalt ist der **pbData** -Member der [**crypt- \_ Hash- \_ blobstruktur**](/windows/win32/api/dpapi/ns-dpapi-crypt_integer_blob) , der Teil der **CryptoAPI- \_ BLOB** -Struktur ist.</span><span class="sxs-lookup"><span data-stu-id="8a27b-148">The actual content is the **pbData** member of the [**CRYPT\_HASH\_BLOB**](/windows/win32/api/dpapi/ns-dpapi-crypt_integer_blob) structure, which is part of the **CRYPTOAPI\_BLOB** structure.</span></span> <span data-ttu-id="8a27b-149">Dies kann durch Aufrufen von [WinVerifyTrust](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) oder [**msigetfilesignatureinformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)erreicht werden.</span><span class="sxs-lookup"><span data-stu-id="8a27b-149">This may be obtained by calling [WinVerifyTrust](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) or [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa).</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="8a27b-150">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="8a27b-150">Validation</span></span>

<dl>

[<span data-ttu-id="8a27b-151">ICE03</span><span class="sxs-lookup"><span data-stu-id="8a27b-151">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="8a27b-152">ICE06</span><span class="sxs-lookup"><span data-stu-id="8a27b-152">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="8a27b-153">ICE29</span><span class="sxs-lookup"><span data-stu-id="8a27b-153">ICE29</span></span>](ice29.md)  
[<span data-ttu-id="8a27b-154">ICE32</span><span class="sxs-lookup"><span data-stu-id="8a27b-154">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="8a27b-155">ICE66</span><span class="sxs-lookup"><span data-stu-id="8a27b-155">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="8a27b-156">ICE81</span><span class="sxs-lookup"><span data-stu-id="8a27b-156">ICE81</span></span>](ice81.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="8a27b-157">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8a27b-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a27b-158">**Msigetfilesignatureinformation**</span><span class="sxs-lookup"><span data-stu-id="8a27b-158">**MsiGetFileSignatureInformation**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)
</dt> <dt>

[<span data-ttu-id="8a27b-159">Msidigitalcertificate-Tabelle</span><span class="sxs-lookup"><span data-stu-id="8a27b-159">MsiDigitalCertificate table</span></span>](msidigitalcertificate-table.md)
</dt> <dt>

[<span data-ttu-id="8a27b-160">Digitale Signaturen und Windows Installer</span><span class="sxs-lookup"><span data-stu-id="8a27b-160">Digital Signatures and Windows Installer</span></span>](digital-signatures-and-windows-installer.md)
</dt> </dl>

 

 
