---
description: Isolierte Anwendungen sind selbst beschreibende Anwendungen, die mit Manifesten installiert werden. Isolierte Anwendungen können sowohl private als auch freigegebene Assemblys verwenden.
ms.assetid: 66c65b92-7c49-4932-b8c5-91b20fb0a038
title: Isolierte Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10c1b3f175ec05751bfc84e3826b19c9c9db01f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484635"
---
# <a name="isolated-applications"></a>Isolierte Anwendungen

Isolierte Anwendungen sind selbst beschreibende Anwendungen, die mit [Manifesten](manifests.md)installiert werden. Isolierte Anwendungen können sowohl [private](/windows/desktop/Msi/private-assemblies) als auch frei [gegebene](/windows/desktop/Msi/shared-assemblies)Assemblys verwenden.

Eine Anwendung gilt als vollständig isoliert, wenn alle zugehörigen Komponenten entweder frei [gegebene parallele](about-side-by-side-assemblies-.md) Assemblys oder private Assemblys sind. Sie wird teilweise isoliert aufgerufen, wenn einige Komponenten verwendet werden, die keine parallelen Assemblys sind. Beachten Sie Folgendes: Wenn eine Anwendung einige Komponenten verwendet, die keine parallelen Assemblys sind, oder private Assemblys verwendet, kann die Anwendung von der Installation oder Entfernung anderer Anwendungen im System betroffen sein. Weitere Informationen finden Sie unter [](side-by-side-assembly-sharing.md)parallele assemblyfreigabe.

Entwicklern wird empfohlen, isolierte Anwendungen zu entwerfen und vorhandene Anwendungen aus folgenden Gründen in isolierte Anwendungen zu aktualisieren:

-   Isolierte Anwendungen sind stabiler und zuverlässiger aktualisiert, da Sie von der Installation, Entfernung oder Aktualisierung anderer Anwendungen auf dem System nicht betroffen sind.
-   Isolierte Anwendungen können so entworfen werden, dass Sie immer mit denselben Assemblyversionen ausgeführt werden, mit denen Sie erstellt und getestet wurden.
-   Isolierte Anwendungen können Funktionen nutzen, die von den parallelen Assemblys bereitgestellt werden, die von Microsoft zur Verfügung gestellt werden. Weitere Informationen finden Sie [unter Unterstützte](supported-microsoft-side-by-side-assemblies.md)parallele Assemblys von Microsoft.
-   Isolierte Anwendungen sind nicht an den Versand Zeitplan ihrer parallelen Assemblys gebunden, da Anwendungen und Administratoren die Konfiguration nach der Bereitstellung aktualisieren können, ohne die Anwendung neu installieren zu müssen. Dies gilt nicht für den Fall, dass nur eine Version der Assembly verfügbar gemacht wird.
-   Eine vollständig isolierte Anwendung kann mit dem **xcopy** -Befehl installiert werden. [Windows Installer](../msi/windows-installer-portal.md) können auch verwendet werden, um eine isolierte Anwendung ohne Auswirkung auf die Registrierung zu installieren. Weitere Informationen finden Sie unter [Installieren von Win32](../msi/installation-of-win32-assemblies.md)-Assemblys.

In einigen Fällen können vorhandene Anwendungen in eine isolierte Anwendung aktualisiert werden, ohne dass der Anwendungscode neu geschrieben werden muss. Ein [Anwendungs Manifest](application-manifests.md) kann erstellt werden, in dem die Abhängigkeiten der Anwendung [von parallelen](about-side-by-side-assemblies-.md)Assemblys beschrieben werden. Wenn die Anwendung Komponenten verwendet, die keine parallelen Assemblys sind, können diese als [private](/windows/desktop/Msi/private-assemblies)Assemblys bereitgestellt werden. Beachten Sie, dass die Möglichkeit, dies mit Komponenten von Drittanbietern zu tun, möglicherweise von der Lizenzierung abhängig ist, da die Komponente als Assembly erstellt werden muss. Wenn Sie z. b. ein Anwendungs Manifest erstellen und eine Abhängigkeit von den parallelen allgemeinen Steuerelementen (Comctl32) angeben, kann eine Anwendung, die *unter Windows XP* ausgeführt wird, Windows-Designs nutzen. Sie sollten Ihre Anwendung immer testen, um sicherzustellen, dass Sie mit der neuen Version der ComCtl32-Assembly kompatibel ist.

Möglicherweise ist es nicht möglich, jede vorhandene Anwendung in eine vollständig isolierte Anwendung zu aktualisieren. Beispielsweise sind einige [Systemassemblys für den Windows-Datei Schutz (WFP)](/windows/desktop/Wfp/windows-resource-protection-portal) nicht als parallele Assemblys verfügbar und können nicht mit der Anwendung als private Assembly installiert werden. Es kann möglich sein, solche Anwendungen teilweise zu isolieren, indem Sie parallele Assemblyabhängigkeiten für einige Assemblys der Anwendung in einem Anwendungs Manifest angeben.

 

 
