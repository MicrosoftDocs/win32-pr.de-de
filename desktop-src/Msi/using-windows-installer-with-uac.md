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

Windows Das Installationsprogramm entspricht der Benutzerkontensteuerung (User [*Account Control,*](u-gly.md) UAC) in Windows Vista. Mit der Autorisierung durch einen Administrator kann der Windows Installer Anwendungen oder Patches im Namen eines Benutzers installieren, der möglicherweise kein Mitglied der Gruppe "Administratoren" ist. Dies wird als Installation mit [*erhöhten Rechten*](e-gly.md) bezeichnet, da der Windows Installer Änderungen am System im Namen des Benutzers vornimmt, die normalerweise nicht zulässig wären, wenn der Benutzer die Änderungen direkt vornehmen würde.

-   Wenn Sie Windows Vista in einer Unternehmensumgebung verwenden, können Anwendungen als verwaltete Anwendungen festgelegt werden. Mithilfe der Anwendungsbereitstellung und [Gruppenrichtlinie](/previous-versions/windows/desktop/Policy/group-policy-start-page)können Administratoren Verzeichnisse sperren und dann die verwalteten Anwendungen in diesen Verzeichnissen [*Standardbenutzern*](s-gly.md) zum Installieren, Reparieren oder Entfernen zuweisen oder veröffentlichen. Verwaltete Anwendungen werden in der **Registrierungsstruktur HKEY \_ LOCAL \_ MACHINE** registriert. Nachdem eine Anwendung als verwaltete Anwendung registriert wurde, werden nachfolgende Installationsvorgänge immer mit erhöhten Rechten ausgeführt. Wenn der Benutzer als Administrator ausgeführt wird, ist keine Aufforderung erforderlich, um die Installation fortzusetzen. Wenn der Benutzer als Standardbenutzer ausgeführt wird und die Anwendung bereits zugewiesen oder veröffentlicht wurde, kann die Installation der verwalteten Anwendung ohne Aufforderung fortgesetzt werden.
-   Wenn Sie Windows Vista in einer Nicht-Unternehmensumgebung verwenden, übernimmt die UAC die Erhöhung der Anwendungsinstallation. Windows Installer 4.0 kann den [*Application Information Service*](a-gly.md) (CSV) aufrufen, um eine Administratorautorisierung anzufordern, um eine Installation zu erhöhen. Bevor eine Installation ausgeführt werden kann, die administratorrechte erfordert, fordert die Benutzerkontenverwaltung den Benutzer zur Zustimmung auf, um die Installation zu erhöhen. Die Zustimmungsaufforderung wird standardmäßig angezeigt, auch wenn der Benutzer Mitglied der lokalen Administratorengruppe ist, da Administratoren als Standardbenutzer ausgeführt werden, bis eine Anwendung oder Systemkomponente, die Administratoranmeldeinformationen erfordert, die Berechtigung für die Ausführung anfordert. Diese Benutzeroberfläche wird als [*Administratorgenehmigungsmodus (Admin Approval Mode,*](a-gly.md) AAM) bezeichnet. Wenn ein Standardbenutzer versucht, die Anwendung zu installieren, muss der Benutzer eine Person mit Administratorrechten abrufen, um seine Administratoranmeldeinformationen bereitzustellen, um die Installation fortzusetzen. Diese Benutzeroberfläche wird als Eingabeaufforderung für Ots-Anmeldeinformationen [*(Over the Shoulder)*](o-gly.md) bezeichnet.
-   Da UAC Berechtigungen während der Phasen einer Installation einschränkt, sollten Entwickler von Windows Installer-Paketen nicht davon ausgehen, dass ihre Installation immer Zugriff auf alle Teile des Systems hat. Windows Entwickler von Installerpaketen sollten daher die in [Richtlinien für Pakete](guidelines-for-packages.md) beschriebenen Paketrichtlinien einhalten, um sicherzustellen, dass ihr Paket mit UAC und Windows Vista funktioniert. Ein Paket, das erstellt und getestet wurde, um die UAC zu erfüllen, sollte die [**MSIDEPLOYMENTCOMPLIANT-Eigenschaft**](msideploymentcompliant.md) enthalten, die auf 1 festgelegt ist.
-   Ein Administrator kann auch die im Abschnitt [Installieren eines Pakets mit erhöhten Rechten für einen Nichtadministrator beschriebenen](installing-a-package-with-elevated-privileges-for-a-non-admin.md) Methoden verwenden, um einem Benutzer ohne Administratorrechte das Installieren einer Anwendung mit erhöhten Systemberechtigungen zu ermöglichen.
-   Berechtigungen sind erforderlich, um eine Anwendung im benutzerbezogenen verwalteten Kontext zu installieren. Daher werden nachfolgende Windows Installationsprogramme oder Reparaturen der Anwendung auch vom Installationsprogramm mit erhöhten Rechten ausgeführt. Dies bedeutet, dass nur Patches aus vertrauenswürdigen Quellen auf eine Anwendung im benutzerbezogenen verwalteten Zustand angewendet werden können. Ab Windows Installer 3.0 können Sie einen Patch auf eine benutzerspezifische verwaltete Anwendung anwenden, nachdem der Patch mit erhöhten Rechten registriert wurde. Weitere Informationen finden Sie unter [Patchen von Per-User verwalteten Anwendungen.](patching-per-user-managed-applications.md)

> [!Note]  
> Wenn für die Installation eines Windows Installer-Pakets keine erhöhten Berechtigungen erforderlich sind, kann der Ersteller des Pakets das Dialogfeld unterdrücken, das von der Benutzeroberflächenverwaltung angezeigt wird, um Benutzer zur Administratorautorisierung aufzufordern. Weitere Informationen finden Sie unter [Erstellen von Paketen ohne das UAC-Dialogfeld](authoring-packages-without-the-uac-dialog-box.md).

 

 

 
