---
description: Die Tabelle MsiDigitalCertificate speichert Zertifikate im Binärdatenstromformat und ordnet jedes Zertifikat einem Primärschlüssel zu.
ms.assetid: 834534b8-540a-48c2-8eb0-3511d5a20cb4
title: MsiDigitalCertificate-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 443e5f27d13ebd823fa8e5362de474082d39e4b09b9e240b9ee16e9924342e41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828780"
---
# <a name="msidigitalcertificate-table"></a>MsiDigitalCertificate-Tabelle

Die Tabelle MsiDigitalCertificate speichert Zertifikate im Binärdatenstromformat und ordnet jedes Zertifikat einem Primärschlüssel zu. Der Primärschlüssel wird verwendet, um Zertifikate für mehrere digital signierte Objekte freizugeben. Ein digitales Zertifikat ist ein Anmeldeinformationszertifikat, mit dem die Identität überprüft werden kann. Weitere Informationen finden Sie unter [Digitale Zertifikate](../seccrypto/digital-certificates.md) im Abschnitt [Kryptografie](../seccrypto/cryptography-portal.md) des Microsoft Windows Software Development Kit (SDK).

Die Tabellen [MsiDigitalSignature](msidigitalsignature-table.md) und MsiDigitalCertificate sind ab Windows Installer Version 2.0 verfügbar.

Windows Das Installationsprogramm kann digitale Signaturen verwenden, um beschädigte Ressourcen zu erkennen. Windows Installationsprogrammversion 2.0 kann nur die digitalen Signaturen externer Schränke überprüfen, und zwar nur mithilfe der Tabellen [MsiDigitalSignature](msidigitalsignature-table.md) und MsiDigitalCertificate.

Ab Windows Installer Version 3.0 kann der Windows Installer die digitalen Signaturen von Patches (MSP-Dateien) mithilfe der Tabellen [MsiPatchCertificate](msipatchcertificate-table.md) und MsiDigitalCertificate überprüfen. Weitere Informationen finden Sie unter [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and User Account Control [(UAC) Patching .](user-account-control--uac--patching.md)

Die Tabelle MsiDigitalCertificate weist die folgenden Spalten auf.



| Spalte             | Typ                         | Key | Nullwerte zulässig |
|--------------------|------------------------------|-----|----------|
| DigitalCertificate | [Identifier](identifier.md) | J   | N        |
| CertData           | [Binär (Binary)](binary.md)         | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate
</dt> <dd>

Identifiziert das digitale Signaturzertifikat. Primärschlüssel der Tabelle.

</dd> <dt>

<span id="CertData"></span><span id="certdata"></span><span id="CERTDATA"></span>CertData
</dt> <dd>

Die binäre Darstellung des digitalen Zertifikats. Die Spalte CertData enthält das codierte Bytearray eines Zertifikatkontexts. Dies ist der **pbCertEncoded-Member** der [**CERT \_ CONTEXT-Struktur.**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) Der Zertifikatkontext kann durch Aufrufen von [**WinVerifyTrust,**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)oder durch Importieren einer CER-Datei abgerufen werden.

</dd> </dl>

## <a name="validation"></a>Überprüfung

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

[**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)
</dt> <dt>

[MsiDigitalSignature-Tabelle](msidigitalsignature-table.md)
</dt> <dt>

[Digitale Signaturen und Windows Installer](digital-signatures-and-windows-installer.md)
</dt> </dl>

 

 
