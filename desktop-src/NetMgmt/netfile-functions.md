---
title: Netfile-Funktionen (Netzwerkverwaltung)
description: Die Funktionen der Netzwerk Verwaltungs Datei bieten eine Möglichkeit zum Überwachen und Schließen der Datei, des Geräts und der Pipe-Ressourcen, die auf einem Server geöffnet sind. Die Dateifunktionen sind nachfolgend aufgeführt.
ms.assetid: 3cfb5222-7e02-4bc3-959e-0fc7bc4f0f19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46b56d1c6d50463989e64386f5829a8e663cddd4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104517306"
---
# <a name="netfile-functions-network-management"></a><span data-ttu-id="ec9eb-104">Netfile-Funktionen (Netzwerkverwaltung)</span><span class="sxs-lookup"><span data-stu-id="ec9eb-104">NetFile Functions (Network Management)</span></span>

<span data-ttu-id="ec9eb-105">Die Funktionen der Netzwerk Verwaltungs Datei bieten eine Möglichkeit zum Überwachen und Schließen der Datei, des Geräts und der Pipe-Ressourcen, die auf einem Server geöffnet sind.</span><span class="sxs-lookup"><span data-stu-id="ec9eb-105">The network management file functions provide a way to monitor and close the file, device, and pipe resources open on a server.</span></span> <span data-ttu-id="ec9eb-106">Die Dateifunktionen sind nachfolgend aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="ec9eb-106">The file functions are listed following.</span></span>



| <span data-ttu-id="ec9eb-107">Funktion</span><span class="sxs-lookup"><span data-stu-id="ec9eb-107">Function</span></span>                                | <span data-ttu-id="ec9eb-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ec9eb-108">Description</span></span>                                                          |
|-----------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="ec9eb-109">**Netfileclose**</span><span class="sxs-lookup"><span data-stu-id="ec9eb-109">**NetFileClose**</span></span>](/windows/desktop/api/lmshare/nf-lmshare-netfileclose)     | <span data-ttu-id="ec9eb-110">Erzwingt das Schließen einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="ec9eb-110">Forces a resource to close.</span></span>                                          |
| [<span data-ttu-id="ec9eb-111">**Netfileaufumum**</span><span class="sxs-lookup"><span data-stu-id="ec9eb-111">**NetFileEnum**</span></span>](/windows/desktop/api/lmshare/nf-lmshare-netfileenum)       | <span data-ttu-id="ec9eb-112">Gibt Informationen zu geöffneten Dateien auf einem Server zurück.</span><span class="sxs-lookup"><span data-stu-id="ec9eb-112">Returns information about open files on a server.</span></span>                    |
| [<span data-ttu-id="ec9eb-113">**Netfilegetinfo**</span><span class="sxs-lookup"><span data-stu-id="ec9eb-113">**NetFileGetInfo**</span></span>](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) | <span data-ttu-id="ec9eb-114">Gibt Informationen zu einem bestimmten Öffnen einer Server Ressource zurück.</span><span class="sxs-lookup"><span data-stu-id="ec9eb-114">Returns information about a particular opening of a server resource.</span></span> |



 

<span data-ttu-id="ec9eb-115">Wenn die Datei nicht auf andere Weise geschlossen werden kann, wird die [**netfileclose**](/windows/desktop/api/lmshare/nf-lmshare-netfileclose) -Funktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="ec9eb-115">Call the [**NetFileClose**](/windows/desktop/api/lmshare/nf-lmshare-netfileclose) function when the file cannot be closed by any other means.</span></span> <span data-ttu-id="ec9eb-116">Diese Funktion sollte mit Vorsicht verwendet werden, da **netfileclose** keine Daten schreibt, die auf dem Client System zwischengespeichert wurden, bevor die Datei geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="ec9eb-116">This function should be used with caution because **NetFileClose** does not write data cached on the client system to the file before closing the file.</span></span>

<span data-ttu-id="ec9eb-117">Die [**netfileenum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum) -Funktion gibt Informationen zu Ressourcen zurück, die auf einem Server geöffnet sind.</span><span class="sxs-lookup"><span data-stu-id="ec9eb-117">The [**NetFileEnum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum) function returns information about resources open on a server.</span></span> <span data-ttu-id="ec9eb-118">Eine Datei kann von einer oder mehreren Anwendungen einmal oder mehrmals geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="ec9eb-118">A file can be opened one or more times by one or more applications.</span></span> <span data-ttu-id="ec9eb-119">Alle Datei öffnenden werden eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ec9eb-119">Each file opening is uniquely identified.</span></span> <span data-ttu-id="ec9eb-120">Die **netfileenum** -Funktion gibt einen Eintrag für jede Datei, die geöffnet wird, zurück.</span><span class="sxs-lookup"><span data-stu-id="ec9eb-120">The **NetFileEnum** function returns an entry for each file opening.</span></span> <span data-ttu-id="ec9eb-121">Die [**netfilegetinfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) -Funktion gibt Informationen zu einem Öffnen einer Ressource zurück.</span><span class="sxs-lookup"><span data-stu-id="ec9eb-121">The [**NetFileGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) function returns information about one opening of a resource.</span></span>

<span data-ttu-id="ec9eb-122">Dateiinformationen sind auf folgenden Ebenen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="ec9eb-122">File information is available at the following levels:</span></span>

-   [<span data-ttu-id="ec9eb-123">**Datei \_ Informationen \_ 2**</span><span class="sxs-lookup"><span data-stu-id="ec9eb-123">**FILE\_INFO\_2**</span></span>](/windows/desktop/api/lmshare/ns-lmshare-file_info_2)
-   [<span data-ttu-id="ec9eb-124">**Datei \_ Info \_ 3**</span><span class="sxs-lookup"><span data-stu-id="ec9eb-124">**FILE\_INFO\_3**</span></span>](/windows/desktop/api/lmshare/ns-lmshare-file_info_3)

<span data-ttu-id="ec9eb-125">Die Ebenen 0 und 1 werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ec9eb-125">Levels 0 and 1 are not supported.</span></span> <span data-ttu-id="ec9eb-126">Ebene 2 gibt nur die Identifikationsnummer zurück, die der Ressource zugewiesen wurde, als Sie geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="ec9eb-126">Level 2 returns only the identification number assigned to the resource when it was opened.</span></span> <span data-ttu-id="ec9eb-127">Auf Ebene 3 werden die Identifikationsnummer, Berechtigungen, Dateisperren und der Name des Benutzers, der die Ressource geöffnet hat, zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ec9eb-127">Level 3 returns the identification number, permissions, file locks, and the name of the user who opened the resource.</span></span>

<span data-ttu-id="ec9eb-128">Wenn Sie für Active Directory programmieren, können Sie möglicherweise bestimmte Active Directory Service Interface (ADSI)-Methoden aufrufen, um die gleiche Funktionalität zu erreichen, die Sie durch Aufrufen der Funktionen [**netfileenum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum) und [**netfilegetinfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) erreichen können.</span><span class="sxs-lookup"><span data-stu-id="ec9eb-128">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the [**NetFileEnum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum) and [**NetFileGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) functions.</span></span> <span data-ttu-id="ec9eb-129">Weitere Informationen finden Sie unter [**iadsresource**](/windows/desktop/api/iads/nn-iads-iadsresource) und [**iadsfileserviceoperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).</span><span class="sxs-lookup"><span data-stu-id="ec9eb-129">For more information, see [**IADsResource**](/windows/desktop/api/iads/nn-iads-iadsresource) and [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).</span></span>

 

 
