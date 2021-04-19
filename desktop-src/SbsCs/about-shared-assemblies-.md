---
description: Eine freigegebene Assembly ist eine Assembly, die von mehreren Anwendungen auf dem Computer verwendet werden kann.
ms.assetid: E42688E0-83D8-4C64-98A8-1BE82E4348FA
title: Info
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed044f2c0f6b8e8e04927035991da651b4c26674
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349838"
---
# <a name="about-shared-assemblies"></a>Info

Eine freigegebene Assembly ist eine Assembly, die von mehreren Anwendungen auf dem Computer verwendet werden kann. Unter Windows Vista und Windows XP können parallele Assemblys als [frei](about-side-by-side-assemblies-.md) gegebene Assemblys installiert werden. Freigegebene parallele Assemblys werden nicht global auf dem System registriert, Sie sind jedoch global für Anwendungen verfügbar, die eine Abhängigkeit von der Assembly in [Manifesten](manifests.md)angeben. Mehrere Versionen paralleler Assemblys können von verschiedenen Anwendungen, die gleichzeitig ausgeführt werden, gemeinsam genutzt werden. Weitere Informationen finden Sie unter Informationen [zu isolierten Anwendungen und](about-isolated-applications-and-side-by-side-assemblies.md)parallelen Assemblys. Beispielsweise werden die [unterstützten parallelen Microsoft-](supported-microsoft-side-by-side-assemblies.md) Assemblys, die mit Windows XP ausgeliefert werden, in der Regel von mehreren Anwendungen als freigegebene Assemblys verwendet.

Freigegebene parallele Assemblys werden im Ordner WinSxS installiert. Assemblerverleger,-Anwendungen und-Administratoren können die Version der parallelen Assemblyabhängigkeiten nach der Bereitstellung über die [Konfiguration](configuration.md)ändern. Freigegebene parallele Assemblys können mithilfe eines Betriebssystemupdates oder eines Windows Installer Pakets installiert werden, mit dem eine Anwendung installiert oder aktualisiert wird. Weitere Informationen finden Sie unter [Installieren von Win32](../msi/installation-of-win32-assemblies.md)-Assemblys.

Vor Windows XP wurden freigegebene Assemblys global registriert und im Windows-System Ordner installiert. In diesem Fall ist die neueste installierte Version der Assembly für jede Anwendung verfügbar, die an Sie gebunden ist. Eine parallele Assembly kann auch als private Assembly für die ausschließliche Verwendung einer Anwendung installiert werden. Weitere Informationen finden Sie unter [Private Assemblys](/windows/desktop/Msi/private-assemblies).

 

 
