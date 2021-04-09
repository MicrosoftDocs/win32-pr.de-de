---
description: Windows Installer entspricht der Benutzerkontensteuerung (User Account Control, UAC) in Windows Vista.
ms.assetid: 13955ded-6b7f-475f-bb0f-6530a0b4963f
title: Verwenden von Windows Installer mit UAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a05dcd2fb33eff24fb17702af1cb306f81002d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130268"
---
# <a name="using-windows-installer-with-uac"></a>Verwenden von Windows Installer mit UAC

Windows Installer entspricht der [*Benutzerkontensteuerung (User Account Control*](u-gly.md) , UAC) in Windows Vista. Mithilfe der Autorisierung durch einen Administrator können die Windows Installer Anwendungen oder Patches im Auftrag eines Benutzers installieren, der möglicherweise nicht Mitglied der Gruppe "Administratoren" ist. Dies [*wird als erweiterte Installation bezeichnet*](e-gly.md) , da der Windows Installer im Auftrag des Benutzers Änderungen am System vornimmt, die normalerweise nicht zulässig sind, wenn der Benutzer die Änderungen direkt vornimmt.

-   Bei Verwendung von Windows Vista in einer Unternehmensumgebung können Anwendungen als verwaltete Anwendungen festgelegt werden. Mithilfe der Anwendungs Bereitstellung und- [Gruppenrichtlinie](/previous-versions/windows/desktop/Policy/group-policy-start-page)können Administratoren Verzeichnisse Sperren und die in diesen Verzeichnissen verwalteten Anwendungen dann den [*Standard Benutzern*](s-gly.md) zur Installation, Reparatur oder Entfernung zuweisen oder veröffentlichen. Verwaltete Anwendungen werden in der Registrierungs Struktur des **\_ lokalen \_ HKEY** -Computers registriert. Sobald eine Anwendung als verwaltete Anwendung registriert wurde, werden nachfolgende Installations Vorgänge immer mit erhöhten Rechten ausgeführt. Wenn der Benutzer als Administrator ausgeführt wird, ist keine Eingabeaufforderung erforderlich, um die Installation fortzusetzen. Wenn der Benutzer als Standardbenutzer ausgeführt wird und die Anwendung bereits zugewiesen oder veröffentlicht wurde, kann die Installation der verwalteten Anwendung ohne Aufforderung fortgesetzt werden.
-   Wenn Sie Windows Vista in einer Umgebung verwenden, die nicht im Unternehmen verwendet wird, übernimmt UAC die Erhöhung der Anwendungs Installation. Windows Installer 4,0 kann den [*Anwendungs Informationsdienst (Application Information Service*](a-gly.md) , AIS) anrufen, um die Administrator Autorisierung zum herauf Stufen einer Installation anzufordern. Bevor eine Installation, die erfordert, dass Administratorrechte erforderlich sind, ausgeführt werden kann, fordert UAC den Benutzer zur Zustimmung auf, um die Installation zu erhöhen. Die Zustimmungsaufforderung wird standardmäßig angezeigt, auch wenn der Benutzer ein Mitglied der lokalen Administrator Gruppe ist, da Administratoren so lange als Standardbenutzer ausgeführt werden, bis eine Anwendung oder Systemkomponente, für die administrative Anmelde Informationen erforderlich sind, die Berechtigung zum Ausführen von anfordert. Diese Benutzer Darstellung wird als [*Admin Approval Mode*](a-gly.md) (AAM) bezeichnet. Wenn ein Standardbenutzer versucht, die Anwendung zu installieren, muss der Benutzer eine Person mit Administrator Berechtigung erhalten, um ihm die Administrator Anmelde Informationen zur Verfügung zu stellen, um die Installation fortzusetzen. Diese Benutzer Darstellung wird als Eingabeaufforderung für [*die*](o-gly.md) Eingabeaufforderung (OTS) bezeichnet.
-   Da UAC in den Phasen einer Installation Berechtigungen einschränkt, sollten Entwickler von Windows Installer Paketen nicht davon ausgehen, dass Ihre Installation immer Zugriff auf alle Teile des Systems hat. Entwickler von Windows Installer Paketen sollten daher die in den [Richtlinien für Pakete](guidelines-for-packages.md) beschriebenen Paket Richtlinien befolgen, um sicherzustellen, dass Ihr Paket mit UAC und Windows Vista funktioniert. Ein Paket, das erstellt und für die Einhaltung der UAC getestet wurde, sollte die [**msideploymentcompliance**](msideploymentcompliant.md) -Eigenschaft auf 1 festgelegt haben.
-   Ein Administrator kann auch die Methoden verwenden, die im Abschnitt " [Installieren eines Pakets mit erhöhten Rechten für einen nicht-](installing-a-package-with-elevated-privileges-for-a-non-admin.md) Administrator" beschrieben sind, um einem Benutzer ohne Administratorrechte die Installation einer Anwendung mit erhöhten System Berechtigungen zu ermöglichen.
-   Berechtigungen sind erforderlich, um eine Anwendung im Benutzer verwalteten Kontext zu installieren. Daher werden nachfolgende Windows Installer Neuinstallationen oder Reparaturen der Anwendung auch durch das Installationsprogramm mit erhöhten Rechten ausgeführt. Dies bedeutet, dass nur Patches aus vertrauenswürdigen Quellen auf eine Anwendung im Benutzer verwalteten Zustand angewendet werden können. Ab Windows Installer 3,0 können Sie einen Patch für eine pro Benutzer verwaltete Anwendung anwenden, nachdem der Patch als erweiterte Berechtigungen registriert wurde. Weitere Informationen finden Sie unter [Patchen Per-User verwaltete Anwendungen](patching-per-user-managed-applications.md).

> [!Note]  
> Wenn für die Installation eines Windows Installer Pakets erweiterte Berechtigungen nicht erforderlich sind, kann der Autor des Pakets das von der UAC angeforderte Dialogfeld unterdrücken, um Benutzer zur Administrator Autorisierung aufzufordern. Weitere Informationen finden Sie unter [Erstellen von Paketen ohne das UAC-Dialog Feld](authoring-packages-without-the-uac-dialog-box.md).

 

 

 
