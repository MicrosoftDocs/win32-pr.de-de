---
description: Durch das Patchen der Benutzerkontensteuerung (User Account Control, UAC) können Autoren von Windows Installer-Installationen Digital signierte Patches identifizieren, die in Zukunft von Benutzern ohne Administratorrechte angewendet werden können.
ms.assetid: f7d64f61-24c8-4037-a10b-d68d0e9e3c42
title: Patching der Benutzerkontensteuerung (User Account Control, UAC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d111a39245ab15b24c1734d278a8e0a477e68a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868832"
---
# <a name="user-account-control-uac-patching"></a>Patching der Benutzerkontensteuerung (User Account Control, UAC)

Durch das Patchen der [*Benutzerkontensteuerung (User Account Control*](u-gly.md) , UAC) können Autoren von Windows Installer-Installationen Digital signierte Patches identifizieren, die in Zukunft von Benutzern ohne Administratorrechte angewendet werden können.

Wenn die digitale Signatur nicht mit dem Zertifikat identisch ist, zeigt Windows Vista vor der Installation des Patches ein UAC-Dialogfeld an, das die Administrator Autorisierung anfordert. Auf Systemen, die älter als Windows Vista sind, wendet das Installationsprogramm keinen signierten Patch an, der nicht dem Zertifikat entspricht.

Wenn ein nicht-Administrator versucht, einen Patch auf eine Anwendung anzuwenden, und die folgenden Bedingungen nicht erfüllt sind, wird der Benutzer von Windows Vista benachrichtigt, dass vor der Installation des Patches eine Administrator Autorisierung erforderlich ist. Ein nicht Administrator kann die Installation des Patches fortsetzen, ohne dass zusätzliche Administrator Berechtigungen erforderlich sind, wenn die folgenden Bedingungen erfüllt sind.

-   Die Anwendung wurde unter Windows Vista oder Windows XP mit Windows Installer 3,0 oder höher installiert.

    **Windows Server 2008:** Nicht unterstützt.

-   Wenn die Anwendung unter Windows XP installiert wurde, muss die Anwendung auch auf einem Wechsel Datenträger installiert sein, z. b. CD-ROM oder DVD-Datenträger. Diese Einschränkung gilt nicht, wenn die Anwendung unter Windows Vista installiert wurde.
-   Die Anwendung wurde nicht aus einem Quell Abbild der [administrativen Installation](administrative-installation.md) installiert.
-   Die Anwendung wurde ursprünglich pro Computer installiert. Informationen dazu, wie Sie nicht-Administratoren das Anwenden von Patches auf pro Benutzer verwaltete Anwendungen ermöglichen, nachdem der Patch von einem Administrator als vertrauenswürdig eingestuft wurde, finden Sie unter [Patchen Per-User verwaltete Anwendungen](patching-per-user-managed-applications.md).
-   Die [MsiPatchCertificate-Tabelle](msipatchcertificate-table.md) ist im Windows Installer-Paket (MSI-Datei) vorhanden und enthält die Informationen, die erforderlich sind, um die UAC zu aktivieren. Die Tabelle und die Informationen sind möglicherweise im ursprünglichen Installationspaket enthalten oder wurden von einer Windows Installer Patchdatei (MSP-Datei) zum Paket hinzugefügt.
-   Die Patches sind digital signiert durch ein Zertifikat, das in der [MsiPatchCertificate-Tabelle](msipatchcertificate-table.md)aufgeführt ist. Weitere Informationen zu Zertifikaten für digitale Signaturen finden Sie unter [digitale Signaturen und Windows Installer](digital-signatures-and-windows-installer.md).
-   Die digitale Signatur des Patchpakets kann anhand des Zertifikats in der [MsiPatchCertificate-Tabelle](msipatchcertificate-table.md)überprüft werden. Weitere Informationen zur Verwendung digitaler Signaturen, digitaler Zertifikate und [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust)finden Sie im Abschnitt " [Sicherheit](https://msdn.microsoft.com/library/cc527452.aspx) " des Microsoft Windows Software Development Kit (SDK).
-   Das Signatur Geber Zertifikat, das zum Überprüfen der digitalen Signatur im Patchpaket verwendet wird, ist gültig und wurde nicht widerrufen.
    > [!Note]  
    > Obwohl Sie einen Patch nicht mithilfe eines abgelaufenen Zertifikats signieren können, schlägt die Auswertung einer digitalen Signatur auf einem Patch nicht fehl, wenn das Zertifikat abgelaufen ist. Bei der Auswertung wird die aktuelle [MsiPatchCertificate-Tabelle](msipatchcertificate-table.md)verwendet, die aus der MsiPatchCertificate-Tabelle im ursprünglichen Paket und allen Änderungen an der Tabelle von Patches besteht, die vor dem aktuellen Paket sequenziert wurden. Ein Patch kann der MsiPatchCertificate-Tabelle neue Zertifikate hinzufügen, um die nach dem aktuellen Patch sequenzierten Patches auszuwerten. Ein gesperrtes Zertifikat wird immer abgelehnt.

     

-   Das Patchen von Berechtigungen mit geringsten Rechten wurde nicht deaktiviert, indem die [**msidisableluapatching**](msidisableluapatching.md) -Eigenschaft oder die [disableluapatching](disableluapatching.md) -Richtlinie festgelegt wurde.

Ein Patch, der mithilfe von UAC-Patchen angewendet wurde, kann auch von einem nicht Administrator entfernt werden.

Administratoren können Patches unabhängig von der UAC-Einstellung der Anwendung auf pro Computer installierte Produkte anwenden.

Sie können bestimmen, ob das Patchen mit den geringsten Rechten für eine Anwendung aktiviert ist, indem Sie die [**msigetproductinfoex**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa) -Funktion verwenden, um die von InstallProperty \_ autorisierte \_ Lua-App-Eigenschaft abzufragen \_ , oder indem Sie die [**productinfo**](installer-productinfo.md) -Methode verwenden, um die authorizedluaapp-Eigenschaft abzufragen. Wenn der Wert einer der beiden Eigenschaften 1 ist, wird die Anwendung für das Patchen von Benutzerkonten mit geringstmöglichen Berechtigungen aktiviert.

Ein Administrator kann das Patchen von geringsten Rechten auf dem Computer deaktivieren, indem er die Richtlinie " [disableluapatching](disableluapatching.md) " auf 1 festlegt. Sie können die [**msidisableluapatching**](msidisableluapatching.md) -Eigenschaft während der Erstinstallation einer Anwendung auf 1 festlegen, um das Patchen mit geringsten Rechten nur für diese Anwendung zu verhindern.

Diese Funktionalität ist ab Windows Installer Version 3,0 verfügbar. Das Patchen der Benutzerkontensteuerung (User Account Control, UAC) wurde in Windows XP als Benutzerkonto mit geringsten Rechten (LUA) bezeichnet. Das Lua-Patchen ist unter Windows 2000 und Windows Server 2003 nicht verfügbar.

Weitere Informationen zur Anwendungs Kompatibilität und zum Entwickeln von Anwendungen, die mit der Benutzerkontensteuerung (User Account Control, UAC) kompatibel sind, finden Sie in den auf [Microsoft TechNet](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc709691(v=ws.10))bereitgestellten UAC-Informationen.

 

 
