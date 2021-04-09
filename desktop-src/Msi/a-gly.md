---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ms.assetid: 541fd08c-c21a-4a51-aa1c-d65cc0f5da75
title: A (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46677d8823c5298307db922f2d61285564add437
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131513"
---
# <a name="a-windows-installer"></a>A (Windows Installer)

a [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z

<dl> <dt>

<span id="_msi_accessibility_using_windows_installer_gly"></span><span id="_MSI_ACCESSIBILITY_USING_WINDOWS_INSTALLER_GLY"></span>**Barrierefreiheit**
</dt> <dd>

Entwurfs Implementierung, damit alle Benutzer auf die Benutzeroberfläche des Installers zugreifen können. Weitere Informationen zur Barrierefreiheit finden Sie im Übersichts Thema: [Barrierefreiheit](accessibility.md).

</dd> <dt>

<span id="_msi_acquisition_phase_gly"></span><span id="_MSI_ACQUISITION_PHASE_GLY"></span>**Erwerbsphase**
</dt> <dd>

Phase der Installation, in der das Installationsprogramm die Prozedur bestimmt. Die Erwerbsphase beginnt, wenn eine Anwendung oder ein Benutzer [*Windows Installer*](m-gly.md) anweist, eine Anwendung oder ein Feature zu installieren. Der Installer fragt dann die [*Datenbank*](i-gly.md) nach Informationen ab, wenn das [*Ausführungs Skript*](e-gly.md) für die Installation generiert wird. Weitere Informationen zu den Phasen einer-Installation finden Sie unter [Installationsmechanismus](installation-mechanism.md).

</dd> <dt>

<span id="_msi_action_gly"></span><span id="_MSI_ACTION_GLY"></span>**Hinspiel**
</dt> <dd>

Viele der Funktionen, die von Windows Installer ausgeführt werden, werden in Aktionen gekapselt. Jede Aktion gibt die Ausführung einer bestimmten Funktion an, und der gesamte prozedurale Ablauf der Installation wird durch die Abfolge der Aktionen in den [*Sequenz Tabellen*](s-gly.md)vorgeschrieben. [*Standard Aktionen*](s-gly.md) werden in Windows Installer integriert. [*Benutzerdefinierte Aktionen*](c-gly.md) werden vom Autor des Installations [*Pakets*](p-gly.md)geschrieben.

</dd> <dt>

<span id="_msi_admin_approval_mode_gly"></span><span id="_MSI_ADMIN_APPROVAL_MODE_GLY"></span>**Administrator Genehmigungs Modus**
</dt> <dd>

Der durch den Benutzerkonten Schutz (User Account Protection, UAC) aktivierte Genehmigungs Zustand, der alle Benutzer mit geringsten Rechten (einschließlich Administratoren) ausführt. Benutzer müssen Ihre Zustimmung erteilen, um Installationen zu erhöhen, für die Administratorrechte erforderlich sind.

</dd> <dt>

<span id="_msi_advertising_gly"></span><span id="_MSI_ADVERTISING_GLY"></span>**Lip**
</dt> <dd>

Die Möglichkeit, die zum Laden von erforderlichen Schnittstellen zu erstellen und eine Anwendung verfügbar zu machen, ohne die Anwendung zu installieren. Wenn ein Benutzer oder eine Anwendung eine angekündigte Oberfläche aktiviert, fährt der Installer mit der Installation der erforderlichen Komponenten fort. Die beiden Arten der Werbung sind das [*zuweisen*](/windows) und [*veröffentlichen*](p-gly.md). Weitere Informationen finden Sie unter auch [*bei Bedarf installieren*](i-gly.md). Weitere Informationen darüber, wie das Installationsprogramm Anwendungen angekündigt [, finden Sie](advertisement.md)unter Ankündigung.

</dd> <dt>

<span id="_msi_application_information_service_gly"></span><span id="_MSI_APPLICATION_INFORMATION_SERVICE_GLY"></span>**Anwendungs Informationsdienst (AIS)**
</dt> <dd>

Ein Systemdienst von Windows Vista, der das Starten von Installationen ermöglicht, für die erhöhte Rechte erforderlich sind. Stellt die Zustimmungs Benutzeroberfläche bereit, die von der Benutzerkontensteuerung verwendet wird, um einen Benutzer zur Administrator Autorisierung aufzufordern

</dd> <dt>

<span id="_msi_assigning_gly"></span><span id="_MSI_ASSIGNING_GLY"></span>**Musters**
</dt> <dd>

Stellt eine Anwendung zur Verfügung und macht Sie so angezeigt, als wäre sie für einen Benutzer installiert, ohne Sie tatsächlich zu installieren. Beim zuweisen werden dem **Startmenü** Verknüpfungen und Symbole hinzugefügt, die entsprechenden Dateien zugeordnet und Registrierungseinträge für die Anwendung geschrieben. Wenn ein Benutzer versucht, eine zugewiesene Anwendung zu öffnen, installiert das Installationsprogramm die Anwendung. Das zuweisen und [*veröffentlichen*](p-gly.md) sind zwei Methoden zur [*Werbung*](/windows). Weitere Informationen finden Sie unter [Ankündigung.](advertisement.md)

</dd> <dt>

<span id="_msi_asynchronous_execution_using_windows_installer_gly"></span><span id="_MSI_ASYNCHRONOUS_EXECUTION_USING_WINDOWS_INSTALLER_GLY"></span>**asynchrone Ausführung**
</dt> <dd>

[*Benutzerdefinierte Aktion*](c-gly.md) , bei der das Installationsprogramm separate Threads der benutzerdefinierten Aktion und der aktuellen Installation gleichzeitig ausführt. Weitere Informationen finden Sie unter [synchrone und asynchrone benutzerdefinierte Aktionen](synchronous-and-asynchronous-custom-actions.md).

</dd> </dl>

 

 
