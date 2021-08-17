---
description: Ein Administrator kann die folgenden Methoden verwenden, um einem Benutzer ohne Administratorrechte die Installation einer Anwendung mit erhöhten Systemberechtigungen zu ermöglichen.
ms.assetid: 61b9297e-f45e-4f50-9001-9bae580e1bf4
title: Installieren eines Pakets mit erhöhten Rechten für einen Nicht-Administrator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 603d2a39fd20a6ae2971a29e615887041e2a1fbf64989e93d5a1046f96102b5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946108"
---
# <a name="installing-a-package-with-elevated-privileges-for-a-non-admin"></a>Installieren eines Pakets mit erhöhten Rechten für einen Nicht-Administrator

Ein Administrator kann die folgenden Methoden verwenden, um einem Benutzer ohne Administratorrechte die Installation einer Anwendung mit erhöhten Systemberechtigungen zu ermöglichen.

-   In Windows Vista mit Windows Installer kann ein Mitglied der Gruppe Administratoren einem Nichtadministrator die Berechtigung zum Erhöhen der Installation über die Benutzerkontensteuerung (User [*Account Control,*](u-gly.md) UAC) bereitstellen, wie unter Verwenden des [Windows-Installers](using-windows-installer-with-uac.md)mit UAC beschrieben.

    **Windows Vista:** Erforderlich.

Die folgenden Methoden können auch verwendet werden, um eine Anwendung mit erhöhten Systemberechtigungen zu installieren.

-   Ein Administrator kann eine Anwendung auf dem Computer eines Benutzers anbenennen, indem [](/previous-versions/windows/desktop/Policy/group-policy-start-page)er das Paket Windows Installer mithilfe von Anwendungsbereitstellung und -Gruppenrichtlinie. Der Administrator gibt das Paket für die Computerinstallation an. Wenn dann ein Benutzer ohne Administratorrechte die Anwendung installiert, kann die Installation mit erhöhten Rechten ausgeführt werden. Benutzer ohne Administratorrechte können keine nichtvertierten Pakete installieren, die erhöhte Systemberechtigungen erfordern.
-   Ein Administrator kann zum Computer des [](advertisement.md) Benutzers wechseln und die Anwendung für die Installation pro Computer ankn.) Da der Windows-Installer beim Ausführen von Installationen im Installationskontext [](installation-context.md)pro Computer immer über erhöhte Rechte verfügt, kann die Installation mit erhöhten Rechten ausgeführt werden, wenn ein Benutzer ohne Administratorrechte die angekündigte Anwendung installiert. Benutzer ohne Administratorrechte können weiterhin keine nichtvertierten Pakete installieren, die erhöhte Rechte erfordern.
-   Ein nicht privilegierter Benutzer kann eine angekündigte Anwendung installieren, für die erhöhte Rechte erforderlich sind, wenn ein lokaler System-Agent die Anwendung ankn gibt. Die Anwendung kann für eine Benutzer- oder Computerinstallation angekündigt werden. Eine mit dieser Methode installierte Anwendung wird als verwaltet betrachtet. Weitere Informationen finden Sie unter [Advertising a Per-User Application To Be Installed with Elevated Privileges](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md).
-   Ein Administrator kann die [AlwaysInstallElevated-Richtlinie](alwaysinstallelevated.md) sowohl für Benutzer- als auch für Computerinstallationen festlegen. Diese Methode kann ein Sicherheitsrisiko für einen Computer darstellen, da ein Benutzer ohne Administratorrechte Installationen mit erhöhten Rechten ausführen und auf sichere Speicherorte auf dem Computer zugreifen kann, z. B. SystemFolder oder **den HKLM-Registrierungsschlüssel.**

    Wenn die Anwendung pro Computer installiert wird, während die [AlwaysInstallElevated-Richtlinie](alwaysinstallelevated.md) festgelegt ist, wird das Produkt als verwaltet behandelt. In diesem Fall kann die Anwendung weiterhin eine Reparatur mit erhöhten Rechten durchführen, wenn die Richtlinie entfernt wird. Wenn die Anwendung pro Benutzer installiert wird, während die AlwaysInstallElevated-Richtlinie festgelegt ist, kann die Anwendung auch keine Reparatur durchführen, wenn die Richtlinie entfernt wird.

-   Ein Administrator kann zum Computer eines Benutzers wechseln und eine computerspezifische Installation der Anwendung ausführen. Da Berechtigungen erforderlich sind, um diese Art von Installation durchzuführen, werden Installationen pro Computer immer verwaltet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Installationskontext](installation-context.md)
</dt> </dl>

 

 
