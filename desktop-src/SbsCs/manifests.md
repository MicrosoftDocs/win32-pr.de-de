---
description: Manifeste sind XML-Dateien, die parallele Assemblys oder isolierte Anwendungen begleiten und beschreiben.
ms.assetid: 53c4c2e6-fff9-4506-b7e0-d091d2ec9883
title: Manifeste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2536e518f39791b400b9e99002b9575f4428d64d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355652"
---
# <a name="manifests"></a>Manifeste

Manifeste sind XML-Dateien, die parallele Assemblys oder isolierte Anwendungen begleiten und beschreiben. Manifeste identifizieren die Assembly eindeutig über das **assemblyIdentity** -Element der Assembly. Sie enthalten Informationen, die für die Bindung und Aktivierung verwendet werden, wie z. b. com-Klassen, Schnittstellen und Typbibliotheken, die üblicherweise in der Registrierung gespeichert wurden. Manifeste geben auch die Dateien an, aus denen die Assembly besteht, und können Windows-Klassen enthalten, wenn Sie vom assemblyautor mit Versions Angabe versehen werden sollen. Parallele Assemblys sind nicht auf dem System registriert, stehen aber Anwendungen und anderen Assemblys auf dem System zur Verfügung, die Abhängigkeiten in Manifest-Dateien angeben.

Mithilfe von Manifest-Dateien können Administratoren und Anwendungen parallele Assemblyversionen nach der Bereitstellung verwalten. Jeder Seite-an-Seite-Assembly muss ein Manifest zugeordnet sein. Bei der Installation von Windows XP [werden die unterstützten](supported-microsoft-side-by-side-assemblies.md) parallelen Assemblys von Microsoft mit ihren Manifesten installiert. Wenn Sie Ihre eigenen parallelen Assemblys entwickeln, müssen Sie auch Manifest-Dateien installieren. Weitere Informationen finden Sie unter [Installieren](installing-side-by-side-assemblies.md) paralleler Assemblys und [Manifest-Dateireferenz](manifest-files-reference.md).

Manifeste und Konfigurationsdateien werden nicht lokalisiert.

Die folgenden Manifeste werden bei parallelen Assemblys verwendet:

-   [Assemblymanifeste](assembly-manifests.md) beschreiben parallele Assemblys. Sie werden verwendet, um die Namen, Versionen, Ressourcen und abhängigen Assemblys von parallelen Assemblys zu verwalten. Die Manifeste von frei [gegebenen](/windows/desktop/Msi/shared-assemblies) Assemblys werden im Ordner WinSxS des Systems gespeichert. Private Assemblymanifeste werden entweder als Ressource in der DLL oder im Anwendungsordner gespeichert.
-   [Anwendungs Manifeste](application-manifests.md) beschreiben [isolierte Anwendungen](isolated-applications.md). Sie werden verwendet, um die Namen und Versionen von freigegebenen parallelen Assemblys zu verwalten, an die die Anwendung zur Laufzeit binden soll. Anwendungs Manifeste werden in denselben Ordner wie die ausführbare Datei der Anwendung kopiert oder als Ressource in die ausführbare Datei der Anwendung eingefügt.
-   [Anwendungs Konfigurationsdateien](application-configuration-files.md)sind Manifeste, mit denen die Versionen abhängiger Assemblys außer Kraft gesetzt und umgeleitet werden, die von parallelen Assemblys und Anwendungen verwendet werden.
-   [Verleger Konfigurationsdateien](publisher-configuration-files.md)sind Manifeste, die verwendet werden, um die Version einer parallelen Assembly zu einer anderen kompatiblen Version umzuleiten. Die Version, zu der die Assembly umgeleitet wird, sollte die gleichen Major. Minor-Werte wie die ursprüngliche Version aufweisen.

 

 
