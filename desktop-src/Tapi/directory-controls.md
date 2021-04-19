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
# <a name="directory-controls"></a><span data-ttu-id="b0ede-104">Steuerelemente für Verzeichnisse</span><span class="sxs-lookup"><span data-stu-id="b0ede-104">Directory Controls</span></span>

<span data-ttu-id="b0ede-105">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b0ede-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b0ede-106">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="b0ede-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="b0ede-107">Das folgende Diagramm zeigt die Hauptobjekte, die an den Verzeichnis Steuerelementen TAPI 3 Rendezvous beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="b0ede-107">The following diagram illustrates the main objects involved in TAPI 3 Rendezvous directory controls.</span></span> <span data-ttu-id="b0ede-108">Die angezeigten Schnittstellen sind mit den relevanten Referenzseiten hyperverknüpft.</span><span class="sxs-lookup"><span data-stu-id="b0ede-108">Interfaces shown are hyperlinked into the relevant reference pages.</span></span>

![Rendezvous-Verzeichnis Steuerungs Objekte und-Schnittstellen](images/renddir.png)

<span data-ttu-id="b0ede-110">Die zentrale Verzeichnis Steuerungs Schnittstelle ist [**itrendezvous**](/windows/desktop/api/Rend/nn-rend-itrendezvous). diese muss durch Aufrufen von **CoCreateInstance** erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b0ede-110">The main directory control interface is [**ITRendezvous**](/windows/desktop/api/Rend/nn-rend-itrendezvous), which must be created by calling **CoCreateInstance**.</span></span> <span data-ttu-id="b0ede-111">Das Rendezvous-Objekt macht Methoden verfügbar, mit denen Listen verfügbarer Verzeichnisse und neue Verzeichnisse oder Verzeichnisobjekte erstellt werden können.</span><span class="sxs-lookup"><span data-stu-id="b0ede-111">The Rendezvous object exposes methods to get lists of available directories and to create new directories or directory objects.</span></span>

<span data-ttu-id="b0ede-112">Ein Verzeichnis befindet sich auf einem Server und stellt eine Liste von Verzeichnis Objekten sowie beschreibende Informationen dar.</span><span class="sxs-lookup"><span data-stu-id="b0ede-112">A directory resides on a server and is a list of directory objects along with descriptive information.</span></span> <span data-ttu-id="b0ede-113">Mit [**itdirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory) verknüpfte Methoden können Informationen erhalten, die dem Verzeichnis als Ganzes zugeordnet sind, z. b. ob es sich um ein ILS-Verzeichnis handelt.</span><span class="sxs-lookup"><span data-stu-id="b0ede-113">Methods associated with [**ITDirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory) can get information associated with the directory as a whole, such as whether it is an ILS directory.</span></span>

<span data-ttu-id="b0ede-114">Ein Verzeichnis Objekt kann eine Konferenz oder einen Benutzer darstellen.</span><span class="sxs-lookup"><span data-stu-id="b0ede-114">A directory object can represent a conference or a user.</span></span> <span data-ttu-id="b0ede-115">Die [**itdirectoryobject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject) -Schnittstelle stellt Methoden bereit, mit denen Informationen generisch für ein Verzeichnis Objekt, z. b. die Adresse, abgerufen oder geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="b0ede-115">The [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject) interface supplies methods that can retrieve or modify information generic to a directory object, such as the dialable address.</span></span>

<span data-ttu-id="b0ede-116">Konferenz-und Benutzerinformationen, wie z. b. die URL einer Konferenz oder das primäre IP-Telefon eines Benutzers, werden mithilfe der Methoden in den Schnittstellen [**itdirectoryobjectconference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference) und [**itdirectoryobjectuser**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectuser) bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="b0ede-116">Conference and user information, such as the URL of a conference or the primary IP phone of a user, is manipulated by methods provided in the [**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference) and [**ITDirectoryObjectUser**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectuser) interfaces.</span></span>

 

 



