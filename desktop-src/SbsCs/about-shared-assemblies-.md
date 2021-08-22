---
description: Eine freigegebene Assembly ist eine Assembly, die von mehreren Anwendungen auf dem Computer verwendet werden kann.
ms.assetid: E42688E0-83D8-4C64-98A8-1BE82E4348FA
title: Informationen zu freigegebenen Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a5db7f10ea5ffa6e04fd5cd905262eb026b4ca4c24309ffd4c53cb10f9df00b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142623"
---
# <a name="about-shared-assemblies"></a>Informationen zu freigegebenen Assemblys

Eine freigegebene Assembly ist eine Assembly, die von mehreren Anwendungen auf dem Computer verwendet werden kann. Auf Windows Vista und Windows XP [](about-side-by-side-assemblies-.md) können nebenseitige Assemblys als freigegebene Assemblys installiert werden. Freigegebene, gleichzeitige Assemblys werden nicht global im System registriert, sind aber global für Anwendungen verfügbar, die eine Abhängigkeit von der Assembly in [Manifesten angeben.](manifests.md) Mehrere Versionen von gleichzeitigen Assemblys können von verschiedenen Anwendungen gemeinsam genutzt werden, die gleichzeitig ausgeführt werden. Weitere Informationen finden Sie unter [Informationen zu isolierten Anwendungen und nebenseitigen Assemblys.](about-isolated-applications-and-side-by-side-assemblies.md) Beispielsweise werden die unterstützten [microsoft-nebenseitigen](supported-microsoft-side-by-side-assemblies.md) Assemblys, die mit Windows XP ausgeliefert werden, in der Regel von mehreren Anwendungen als freigegebene Assemblys verwendet.

Freigegebene, nebeneinander gespeicherte Assemblys werden im Ordner WinSxS installiert. Assemblyherausgeber, -anwendungen und -administratoren können die Version von abhängigkeitsseitigen Assemblys nach der Bereitstellung über die Konfiguration [ändern.](configuration.md) Freigegebene, nebeneinander ausgeführte Assemblys können durch ein Betriebssystemupdate oder durch ein Windows Installer-Paket installiert oder aktualisiert werden. Weitere Informationen finden Sie unter [Installation von Win32-Assemblys.](../msi/installation-of-win32-assemblies.md)

Vor der Windows XP wurden freigegebene Assemblys global registriert und im ordner Windows System installiert. In diesem Fall ist die neueste installierte Version der Assembly für jede Anwendung verfügbar, die daran gebunden ist. Eine side-by-side-Assembly kann auch als private Assembly für die exklusive Verwendung einer Anwendung installiert werden. Weitere Informationen finden Sie unter [Private Assemblys](/windows/desktop/Msi/private-assemblies).

 

 
