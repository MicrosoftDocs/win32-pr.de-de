---
description: Der Windows Installer kann digitale Signaturen verwenden, um beschädigte Ressourcen zu erkennen.
ms.assetid: 68f2c686-cbe0-495d-a448-a7d2ca1df47b
title: Digitale Signaturen und Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d41dee15da938c586bf061d216d9003586a799c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363287"
---
# <a name="digital-signatures-and-windows-installer"></a>Digitale Signaturen und Windows Installer

Der Windows Installer kann digitale Signaturen verwenden, um beschädigte Ressourcen zu erkennen. Ein Signatur Geber Zertifikat kann mit dem Signatur Geber Zertifikat einer externen Ressource verglichen werden, die vom Paket installiert werden soll. Weitere Informationen zur Verwendung digitaler Signaturen, digitaler Zertifikate und [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust)finden Sie im Abschnitt " [Sicherheit](https://msdn.microsoft.com/library/cc527452.aspx) " des Microsoft Windows Software Development Kit (SDK).

Mit Windows Installer können digitale Signaturen mit Windows Installer Paketen, Transformationen, Patches, Mergemodulen und externen CAB-Dateien verwendet werden. Windows Installer ist in die Software Einschränkungs Richtlinie unter Microsoft Windows XP integriert. Richtlinien können erstellt werden, um Installationen, die auf unterschiedlichen Kriterien basieren, zuzulassen oder zu verhindern, einschließlich eines bestimmten Signatur Geber Zertifikats oder-Verlegers. Der Windows Installer kann die Signatur Überprüfung externer CAB-Dateien auf allen Plattformen durchführen, auf denen die CryptoAPI-Version 2,0 installiert ist.

Beachten Sie, dass das Beispiel Setup.exe Bootstrap, das mit dem Windows Installer SDK bereitgestellt wird, eine Signatur Prüfung für ein Windows Installer Paket durchführt, bevor die Installation initiiert wird.

Durch das Ausführen einer [administrativen Installation](administrative-installation.md) wird die digitale Signatur aus dem Paket entfernt. Eine administrative Installation ändert das Installationspaket, um den adminproperties-Stream hinzuzufügen, wodurch die ursprüngliche digitale Signatur ungültig wird. Ein Administrator kann das Paket zurückziehen.

Wenn Sie einen Patch auf eine administrative Installation anwenden, wird auch die digitale Signatur aus dem Paket entfernt. Der Grund hierfür ist, dass die Änderungen im gepatchten Installationspaket der administrativen Installation beibehalten werden. Ein Administrator kann das Paket zurückziehen.

Ab Windows Installer Version 3,0 ermöglicht das [Patchen von Benutzerkontensteuerung (User Account Control, UAC)](user-account-control--uac--patching.md) Benutzern, die keine Administratoren sind, das Patchen von Anwendungen, die im computerspezifischen Kontext installiert sind. Das UAC-Patchen wird aktiviert, indem ein Signatur Geber Zertifikat in der [MsiPatchCertificate](msipatchcertificate-table.md) -Tabelle bereitgestellt und Patches mit demselben Zertifikat signiert werden.

Weitere Informationen finden Sie unter [digitale Signaturen und externe CAB-Dateien](digital-signatures-and-external-cabinet-files.md), [Windows Installer und Software Einschränkungs Richtlinie](windows-installer-and-software-restriction-policy.md), [Erstellen einer vollständig überprüften signierten Installation](authoring-a-fully-verified-signed-installation.md)und [eines URL-basierten Windows Installer Installations Beispiels](a-url-based-windows-installer-installation-example.md).

 

 
