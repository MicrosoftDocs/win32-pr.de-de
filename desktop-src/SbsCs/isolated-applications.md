---
description: Isolierte Anwendungen sind selbstbeschreibende Anwendungen, die mit Manifesten installiert sind. Isolierte Anwendungen können sowohl private Assemblys als auch freigegebene Assemblys verwenden.
ms.assetid: 66c65b92-7c49-4932-b8c5-91b20fb0a038
title: Isolierte Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78abe13dc452c81b2a763706036e1f59400f31ccd138c95a9ab241481898aee6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142123"
---
# <a name="isolated-applications"></a>Isolierte Anwendungen

Isolierte Anwendungen sind selbstbeschreibende Anwendungen, die mit [Manifesten installiert werden.](manifests.md) Isolierte Anwendungen können sowohl [private Assemblys als auch](/windows/desktop/Msi/private-assemblies) [freigegebene Assemblys verwenden.](/windows/desktop/Msi/shared-assemblies)

Eine Anwendung wird als vollständig isoliert betrachtet, [](about-side-by-side-assemblies-.md) wenn es sich bei allen Komponenten um gemeinsam genutzte und private Assemblys handelt. Sie wird als teilweise isoliert bezeichnet, wenn einige Komponenten verwendet werden, die keine nebeneinander seitigen Assemblys sind. Beachten Sie Folgendes: Wenn eine Anwendung einige Komponenten verwendet, die keine nebenseitigen Assemblys sind, oder private Assemblys verwendet, kann dies von der Installation oder Entfernung anderer Anwendungen auf dem System betroffen sein. Weitere Informationen finden Sie unter [Side-by-side Assembly Sharing](side-by-side-assembly-sharing.md).

Entwicklern wird empfohlen, isolierte Anwendungen zu entwerfen und vorhandene Anwendungen aus den folgenden Gründen in isolierte Anwendungen zu aktualisieren:

-   Isolierte Anwendungen sind stabiler und zuverlässiger aktualisiert, da sie von der Installation, Entfernung oder dem Upgrade anderer Anwendungen auf dem System nicht betroffen sind.
-   Isolierte Anwendungen können so entworfen werden, dass sie immer mit den gleichen Assemblyversionen ausgeführt werden, mit denen sie erstellt und getestet wurden.
-   Isolierte Anwendungen können Funktionen verwenden, die von den von Microsoft zur Verfügung gestellten nebenseitigen Assemblys bereitgestellt werden. Weitere Informationen finden Sie unter [Supported Microsoft Side-by-side Assemblies](supported-microsoft-side-by-side-assemblies.md).
-   Isolierte Anwendungen sind nicht an den Versandzeitplan ihrer nebenseitigen Assemblys gebunden, da Anwendungen und Administratoren die Konfiguration nach der Bereitstellung aktualisieren können, ohne die Anwendung neu installieren zu müssen. Dies gilt nicht, wenn nur eine Version der Assembly verfügbar gemacht wird.
-   Eine vollständig isolierte Anwendung kann mit dem Befehl **xcopy installiert** werden. [Windows Installer](../msi/windows-installer-portal.md) kann auch verwendet werden, um eine isolierte Anwendung ohne Auswirkungen auf die Registrierung zu installieren. Weitere Informationen finden Sie unter [Installation von Win32-Assemblys.](../msi/installation-of-win32-assemblies.md)

In einigen Fällen können vorhandene Anwendungen in eine isolierte Anwendung aktualisiert werden, ohne den Anwendungscode neu schreiben zu müssen. Es [kann ein Anwendungsmanifest](application-manifests.md) erstellt werden, das die Abhängigkeiten der Anwendung von [nebenseitigen Assemblys beschreibt.](about-side-by-side-assemblies-.md) Wenn die Anwendung Komponenten verwendet, die keine nebenseitigen Assemblys sind, können diese als private [Assemblys bereitgestellt werden.](/windows/desktop/Msi/private-assemblies) Beachten Sie, dass die Möglichkeit, dies mit Drittanbieterkomponenten zu tun, von der Lizenzierung abhängen kann, da die Komponente als Assembly erstellen muss. Wenn Sie z. B. ein Anwendungsmanifest erstellen und eine Abhängigkeit von den nebenseitigen allgemeinen Steuerelementen (COMCTL32) angeben, kann eine Anwendung, die unter Windows XP ausgeführt wird, die Vorteile *Windows-Theming nutzen.* Sie sollten Ihre Anwendung immer testen, um sicherzustellen, dass sie mit der neuen Version der COMCTL32-Assembly kompatibel ist.

Es ist möglicherweise nicht möglich, jede vorhandene Anwendung in eine vollständig isolierte Anwendung zu aktualisieren. Beispielsweise sind einige Windows File Protection -Systemassemblys [(WFP)](/windows/desktop/Wfp/windows-resource-protection-portal) nicht als nebenseitige Assemblys verfügbar und können nicht mit der Anwendung als private Assembly installiert werden. Es kann möglich sein, solche Anwendungen teilweise zu isolieren, indem Sie für einige der Anwendungsassemblys in einem Anwendungsmanifest abhängigkeiten von Assemblys angeben.

 

 
