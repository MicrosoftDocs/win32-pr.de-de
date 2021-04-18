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
# <a name="msidigitalsignature-table"></a>Msidigitalsignature-Tabelle

Die msidigitalsignature-Tabelle enthält die Signatur Informationen für jedes Digital signierte Objekt in der Installations Datenbank.

Die Tabellen msidigitalsignature und [msidigitalcertificate](msidigitalcertificate-table.md) sind ab Windows Installer Version 2,0 verfügbar.

Windows Installer Version kann digitale Signaturen als Mittel zum erkennen beschädigter Ressourcen verwenden. In Windows Installer 2,0 können nur die digitalen Signaturen externer Schränke und nur die Verwendung der Tabellen msidigitalsignature und [msidigitalcertificate](msidigitalcertificate-table.md) überprüft werden.

Ab Windows Installer 3,0 kann der Windows Installer die digitalen Signaturen von Patches (MSP-Dateien) mithilfe der [MsiPatchCertificate](msipatchcertificate-table.md) -und msidigitalcertificate-Tabellen überprüfen. Weitere Informationen finden Sie unter [Richtlinien zum Erstellen von sicheren Installationen](guidelines-for-authoring-secure-installations.md) und zum [Patchen von Benutzerkontensteuerung (User Account Control, UAC)](user-account-control--uac--patching.md).

Die msidigitalsignature-Tabelle weist die folgenden Spalten auf.



| Spalte               | Typ                         | Schlüssel | Nullwerte zulässig |
|----------------------|------------------------------|-----|----------|
| Tabelle                | [Bezeichner](identifier.md) | J   | N        |
| Signobject           | [Text](text.md)             | J   | N        |
| Digitalcertificate\_ | [Bezeichner](identifier.md) | N   | N        |
| Hash                 | [Binär (Binary)](binary.md)         | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Glaub
</dt> <dd>

Bei der Windows Installer Version 2,0 muss der Eintrag in diesem Feld für die [Medien Tabelle](media-table.md)"Media" lauten. Das Installationsprogramm überprüft nur die digitalen Signaturen auf externen CAB-Medien Einträgen. Diese Spalte und die signobject-Spalte geben die Ressource an, die digital signiert ist.

</dd> <dt>

<span id="SignObject"></span><span id="signobject"></span><span id="SIGNOBJECT"></span>Signobject
</dt> <dd>

Ein Fremdschlüssel in den Primärschlüssel der Tabelle, der in der Tabellenspalte angegeben ist. In dieser Spalte und der Tabellenspalte wird die Ressource, die digital signiert ist, in der Spalte angegeben.

</dd> <dt>

<span id="DigitalCertificate_"></span><span id="digitalcertificate_"></span><span id="DIGITALCERTIFICATE_"></span>Digitalcertificate\_
</dt> <dd>

Ein Fremdschlüssel in die [msidigitalcertificate-Tabelle](msidigitalcertificate-table.md). Dadurch wird das Zertifikat identifiziert, das in der Datei vorhanden sein muss, damit die zugeordnete Aktion erfolgreich ausgeführt werden konnte. Die Ressource (oder das Objekt) muss immer mit diesem Zertifikat in der Tabelle "msidigitalcertificate" abgeglichen werden.

</dd> <dt>

<span id="Hash"></span><span id="hash"></span><span id="HASH"></span>Hash
</dt> <dd>

Geben Sie in diesem Feld den Verweis Hash der Ressource (oder des Objekts) ein, die mit dem tatsächlichen Hash der Ressource (oder des Objekts) überprüft werden soll, die zur Laufzeit abgerufen wurde. Wenn nur das Zertifikat überprüft werden muss, ist das hashfeld möglicherweise NULL. Beachten Sie, dass das Format des Hashs abhängig vom Typ der zu Signier enden Ressource (oder des Objekts) ist.

Die Hash Spalte enthält die binäre Darstellung des Hashs. Der tatsächliche Inhalt ist der **pbData** -Member der [**crypt- \_ Hash- \_ blobstruktur**](/windows/win32/api/dpapi/ns-dpapi-crypt_integer_blob) , der Teil der **CryptoAPI- \_ BLOB** -Struktur ist. Dies kann durch Aufrufen von [WinVerifyTrust](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) oder [**msigetfilesignatureinformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)erreicht werden.

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

[Msidigitalcertificate-Tabelle](msidigitalcertificate-table.md)
</dt> <dt>

[Digitale Signaturen und Windows Installer](digital-signatures-and-windows-installer.md)
</dt> </dl>

 

 
