---
description: Windows Das Installationsprogramm entspricht der Benutzerkontensteuerung (User Account Control, UAC) in Windows Vista.
ms.assetid: 13955ded-6b7f-475f-bb0f-6530a0b4963f
title: Verwenden Windows Installers mit UAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 458d6265938f44a694366e8145d60aa5d031d47e715932502bd1b82e7012b87f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942280"
---
# <a name="using-windows-installer-with-uac"></a>Verwenden Windows Installers mit UAC

Windows Das Installationsprogramm entspricht der Benutzerkontensteuerung (User [*Account Control,*](u-gly.md) UAC) in Windows Vista. Mit der Autorisierung durch einen Administrator kann der Windows Installer Anwendungen oder Patches im Namen eines Benutzers installieren, der möglicherweise kein Mitglied der Gruppe "Administratoren" ist. Dies wird als [](e-gly.md) Installation mit erhöhten Rechten bezeichnet, da der Windows-Installer Änderungen am System im Namen des Benutzers vorsingt, die normalerweise nicht zulässig wären, wenn der Benutzer die Änderungen direkt vornehmen würde.

-   Wenn Sie Windows Vista in einer Unternehmensumgebung verwenden, können Anwendungen als verwaltete Anwendungen festgelegt werden. Mithilfe der Anwendungsbereitstellung und [Gruppenrichtlinie](/previous-versions/windows/desktop/Policy/group-policy-start-page)können Administratoren Verzeichnisse sperren und dann die verwalteten [](s-gly.md) Anwendungen in diesen Verzeichnissen Standardbenutzern zum Installieren, Reparieren oder Entfernen zuweisen oder veröffentlichen. Verwaltete Anwendungen werden in der **Registrierungsstruktur HKEY \_ LOCAL \_ MACHINE** registriert. Sobald eine Anwendung als verwaltete Anwendung registriert wurde, werden nachfolgende Installationsvorgänge immer mit erhöhten Rechten ausgeführt. Wenn der Benutzer als Administrator ausgeführt wird, ist keine Aufforderung erforderlich, um die Installation fortsetzen zu können. Wenn der Benutzer als Standardbenutzer ausgeführt wird und die Anwendung bereits zugewiesen oder veröffentlicht wurde, kann die Installation der verwalteten Anwendung ohne Aufforderung fortgesetzt werden.
-   Wenn Sie Windows Vista in einer Nicht-Unternehmensumgebung verwenden, übernimmt die UAC die Erhöhung der Anwendungsinstallation. Windows Installer 4.0 kann den [*Application Information Service*](a-gly.md) aufrufen, um die Administratorautorisierung zum Erhöhen einer Installation an fordern. Bevor eine Installation ausgeführt werden kann, für die Administratorrechte erforderlich sind, fordert UAC den Benutzer zur Zustimmung auf, die Installation zu erhöhen. Die Zustimmungsaufforderung wird standardmäßig angezeigt, auch wenn der Benutzer Mitglied der lokalen Administratorengruppe ist, da Administratoren als Standardbenutzer ausgeführt werden, bis eine Anwendung oder Systemkomponente, für die administrative Anmeldeinformationen erforderlich sind, die Berechtigung zum Ausführen anfordert. Diese Benutzeroberfläche wird als [*Administratorgenehmigungsmodus*](a-gly.md) (Admin Approval Mode, AAM) bezeichnet. Wenn ein Standardbenutzer versucht, die Anwendung zu installieren, muss der Benutzer eine Person mit Administratorrechten erhalten, um ihre Administratoranmeldeinformationen anzugeben, um die Installation fortsetzen zu können. Diese Benutzeroberfläche wird als Over-the-Shoulder-Anmeldeinformationsaufforderung (Over [*the Shoulder,*](o-gly.md) OTS) bezeichnet.
-   Da UAC Berechtigungen während der Phasen einer Installation einschränkt, sollten Entwickler von Windows Installer-Paketen nicht davon ausgehen, dass ihre Installation immer Zugriff auf alle Teile des Systems hat. Windows Entwickler von Installerpaketen sollten daher die [](guidelines-for-packages.md) unter Richtlinien für Pakete beschriebenen Paketrichtlinien einhalten, um sicherzustellen, dass ihr Paket mit UAC und Windows Vista funktioniert. Ein Paket, das für die Einhaltung der UAC erstellt und getestet wurde, sollte die [**MSIDEPLOYMENTCOMPLIANT-Eigenschaft**](msideploymentcompliant.md) enthalten, die auf 1 festgelegt ist.
-   Ein Administrator kann auch die im Abschnitt Installieren eines [Pakets](installing-a-package-with-elevated-privileges-for-a-non-admin.md) mit erhöhten Rechten für einen Nichtadministrator beschriebenen Methoden verwenden, um einem Benutzer ohne Administratorrechte die Installation einer Anwendung mit erhöhten Systemberechtigungen zu ermöglichen.
-   Berechtigungen sind erforderlich, um eine Anwendung im benutzerspezifischen verwalteten Kontext zu installieren. Daher werden nachfolgende Neuinstallationen oder Reparaturen des Windows-Installers der Anwendung auch vom Installationsprogramm mit erhöhten Rechten ausgeführt. Dies bedeutet, dass nur Patches aus vertrauenswürdigen Quellen auf eine Anwendung im vom Benutzer verwalteten Zustand angewendet werden können. Ab Windows Installer 3.0 können Sie einen Patch auf eine benutzerspezifische verwaltete Anwendung anwenden, nachdem der Patch als mit erhöhten Rechten registriert wurde. Weitere Informationen finden Sie [unter Patchen Per-User Verwalteten Anwendungen](patching-per-user-managed-applications.md).

> [!Note]  
> Wenn erhöhte Rechte zum Installieren eines Windows Installer-Pakets nicht erforderlich sind, kann der Autor des Pakets das Dialogfeld unterdrücken, das von der UAC angezeigt wird, um Benutzer zur Administratorautorisierung aufforderungen. Weitere Informationen finden Sie unter [Erstellen von Paketen ohne das UAC-Dialogfeld](authoring-packages-without-the-uac-dialog-box.md).

 

 

 
