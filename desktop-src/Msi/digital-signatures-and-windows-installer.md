---
description: Der Windows Installer kann digitale Signaturen verwenden, um beschädigte Ressourcen zu erkennen.
ms.assetid: 68f2c686-cbe0-495d-a448-a7d2ca1df47b
title: Digitale Signaturen und Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 334cf226d683c9b9a658ce72e25bf7bf90145369c315da372bd6c4e9368b796a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692810"
---
# <a name="digital-signatures-and-windows-installer"></a>Digitale Signaturen und Windows Installer

Der Windows Installer kann digitale Signaturen verwenden, um beschädigte Ressourcen zu erkennen. Ein Signatorzertifikat kann mit dem Signatorzertifikat einer externen Ressource verglichen werden, die vom Paket installiert werden soll. Weitere Informationen zur Verwendung von digitalen Signaturen, digitalen Zertifikaten und [](https://msdn.microsoft.com/library/cc527452.aspx) [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust)finden Sie im Abschnitt Sicherheit des Microsoft Windows Software Development Kit (SDK).

Mit Windows Installer können digitale Signaturen mit installer Windows Paketen, Transformationen, Patches, Mergemodulen und externen Schränkendateien verwendet werden. Windows Das Installationsprogramm ist in die Softwareeinschränkungsrichtlinie auf Microsoft Windows XP integriert. Richtlinien können erstellt werden, um Installationen basierend auf verschiedenen Kriterien zu ermöglichen oder zu verhindern, einschließlich eines bestimmten Signatorzertifikats oder Herausgebers. Der Windows Installer kann die Signaturüberprüfung externer Schränkdateien auf allen Plattformen durchführen, auf denen CryptoAPI Version 2.0 installiert ist.

Beachten Sie, dass der Setup.exe-Bootstrap, der mit dem Windows Installer SDK bereitgestellt wird, vor dem Initiieren der Installation eine Signaturüberprüfung für ein Windows Installer-Paket ausführt.

Beim Ausführen [einer Administratorinstallation](administrative-installation.md) wird die digitale Signatur aus dem Paket entfernt. Eine Administratorinstallation ändert das Installationspaket, um den AdminProperties-Stream hinzuzufügen, wodurch die ursprüngliche digitale Signatur ungültig wird. Ein Administrator kann das Paket bezwingen.

Durch anwenden eines Patches auf eine Administratorinstallation wird auch die digitale Signatur aus dem Paket entfernt. Der Grund dafür ist, dass die Änderungen im gepatchten Installationspaket der Administratorinstallation beibehalten werden. Ein Administrator kann das Paket bezwingen.

Ab version 3.0 des Windows Installers ermöglicht das Patchen der Benutzerkontensteuerung [(User Account Control, UAC)](user-account-control--uac--patching.md) Benutzern ohne Administratorrechte das Patchen von Anwendungen, die im Kontext pro Computer installiert sind. Das UAC-Patchen wird aktiviert, indem ein Signaturzertifikat in der [Tabelle MsiPatchCertificate](msipatchcertificate-table.md) bereitgestellt und Patches mit demselben Zertifikat signiert werden.

Weitere Informationen finden Sie unter [Digitale](digital-signatures-and-external-cabinet-files.md)Signaturen und externe Schränkdateien, Windows Installer und [Softwareeinschränkungsrichtlinie,](windows-installer-and-software-restriction-policy.md) [](authoring-a-fully-verified-signed-installation.md)Erstellen einer vollständig überprüften signierten Installation und Eine URL-basierte Windows [Installer-Installationsbeispiel](a-url-based-windows-installer-installation-example.md).

 

 
