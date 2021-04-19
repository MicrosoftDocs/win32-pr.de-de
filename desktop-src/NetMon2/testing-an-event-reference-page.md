---
description: Der letzte Schritt beim Erstellen einer Ereignis Referenzseite (ERP) ist das Testen.
ms.assetid: 12690317-1cd2-496c-8a0d-ba6caca58b86
title: Testen einer Ereignis Referenzseite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6afaaec279403922abde578b9e73931e607680f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346975"
---
# <a name="testing-an-event-reference-page"></a><span data-ttu-id="06f67-103">Testen einer Ereignis Referenzseite</span><span class="sxs-lookup"><span data-stu-id="06f67-103">Testing an Event Reference Page</span></span>

<span data-ttu-id="06f67-104">Der letzte Schritt beim Erstellen einer Ereignis Referenzseite (ERP) ist das Testen.</span><span class="sxs-lookup"><span data-stu-id="06f67-104">The final step of creating an event reference page (ERP) is to test it.</span></span> <span data-ttu-id="06f67-105">Sie können ein ERP testen, indem Sie die Datei in einem HTML-Browser wie z. b. Microsoft Internet Explorer anzeigen.</span><span class="sxs-lookup"><span data-stu-id="06f67-105">You can test an ERP by viewing the file in an HTML browser such as Microsoft Internet Explorer.</span></span> <span data-ttu-id="06f67-106">Oder Sie können das ERP und seine Experten-dll installieren, um es für den Ereignis Aufruf zu testen und in der Netzwerkmonitor Ereignisanzeige anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="06f67-106">Or, you can install the ERP and its expert DLL to test it for event invocation and display it in the Network Monitor Event Viewer.</span></span>

## <a name="viewing-erps-that-have-no-dll"></a><span data-ttu-id="06f67-107">Anzeigen von Erps ohne dll</span><span class="sxs-lookup"><span data-stu-id="06f67-107">Viewing ERPs that Have No DLL</span></span>

<span data-ttu-id="06f67-108">Öffnen Sie die Datei mit einem HTML-Viewer, der Ihre eingebetteten Quellen unterstützt, um das abgeschlossene ERP ohne eine installierte Experte-dll anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="06f67-108">To view the completed ERP without an installed expert DLL, open the file with an HTML viewer that supports your embedded sources.</span></span> <span data-ttu-id="06f67-109">Die folgende Abbildung zeigt die ERP-Beispieldatei, die in [Schreiben eines ERP](writing-an-event-reference-page.md) -Dokuments beschrieben wird, wie es mit Microsoft Internet Explorer Version 4,01 angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="06f67-109">The following illustration shows the sample ERP file described in [Writing an ERP](writing-an-event-reference-page.md) as it is displayed using Microsoft Internet Explorer Version 4.01.</span></span>

![Beispiel-ERP-Datei](images/ie-erp.png)

<span data-ttu-id="06f67-111">Testen von Erps mit einer dll</span><span class="sxs-lookup"><span data-stu-id="06f67-111">Testing ERPs that Have a DLL</span></span>

<span data-ttu-id="06f67-112">Nachdem die ERP-Dateien und die [**Experten-**](experts.md) dll erstellt wurden, können Sie die gesamte Funktionalität Ihrer Erps mit Netzwerkmonitor testen.</span><span class="sxs-lookup"><span data-stu-id="06f67-112">After the ERP files and the [**expert**](experts.md) DLL is created, you can test the complete functionality of your ERPs with Network Monitor.</span></span> <span data-ttu-id="06f67-113">Es wird davon ausgegangen, dass die dll debuggten ist und gültige Ereignisse generieren kann.</span><span class="sxs-lookup"><span data-stu-id="06f67-113">It is assumed that the DLL is debugged and can generate valid events.</span></span>

<span data-ttu-id="06f67-114">**So testen Sie Erps, die eine DLL haben**</span><span class="sxs-lookup"><span data-stu-id="06f67-114">**To test ERPs that have a DLL**</span></span>

1.  <span data-ttu-id="06f67-115">Vergewissern Sie sich, dass die richtige Experten-dll im entsprechenden Verzeichnis installiert ist.</span><span class="sxs-lookup"><span data-stu-id="06f67-115">Verify that the correct expert DLL is installed in the appropriate directory.</span></span> <span data-ttu-id="06f67-116">Weitere Informationen finden Sie unter [Installieren eines Experten in Netzwerkmonitor 2,1](installing-an-expert-to-network-monitor-2-1.md).</span><span class="sxs-lookup"><span data-stu-id="06f67-116">For more information, see [Installing an Expert to Network Monitor 2.1](installing-an-expert-to-network-monitor-2-1.md).</span></span>
2.  <span data-ttu-id="06f67-117">Überprüfen Sie den [richtigen Namen](naming-an-event-reference-page.md) der ERP-Datei.</span><span class="sxs-lookup"><span data-stu-id="06f67-117">Verify the [correct name](naming-an-event-reference-page.md) of the ERP file.</span></span>
3.  <span data-ttu-id="06f67-118">Überprüfen Sie den [richtigen Speicherort](installing-existing-erps-to-network-monitor-2-1.md) der Erps im Netzwerkmonitor Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="06f67-118">Verify the [correct location](installing-existing-erps-to-network-monitor-2-1.md) of the ERPs in the Network Monitor directory.</span></span>
4.  <span data-ttu-id="06f67-119">Testen von Experten Erps in der Netzwerkmonitor-Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="06f67-119">Test expert ERPs in the Network Monitor UI.</span></span>
5.  <span data-ttu-id="06f67-120">Generieren Sie ein Test Ereignis.</span><span class="sxs-lookup"><span data-stu-id="06f67-120">Generate a test event.</span></span>
6.  <span data-ttu-id="06f67-121">Überprüfen Sie, ob das ERP in der Netzwerkmonitor Ereignisanzeige angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="06f67-121">Verify that the ERP appears in the Network Monitor Event Viewer.</span></span>

<span data-ttu-id="06f67-122">Weitere Informationen zum Erstellen eines ERP finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="06f67-122">For more information about creating an ERP, see:</span></span>

-   [<span data-ttu-id="06f67-123">Erstellen von Referenzseiten für Experten und Überwachungs Ereignisse</span><span class="sxs-lookup"><span data-stu-id="06f67-123">Creating Expert and Monitor Event Reference Pages</span></span>](creating-expert-and-monitor-event-reference-pages.md)
-   [<span data-ttu-id="06f67-124">Schreiben einer Ereignis Referenzseite</span><span class="sxs-lookup"><span data-stu-id="06f67-124">Writing an Event Reference Page</span></span>](writing-an-event-reference-page.md)
-   [<span data-ttu-id="06f67-125">Benennen einer Ereignis Referenzseite</span><span class="sxs-lookup"><span data-stu-id="06f67-125">Naming an Event Reference Page</span></span>](naming-an-event-reference-page.md)

 

 



