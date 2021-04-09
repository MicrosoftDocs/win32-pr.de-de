---
description: Ein Administrator kann die folgenden Methoden verwenden, um einem Benutzer ohne Administratorrechte die Installation einer Anwendung mit erhöhten System Berechtigungen zu ermöglichen.
ms.assetid: 61b9297e-f45e-4f50-9001-9bae580e1bf4
title: Installieren eines Pakets mit erhöhten Rechten für einen nicht Administrator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec81de333d6ca388017e03c96f739d7bd258a7c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868227"
---
# <a name="installing-a-package-with-elevated-privileges-for-a-non-admin"></a>Installieren eines Pakets mit erhöhten Rechten für einen nicht Administrator

Ein Administrator kann die folgenden Methoden verwenden, um einem Benutzer ohne Administratorrechte die Installation einer Anwendung mit erhöhten System Berechtigungen zu ermöglichen.

-   In Windows Vista mit Windows Installer kann ein Mitglied der Gruppe "Administratoren" eine Autorisierung für einen nicht Administrator bereitstellen, um die Installation über die [*Benutzerkontensteuerung (User Account Control*](u-gly.md) , UAC) zu erhöhen, wie in [Verwenden von Windows Installer mit UAC](using-windows-installer-with-uac.md)beschrieben.

    **Windows Vista:** Erforderlich.

Die folgenden Methoden können auch zum Installieren einer Anwendung mit erhöhten System Berechtigungen verwendet werden.

-   Ein Administrator kann eine Anwendung auf dem Computer eines Benutzers ankündigen, indem er das Windows Installer-Paket mithilfe von Anwendungs Bereitstellung und [Gruppenrichtlinie](/previous-versions/windows/desktop/Policy/group-policy-start-page)zuweisen oder veröffentlichen. Der Administrator kündigt das Paket für die Installation pro Computer an. Wenn ein Benutzer, der nicht Administrator ist, die Anwendung installiert, kann die Installation mit erhöhten Rechten ausgeführt werden. Benutzer ohne Administratorrechte können nicht angekündigte Pakete nicht installieren, für die erhöhte System Berechtigungen erforderlich sind.
-   Ein Administrator kann zum [Computer des Benutzers wechseln und die](advertisement.md) Anwendung für die Installation pro Computer ankündigen. Da der Windows Installer immer über erhöhte Rechte verfügt, während Installationen im [Installations Kontext](installation-context.md)pro Computer ausgeführt werden, kann die Installation mit erhöhten Rechten ausgeführt werden, wenn ein Benutzer, der nicht Administrator ist, die angekündigte Anwendung installiert. Benutzer ohne Administratorrechte können weiterhin nicht angekündigte Pakete installieren, die erhöhte Rechte erfordern.
-   Ein nicht privilegierter Benutzer kann eine angekündigte Anwendung installieren, die erhöhte Rechte erfordert, wenn ein lokaler System-Agent die Anwendung ankündigt. Die Anwendung kann für eine Installation pro Benutzer oder pro Computer angekündigt werden. Eine mit dieser Methode installierte Anwendung wird als verwaltet betrachtet. Weitere Informationen finden Sie unter ankündigen [einer Per-User Anwendung, die mit erhöhten Rechten installiert werden soll](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md).
-   Ein Administrator kann die [alwaysinstallerhöhten](alwaysinstallelevated.md) -Richtlinie sowohl für Einzelbenutzer-als auch pro-Computer-Installationen festlegen. Diese Methode kann einen Computer mit einem Sicherheitsrisiko öffnen, denn wenn diese Richtlinie festgelegt ist, kann ein Benutzer, der kein Administrator ist, Installationen mit erhöhten Rechten ausführen und auf sichere Speicherorte auf dem Computer zugreifen, wie z. b. den Systemordner oder den **HKLM** -Registrierungsschlüssel.

    Wenn die Anwendung pro Computer installiert wird, während die [alwaysinstallerhöhten](alwaysinstallelevated.md) -Richtlinie festgelegt ist, wird das Produkt als verwaltet behandelt. In diesem Fall kann die Anwendung weiterhin eine Reparatur mit erhöhten Rechten durchführen, wenn die Richtlinie entfernt wird. Auch wenn die Anwendung pro Benutzer installiert wird, während die alwaysinstallerhöhten-Richtlinie festgelegt ist, kann die Anwendung keine Reparatur durchführen, wenn die Richtlinie entfernt wird.

-   Ein Administrator kann den Computer eines Benutzers aufrufen und eine Installation der Anwendung pro Computer durchführen. Da Berechtigungen zum Ausführen dieser Art von Installation erforderlich sind, werden Installationen pro Computer immer verwaltet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Installations Kontext](installation-context.md)
</dt> </dl>

 

 
