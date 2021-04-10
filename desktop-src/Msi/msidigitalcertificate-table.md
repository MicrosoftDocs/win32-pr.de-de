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
# <a name="msidigitalcertificate-table"></a>Msidigitalcertificate-Tabelle

Die msidigitalcertificate-Tabelle speichert Zertifikate im binären Streamformat und ordnet jedes Zertifikat einem Primärschlüssel zu. Der Primärschlüssel wird zum Freigeben von Zertifikaten für mehrere Digital signierte Objekte verwendet. Ein digitales Zertifikat ist eine Anmelde Information, die eine Möglichkeit zum Überprüfen der Identität bereitstellt. Weitere Informationen finden Sie im Abschnitt zur [Kryptografie](../seccrypto/cryptography-portal.md) [im Microsoft](../seccrypto/digital-certificates.md) Windows Software Development Kit (SDK).

Die Tabellen [msidigitalsignature](msidigitalsignature-table.md) und msidigitalcertificate sind ab Windows Installer Version 2,0 verfügbar.

Windows Installer können digitale Signaturen als Mittel zum erkennen beschädigter Ressourcen verwenden. In Windows Installer Version 2,0 können nur die digitalen Signaturen externer Schränke und nur die Verwendung der Tabellen [msidigitalsignature](msidigitalsignature-table.md) und msidigitalcertificate überprüft werden.

Ab Windows Installer Version 3,0 können die Windows Installer die digitalen Signaturen von Patches (MSP-Dateien) mithilfe der [MsiPatchCertificate](msipatchcertificate-table.md) -und msidigitalcertificate-Tabellen überprüfen. Weitere Informationen finden Sie unter [Richtlinien zum Erstellen von sicheren Installationen](guidelines-for-authoring-secure-installations.md) und zum [Patchen von Benutzerkontensteuerung (User Account Control, UAC)](user-account-control--uac--patching.md).

Die msidigitalcertificate-Tabelle weist die folgenden Spalten auf.



| Spalte             | Typ                         | Schlüssel | Nullwerte zulässig |
|--------------------|------------------------------|-----|----------|
| Digitalcertificate | [Bezeichner](identifier.md) | J   | N        |
| Certdata           | [Binär (Binary)](binary.md)         | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>Digitalcertificate
</dt> <dd>

Identifiziert das digitale Signaturzertifikat. Primärschlüssel der Tabelle.

</dd> <dt>

<span id="CertData"></span><span id="certdata"></span><span id="CERTDATA"></span>Certdata
</dt> <dd>

Die binäre Darstellung des digitalen Zertifikats. Die certdata-Spalte enthält das codierte Bytearray eines Zertifikat Kontexts. Dies ist der **pbcertencoded** -Member der [**CERT- \_ Kontext**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) Struktur. Der Zertifikat Kontext kann durch Aufrufen von [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust), [**msigetfilesignatureinformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)oder durch Importieren einer CER-Datei abgerufen werden.

</dd> </dl>

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE29](ice29.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
[ICE81](ice81.md)  
</dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Msigetfilesignatureinformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)
</dt> <dt>

[Msidigitalsignature-Tabelle](msidigitalsignature-table.md)
</dt> <dt>

[Digitale Signaturen und Windows Installer](digital-signatures-and-windows-installer.md)
</dt> </dl>

 

 
