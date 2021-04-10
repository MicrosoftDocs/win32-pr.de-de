---
description: Die msidigitalcertificate-Tabelle speichert Zertifikate im binären Streamformat und ordnet jedes Zertifikat einem Primärschlüssel zu.
ms.assetid: 834534b8-540a-48c2-8eb0-3511d5a20cb4
title: Msidigitalcertificate-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff4765dee433cfab989e79c7ef4663d8939381ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755416"
---
# <a name="msidigitalcertificate-table"></a><span data-ttu-id="087f7-103">Msidigitalcertificate-Tabelle</span><span class="sxs-lookup"><span data-stu-id="087f7-103">MsiDigitalCertificate Table</span></span>

<span data-ttu-id="087f7-104">Die msidigitalcertificate-Tabelle speichert Zertifikate im binären Streamformat und ordnet jedes Zertifikat einem Primärschlüssel zu.</span><span class="sxs-lookup"><span data-stu-id="087f7-104">The MsiDigitalCertificate table stores certificates in binary stream format and associates each certificate with a primary key.</span></span> <span data-ttu-id="087f7-105">Der Primärschlüssel wird zum Freigeben von Zertifikaten für mehrere Digital signierte Objekte verwendet.</span><span class="sxs-lookup"><span data-stu-id="087f7-105">The primary key is used to share certificates among multiple digitally signed objects.</span></span> <span data-ttu-id="087f7-106">Ein digitales Zertifikat ist eine Anmelde Information, die eine Möglichkeit zum Überprüfen der Identität bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="087f7-106">A digital certificate is a credential that provides a means to verify identity.</span></span> <span data-ttu-id="087f7-107">Weitere Informationen finden Sie im Abschnitt zur [Kryptografie](../seccrypto/cryptography-portal.md) [im Microsoft](../seccrypto/digital-certificates.md) Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="087f7-107">For more information, see [Digital Certificates](../seccrypto/digital-certificates.md) in the [Cryptography](../seccrypto/cryptography-portal.md) section of the Microsoft Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="087f7-108">Die Tabellen [msidigitalsignature](msidigitalsignature-table.md) und msidigitalcertificate sind ab Windows Installer Version 2,0 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="087f7-108">The [MsiDigitalSignature](msidigitalsignature-table.md) and MsiDigitalCertificate tables are available starting with Windows Installer version 2.0.</span></span>

<span data-ttu-id="087f7-109">Windows Installer können digitale Signaturen als Mittel zum erkennen beschädigter Ressourcen verwenden.</span><span class="sxs-lookup"><span data-stu-id="087f7-109">Windows Installer can use digital signatures as a means to detect corrupted resources.</span></span> <span data-ttu-id="087f7-110">In Windows Installer Version 2,0 können nur die digitalen Signaturen externer Schränke und nur die Verwendung der Tabellen [msidigitalsignature](msidigitalsignature-table.md) und msidigitalcertificate überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="087f7-110">Windows Installer version 2.0 can only verify the digital signatures of external cabinets, and only by the use of the [MsiDigitalSignature](msidigitalsignature-table.md) and MsiDigitalCertificate tables.</span></span>

<span data-ttu-id="087f7-111">Ab Windows Installer Version 3,0 können die Windows Installer die digitalen Signaturen von Patches (MSP-Dateien) mithilfe der [MsiPatchCertificate](msipatchcertificate-table.md) -und msidigitalcertificate-Tabellen überprüfen.</span><span class="sxs-lookup"><span data-stu-id="087f7-111">Beginning with Windows Installer version 3.0, the Windows Installer can verify the digital signatures of patches (.msp files) by using the [MsiPatchCertificate](msipatchcertificate-table.md) and MsiDigitalCertificate tables.</span></span> <span data-ttu-id="087f7-112">Weitere Informationen finden Sie unter [Richtlinien zum Erstellen von sicheren Installationen](guidelines-for-authoring-secure-installations.md) und zum [Patchen von Benutzerkontensteuerung (User Account Control, UAC)](user-account-control--uac--patching.md).</span><span class="sxs-lookup"><span data-stu-id="087f7-112">For more information, see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and [User Account Control (UAC) Patching](user-account-control--uac--patching.md).</span></span>

<span data-ttu-id="087f7-113">Die msidigitalcertificate-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="087f7-113">The MsiDigitalCertificate table has the following columns.</span></span>



