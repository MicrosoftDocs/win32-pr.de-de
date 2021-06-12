---
description: Erfahren Sie Windows Installer Konzepte, die mit dem Buchstaben A beginnen, z. B. Barrierefreiheit und Erwerbsphase.
ms.assetid: 541fd08c-c21a-4a51-aa1c-d65cc0f5da75
title: A (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eea91c044553ec374f28309a86002a386961d2c9
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011123"
---
# <a name="a-windows-installer"></a>A (Windows Installer)

A [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z

<dl> <dt>

<span id="_msi_accessibility_using_windows_installer_gly"></span><span id="_MSI_ACCESSIBILITY_USING_WINDOWS_INSTALLER_GLY"></span>**Zugänglichkeit**
</dt> <dd>

Entwurfsimplementierung, um die Benutzeroberfläche des Installationsprogramms für alle Benutzer zugänglich zu machen. Weitere Informationen zur Barrierefreiheit finden Sie im Übersichtsthema [Barrierefreiheit.](accessibility.md)

</dd> <dt>

<span id="_msi_acquisition_phase_gly"></span><span id="_MSI_ACQUISITION_PHASE_GLY"></span>**Erwerbsphase**
</dt> <dd>

Installationsphase, in der das Installationsprogramm die Prozedur bestimmt. Die Erwerbsphase beginnt, wenn eine [](m-gly.md) Anwendung oder ein Benutzer Windows Installer anweisen, eine Anwendung oder ein Feature zu installieren. Das Installationsprogramm fragt dann die Datenbank [*nach Informationen ab,*](i-gly.md) während das Ausführungsskript [*für*](e-gly.md) die Installation generiert wird. Weitere Informationen zu den Phasen einer Installation finden Sie unter [Installationsmechanismus](installation-mechanism.md).

</dd> <dt>

<span id="_msi_action_gly"></span><span id="_MSI_ACTION_GLY"></span>**Aktion**
</dt> <dd>

Viele der funktionen, die von Windows Installer werden in Aktionen gekapselt. Jede Aktion gibt die Ausführung einer bestimmten Funktion an, und der gesamte prozedurale Ablauf der Installation wird durch die Abfolge von Aktionen in den [*Sequenztabellen vorgegeben.*](s-gly.md) [*Standardaktionen*](s-gly.md) sind in Windows Installer. [*Benutzerdefinierte Aktionen*](c-gly.md) werden vom Autor des Installationspakets [*geschrieben.*](p-gly.md)

</dd> <dt>

<span id="_msi_admin_approval_mode_gly"></span><span id="_MSI_ADMIN_APPROVAL_MODE_GLY"></span>**Administratorgenehmigungsmodus**
</dt> <dd>

Der genehmigungsstatus, der durch den Benutzerkontenschutz (User Account Protection, UAC) aktiviert wird, der alle Benutzer mit den geringsten Berechtigungen einschließlich Administratoren ausführen kann. Benutzer müssen ihre Zustimmung zum Erhöhen von Installationen erteilen, für die Administratorrechte erforderlich sind.

</dd> <dt>

<span id="_msi_advertising_gly"></span><span id="_MSI_ADVERTISING_GLY"></span>**Werbung**
</dt> <dd>

Möglichkeit, die schnittstellen, die zum Laden erforderlich sind, und eine Anwendung verfügbar zu machen, ohne die Anwendung zu installieren. Wenn ein Benutzer oder eine Anwendung eine angekündigte Schnittstelle aktiviert, wird das Installationsprogramm mit der Installation der erforderlichen Komponenten fortgesetzt. Die beiden Arten der Werbung sind das [*Zuweisen und*](/windows) [*Veröffentlichen von*](p-gly.md). Weitere Informationen finden Sie unter [*install-on-demand*](i-gly.md). Weitere Informationen zur Ankündigung von Anwendungen durch das Installationsprogramm finden Sie unter [Ankündigung](advertisement.md)von .

</dd> <dt>

<span id="_msi_application_information_service_gly"></span><span id="_MSI_APPLICATION_INFORMATION_SERVICE_GLY"></span>**Application Information Service (III)**
</dt> <dd>

Ein Systemdienst von Windows Vista, der das Starten von Installationen erleichtert, für deren Ausführung erhöhte Rechte erforderlich sind. Stellt die Zustimmungsbenutzeroberfläche zur Verfügung, die von der Benutzerkontensteuerung verwendet wird, um einen Benutzer zur Administratorautorisierung aufforderungen.

</dd> <dt>

<span id="_msi_assigning_gly"></span><span id="_MSI_ASSIGNING_GLY"></span>**Zuweisen**
</dt> <dd>

Macht eine Anwendung verfügbar und sieht so aus, als wäre sie für einen Benutzer installiert worden, ohne sie tatsächlich zu installieren. Durch zuweisen werden dem Startmenü Verknüpfungen und Symbole hinzufügt, entsprechende Dateien zugeordnet und Registrierungseinträge für die Anwendung schreibt.  Wenn ein Benutzer versucht, eine zugewiesene Anwendung zu öffnen, installiert das Installationsprogramm die Anwendung. Das Zuweisen und [*Veröffentlichen sind*](p-gly.md) zwei Methoden zur [*Werbung*](/windows)von . Weitere Informationen finden Sie unter [Advertisement](advertisement.md).

</dd> <dt>

<span id="_msi_asynchronous_execution_using_windows_installer_gly"></span><span id="_MSI_ASYNCHRONOUS_EXECUTION_USING_WINDOWS_INSTALLER_GLY"></span>**asynchrone Ausführung**
</dt> <dd>

[*Benutzerdefinierte Aktion,*](c-gly.md) bei der das Installationsprogramm separate Threads der benutzerdefinierten Aktion und der aktuellen Installation gleichzeitig ausgeführt. Weitere Informationen finden Sie unter [Synchrone und asynchrone benutzerdefinierte Aktionen.](synchronous-and-asynchronous-custom-actions.md)

</dd> </dl>

 

 
