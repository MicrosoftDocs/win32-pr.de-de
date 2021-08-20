---
description: Das Patchen der Benutzerkontensteuerung (User Account Control, UAC) ermöglicht es den Autoren von Installationen des Windows-Installers, digital signierte Patches zu identifizieren, die zukünftig von Benutzern ohne Administratorrechte angewendet werden können.
ms.assetid: f7d64f61-24c8-4037-a10b-d68d0e9e3c42
title: Patchen der Benutzerkontensteuerung (User Account Control, UAC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 689da3d09541199d6ff231e4f6ce909d7342025ab443d79e4db47aee9deb2733
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012808"
---
# <a name="user-account-control-uac-patching"></a>Patchen der Benutzerkontensteuerung (User Account Control, UAC)

[*Das Patchen*](u-gly.md) der Benutzerkontensteuerung (User Account Control, UAC) ermöglicht es den Autoren von Installationen des Windows-Installers, digital signierte Patches zu identifizieren, die zukünftig von Benutzern ohne Administratorrechte angewendet werden können.

Wenn die digitale Signatur nicht mit dem Zertifikat kompatibel ist, zeigt Windows Vista ein UAC-Dialogfeld an, in dem die Administratorautorisierung vor der Installation des Patches erforderlich ist. Auf Systemen vor Windows Vista wird vom Installationsprogramm kein signierter Patch angewendet, der nicht mit dem Zertifikat kompatibel ist.

Wenn ein Nichtadministrator versucht, einen Patch auf eine Anwendung anzuwenden, und die folgenden Bedingungen nicht erfüllt sind, benachrichtigt Windows Vista den Benutzer, dass eine Administratorautorisierung erforderlich ist, bevor der Patch installiert wird. Ein Nichtadministrator kann den Patch weiterhin installieren, ohne zusätzliche Administratorautorisierung zu erhalten, vorausgesetzt, die folgenden Bedingungen sind erfüllt.

-   Die Anwendung wurde unter Windows Vista oder Windows XP mit Windows Installer 3.0 oder höher installiert.

    **Windows Server 2008:** Nicht unterstützt.

-   Wenn die Anwendung auf Windows XP installiert wurde, muss die Anwendung auch von Wechselmedien wie CD-ROM oder DVD-Datenträgern installiert worden sein. Diese Einschränkung gilt nicht, wenn die Anwendung auf Windows Vista installiert wurde.
-   Die Anwendung wurde nicht von einem Quellimage [für die Administratorinstallation](administrative-installation.md) installiert.
-   Die Anwendung wurde ursprünglich pro Computer installiert. Informationen dazu, wie Sie es Nichtadministratoren ermöglichen, Patches auf benutzerspezifische verwaltete Anwendungen anzuwenden, nachdem der Patch von einem Administrator als vertrauenswürdig genehmigt wurde, finden Sie unter Patchen Per-User [Verwalteten Anwendungen](patching-per-user-managed-applications.md).
-   Die [Tabelle MsiPatchCertificate](msipatchcertificate-table.md) ist im Window Installer-Paket (.msi-Datei) vorhanden und enthält die Informationen, die zum Aktivieren der UAC erforderlich sind. Die Tabelle und die Informationen wurden möglicherweise im ursprünglichen Installationspaket enthalten oder dem Paket durch eine Windows Installer-Patchdatei (MSP-Datei) hinzugefügt.
-   Die Patches werden digital von einem Zertifikat signiert, das in der [MsiPatchCertificate-Tabelle aufgeführt ist.](msipatchcertificate-table.md) Weitere Informationen zu Zertifikaten für digitale Signaturen finden Sie unter [Digitale Signaturen und Windows Installer.](digital-signatures-and-windows-installer.md)
-   Die digitale Signatur im Patchpaket kann anhand des Zertifikats in der [Tabelle MsiPatchCertificate überprüft werden.](msipatchcertificate-table.md) Weitere Informationen zur Verwendung von digitalen Signaturen, digitalen Zertifikaten und [](https://msdn.microsoft.com/library/cc527452.aspx) [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust)finden Sie im Abschnitt Sicherheit des Microsoft Windows Software Development Kit (SDK).
-   Das Signaturzertifikat, mit dem überprüft wird, ob die digitale Signatur im Patchpaket gültig ist und nicht widerrufen wurde.
    > [!Note]  
    > Obwohl Sie einen Patch nicht mit einem abgelaufenen Zertifikat signieren können, kann die Auswertung einer digitalen Signatur auf einem Patch nicht fehlschlagen, wenn das Zertifikat abgelaufen ist. Bei der Auswertung wird die aktuelle [MsiPatchCertificate-Tabelle](msipatchcertificate-table.md)verwendet, die aus der MsiPatchCertificate-Tabelle im ursprünglichen Paket und allen Änderungen an der Tabelle nach Patches besteht, die vor dem aktuellen Paket sequenziert wurden. Ein Patch kann der MsiPatchCertificate-Tabelle neue Zertifikate hinzufügen, um Patches zu bewerten, die nach dem aktuellen Patch sequenziert wurden. Ein gesperrtes Zertifikat wird immer abgelehnt.

     

-   Das Patchen mit den geringsten Rechten wurde nicht durch Festlegen der [**MSIDISABLELUAPATCHING-Eigenschaft**](msidisableluapatching.md) oder der [DisableLUAPatching-Richtlinie](disableluapatching.md) deaktiviert.

Ein Patch, der mithilfe von UAC-Patching angewendet wurde, kann auch von einem Nichtadministrator entfernt werden.

Administratoren können Patches auf pro Computer installierte Produkte anwenden, unabhängig von der UAC-Einstellung der Anwendung.

Sie können bestimmen, ob das Patchen mit den geringsten Rechten für eine Anwendung aktiviert ist, indem Sie die [**MsiGetProductInfoEx-Funktion**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa) verwenden, um die INSTALLPROPERTY AUTHORIZED LUA APP-Eigenschaft abfragt, oder indem Sie die ProductInfo-Methode verwenden, um die \_ \_ Eigenschaft \_ "AuthorizedLUAApp" [](installer-productinfo.md) abfragt. Wenn der Wert einer eigenschaft 1 ist, wird die Anwendung für das Patchen von Benutzerkonten mit den geringsten Rechten aktiviert.

Ein Administrator kann das Patchen mit den geringsten Rechten auf dem Computer deaktivieren, indem er die [DisableLUAPatching-Richtlinie](disableluapatching.md) auf 1 festgelegt. Sie können die [**MSIDISABLELUAPATCHING-Eigenschaft**](msidisableluapatching.md) während der Erstinstallation einer Anwendung auf 1 festlegen, um das Patchen der geringsten Rechte nur für diese Anwendung zu verhindern.

Diese Funktionalität ist ab version 3.0 Windows Installer verfügbar. Das Patchen der Benutzerkontensteuerung (User Account Control, UAC) wurde als LUA-Patching (Least-Privilege User Account) in Windows XP bezeichnet. LUA-Patchen ist auf Windows 2000 und Windows Server 2003 nicht verfügbar.

Weitere Informationen zur Anwendungskompatibilität und zum Entwickeln von Anwendungen, die mit der Benutzerkontensteuerung (User Account Control, UAC) kompatibel sind, finden Sie in den UAC-Informationen, die auf [Microsoft Technet bereitgestellt werden.](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc709691(v=ws.10))

 

 