| <span data-ttu-id="087f7-114">Spalte</span><span class="sxs-lookup"><span data-stu-id="087f7-114">Column</span></span>             | <span data-ttu-id="087f7-115">Typ</span><span class="sxs-lookup"><span data-stu-id="087f7-115">Type</span></span>                         | <span data-ttu-id="087f7-116">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="087f7-116">Key</span></span> | <span data-ttu-id="087f7-117">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="087f7-117">Nullable</span></span> |
|--------------------|------------------------------|-----|----------|
| <span data-ttu-id="087f7-118">Digitalcertificate</span><span class="sxs-lookup"><span data-stu-id="087f7-118">DigitalCertificate</span></span> | [<span data-ttu-id="087f7-119">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="087f7-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="087f7-120">J</span><span class="sxs-lookup"><span data-stu-id="087f7-120">Y</span></span>   | <span data-ttu-id="087f7-121">N</span><span class="sxs-lookup"><span data-stu-id="087f7-121">N</span></span>        |
| <span data-ttu-id="087f7-122">Certdata</span><span class="sxs-lookup"><span data-stu-id="087f7-122">CertData</span></span>           | [<span data-ttu-id="087f7-123">Binär (Binary)</span><span class="sxs-lookup"><span data-stu-id="087f7-123">Binary</span></span>](binary.md)         | <span data-ttu-id="087f7-124">N</span><span class="sxs-lookup"><span data-stu-id="087f7-124">N</span></span>   | <span data-ttu-id="087f7-125">N</span><span class="sxs-lookup"><span data-stu-id="087f7-125">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="087f7-126">Spalten</span><span class="sxs-lookup"><span data-stu-id="087f7-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="087f7-127"><span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>Digitalcertificate</span><span class="sxs-lookup"><span data-stu-id="087f7-127"><span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate</span></span>
</dt> <dd>

<span data-ttu-id="087f7-128">Identifiziert das digitale Signaturzertifikat.</span><span class="sxs-lookup"><span data-stu-id="087f7-128">Identifies the digital signature certificate.</span></span> <span data-ttu-id="087f7-129">Primärschlüssel der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="087f7-129">Primary key of table.</span></span>

</dd> <dt>

<span data-ttu-id="087f7-130"><span id="CertData"></span><span id="certdata"></span><span id="CERTDATA"></span>Certdata</span><span class="sxs-lookup"><span data-stu-id="087f7-130"><span id="CertData"></span><span id="certdata"></span><span id="CERTDATA"></span>CertData</span></span>
</dt> <dd>

<span data-ttu-id="087f7-131">Die binäre Darstellung des digitalen Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="087f7-131">The binary representation of the digital certificate.</span></span> <span data-ttu-id="087f7-132">Die certdata-Spalte enthält das codierte Bytearray eines Zertifikat Kontexts.</span><span class="sxs-lookup"><span data-stu-id="087f7-132">The CertData column contains the encoded byte array of a certificate context.</span></span> <span data-ttu-id="087f7-133">Dies ist der **pbcertencoded** -Member der [**CERT- \_ Kontext**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) Struktur.</span><span class="sxs-lookup"><span data-stu-id="087f7-133">This is the **pbCertEncoded** member of the [**CERT\_CONTEXT**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) structure.</span></span> <span data-ttu-id="087f7-134">Der Zertifikat Kontext kann durch Aufrufen von [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust), [**msigetfilesignatureinformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)oder durch Importieren einer CER-Datei abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="087f7-134">The certificate context can be obtained by calling [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust), [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa), or by importing a .cer file.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="087f7-135">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="087f7-135">Validation</span></span>

<dl>

[<span data-ttu-id="087f7-136">ICE03</span><span class="sxs-lookup"><span data-stu-id="087f7-136">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="087f7-137">ICE06</span><span class="sxs-lookup"><span data-stu-id="087f7-137">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="087f7-138">ICE29</span><span class="sxs-lookup"><span data-stu-id="087f7-138">ICE29</span></span>](ice29.md)  
[<span data-ttu-id="087f7-139">ICE32</span><span class="sxs-lookup"><span data-stu-id="087f7-139">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="087f7-140">ICE66</span><span class="sxs-lookup"><span data-stu-id="087f7-140">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="087f7-141">ICE81</span><span class="sxs-lookup"><span data-stu-id="087f7-141">ICE81</span></span>](ice81.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="087f7-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="087f7-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="087f7-143">**Msigetfilesignatureinformation**</span><span class="sxs-lookup"><span data-stu-id="087f7-143">**MsiGetFileSignatureInformation**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)
</dt> <dt>

[<span data-ttu-id="087f7-144">Msidigitalsignature-Tabelle</span><span class="sxs-lookup"><span data-stu-id="087f7-144">MsiDigitalSignature table</span></span>](msidigitalsignature-table.md)
</dt> <dt>

[<span data-ttu-id="087f7-145">Digitale Signaturen und Windows Installer</span><span class="sxs-lookup"><span data-stu-id="087f7-145">Digital Signatures and Windows Installer</span></span>](digital-signatures-and-windows-installer.md)
</dt> </dl>

 

 
