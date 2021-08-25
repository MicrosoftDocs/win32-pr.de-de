---
description: Manifeste sind XML-Dateien, die nebeneinander gespeicherte Assemblys oder isolierte Anwendungen begleiten und beschreiben.
ms.assetid: 53c4c2e6-fff9-4506-b7e0-d091d2ec9883
title: Manifeste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 974aaea3dad60c80456d0acd085d610c81b93716342962abcd465adaf9efdf48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119977210"
---
# <a name="manifests"></a>Manifeste

Manifeste sind XML-Dateien, die nebeneinander gespeicherte Assemblys oder isolierte Anwendungen begleiten und beschreiben. Manifeste identifizieren die Assembly eindeutig über das **assemblyIdentity-Element der** Assembly. Sie enthalten Informationen, die für die Bindung und Aktivierung verwendet werden, z. B. COM-Klassen, Schnittstellen und Typbibliotheken, die traditionell in der Registrierung gespeichert wurden. Manifeste geben auch die Dateien an, aus denen die Assembly Windows, wenn der Assemblyautor möchte, dass sie versioniert werden. Gleichzeitige Assemblys werden nicht auf dem System registriert, sind aber für Anwendungen und andere Assemblys auf dem System verfügbar, die Abhängigkeiten in Manifestdateien angeben.

Manifestdateien ermöglichen Administratoren und Anwendungen das Verwalten von nebenseitigen Assemblyversionen nach der Bereitstellung. Jeder seiteseitigen Assembly muss ein Manifest zugeordnet sein. Bei der Installation Windows XP werden die unterstützten [microsoft-nebenseitigen](supported-microsoft-side-by-side-assemblies.md) Assemblys mit ihren Manifesten installiert. Wenn Sie ihre eigenen assemblyseitigen Assemblys entwickeln, müssen Sie auch Manifestdateien installieren. Weitere Informationen finden Sie unter [Installing Side-by-Side Assemblies](installing-side-by-side-assemblies.md) and Manifest Files Reference ( Installieren von nebenseitigen Assemblys und [Manifestdateien – Referenz).](manifest-files-reference.md)

Manifeste und Konfigurationsdateien werden nicht lokalisiert.

Die folgenden Manifesttypen werden mit nebeneinander verfügbaren Assemblys verwendet:

-   [Assemblymanifeste](assembly-manifests.md) beschreiben nebenseitige Assemblys. Sie werden verwendet, um die Namen, Versionen, Ressourcen und abhängigen Assemblys von nebenseitigen Assemblys zu verwalten. Die Manifeste [freigegebener Assemblys](/windows/desktop/Msi/shared-assemblies) werden im WinSxS-Ordner des Systems gespeichert. Private Assemblymanifeste werden entweder als Ressource in der DLL oder im Anwendungsordner gespeichert.
-   [Anwendungsmanifesten](application-manifests.md) beschreiben [isolierte Anwendungen.](isolated-applications.md) Sie werden verwendet, um die Namen und Versionen freigegebener, nebeneinander verwendeter Assemblys zu verwalten, an die die Anwendung zur Laufzeit gebunden werden soll. Anwendungsmanifeste werden in denselben Ordner wie die ausführbare Datei der Anwendung kopiert oder als Ressource in die ausführbare Datei der Anwendung aufgenommen.
-   [Anwendungskonfigurationsdateien](application-configuration-files.md)sind Manifeste, die zum Überschreiben und Umleiten der Versionen von abhängigen Assemblys verwendet werden, die von nebenseitigen Assemblys und Anwendungen verwendet werden.
-   [Publisher Konfigurationsdateien sind](publisher-configuration-files.md)Manifeste, die zum Umleiten der Version einer nebenseitigen Assembly zu einer anderen kompatiblen Version verwendet werden. Die Version, zu der die Assembly umgeleitet wird, sollte die gleichen Major.Minor-Werte wie die ursprüngliche Version haben.

 

 
