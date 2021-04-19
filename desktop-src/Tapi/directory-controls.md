---
description: Das folgende Diagramm zeigt die Hauptobjekte, die an den Verzeichnis Steuerelementen TAPI 3 Rendezvous beteiligt sind. Die angezeigten Schnittstellen sind mit den relevanten Referenzseiten hyperverknüpft.
ms.assetid: f5ca1d61-5266-4406-8199-338e6a712db8
title: Steuerelemente für Verzeichnisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87a7b9c0b11c76aac6067e1a3f67c3899552f1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357341"
---
# <a name="directory-controls"></a>Steuerelemente für Verzeichnisse

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Das folgende Diagramm zeigt die Hauptobjekte, die an den Verzeichnis Steuerelementen TAPI 3 Rendezvous beteiligt sind. Die angezeigten Schnittstellen sind mit den relevanten Referenzseiten hyperverknüpft.

![Rendezvous-Verzeichnis Steuerungs Objekte und-Schnittstellen](images/renddir.png)

Die zentrale Verzeichnis Steuerungs Schnittstelle ist [**itrendezvous**](/windows/desktop/api/Rend/nn-rend-itrendezvous). diese muss durch Aufrufen von **CoCreateInstance** erstellt werden. Das Rendezvous-Objekt macht Methoden verfügbar, mit denen Listen verfügbarer Verzeichnisse und neue Verzeichnisse oder Verzeichnisobjekte erstellt werden können.

Ein Verzeichnis befindet sich auf einem Server und stellt eine Liste von Verzeichnis Objekten sowie beschreibende Informationen dar. Mit [**itdirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory) verknüpfte Methoden können Informationen erhalten, die dem Verzeichnis als Ganzes zugeordnet sind, z. b. ob es sich um ein ILS-Verzeichnis handelt.

Ein Verzeichnis Objekt kann eine Konferenz oder einen Benutzer darstellen. Die [**itdirectoryobject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject) -Schnittstelle stellt Methoden bereit, mit denen Informationen generisch für ein Verzeichnis Objekt, z. b. die Adresse, abgerufen oder geändert werden können.

Konferenz-und Benutzerinformationen, wie z. b. die URL einer Konferenz oder das primäre IP-Telefon eines Benutzers, werden mithilfe der Methoden in den Schnittstellen [**itdirectoryobjectconference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference) und [**itdirectoryobjectuser**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectuser) bearbeitet.

 

 



