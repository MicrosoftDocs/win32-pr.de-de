---
description: Die Funktionen zum Umleiten von Geräten leiten Standard-MS-DOS-Geräte, Laufwerk Buchstaben und LPT-Ports um. Auf diese Weise können Anwendungen, die auf dem System ausgeführt werden, die Geräte verwenden und auf das Netzwerk vollständig transparent zugreifen.
ms.assetid: a61ab1e6-dad9-4dc0-a908-f8440619f610
title: Device-Redirecting Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 577f8d108b6bfdeb01f786478cd736e6c84cc83d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214410"
---
# <a name="device-redirecting-functions"></a><span data-ttu-id="953e0-104">Device-Redirecting Funktionen</span><span class="sxs-lookup"><span data-stu-id="953e0-104">Device-Redirecting Functions</span></span>

<span data-ttu-id="953e0-105">Die Funktionen zum Umleiten von Geräten leiten Standard-MS-DOS-Geräte, Laufwerk Buchstaben und LPT-Ports um.</span><span class="sxs-lookup"><span data-stu-id="953e0-105">The device-redirecting functions redirect standard MS-DOS devices, drive letters and LPT ports.</span></span> <span data-ttu-id="953e0-106">Auf diese Weise können Anwendungen, die auf dem System ausgeführt werden, die Geräte verwenden und auf das Netzwerk vollständig transparent zugreifen.</span><span class="sxs-lookup"><span data-stu-id="953e0-106">This enables applications running on the system to use the devices and access the network in a totally transparent manner.</span></span>



| <span data-ttu-id="953e0-107">Funktion</span><span class="sxs-lookup"><span data-stu-id="953e0-107">Function</span></span>                                                         | <span data-ttu-id="953e0-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="953e0-108">Description</span></span>                                                                                                                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="953e0-109">**Npaddconnection**</span><span class="sxs-lookup"><span data-stu-id="953e0-109">**NPAddConnection**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npaddconnection)                       | <span data-ttu-id="953e0-110">Leitet ein lokales Gerät an eine Netzwerkressource um und stellt eine Verbindung her.</span><span class="sxs-lookup"><span data-stu-id="953e0-110">Redirects or connects a local device to a network resource.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="953e0-111">**NPAddConnection3**</span><span class="sxs-lookup"><span data-stu-id="953e0-111">**NPAddConnection3**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npaddconnection3)                     | <span data-ttu-id="953e0-112">Führt dieselbe Aktion wie [**npaddconnection**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection)aus, ermöglicht jedoch dem Benutzer anzugeben, welches Fenster die Besitzer von Dialogfeldern sein soll und wie die Verbindung hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="953e0-112">Performs the same action as [**NPAddConnection**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection), but lets the user specify which window should own any dialog boxes and how the connection should be established.</span></span><br/> |
| [<span data-ttu-id="953e0-113">**Npcancelconnection**</span><span class="sxs-lookup"><span data-stu-id="953e0-113">**NPCancelConnection**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npcancelconnection)                 | <span data-ttu-id="953e0-114">Unterbricht eine Netzwerkverbindung.</span><span class="sxs-lookup"><span data-stu-id="953e0-114">Breaks a network connection.</span></span> <span data-ttu-id="953e0-115">Die Änderungen werden gespeichert, wenn ein Gerät getrennt wird, es sei denn, es handelt sich um eine nicht beliebige Verbindung.</span><span class="sxs-lookup"><span data-stu-id="953e0-115">The changes are remembered if a device is disconnected unless the connection is a deviceless connection.</span></span><br/>                                                    |
| [<span data-ttu-id="953e0-116">**Npgetconnection**</span><span class="sxs-lookup"><span data-stu-id="953e0-116">**NPGetConnection**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetconnection)                       | <span data-ttu-id="953e0-117">Gibt Informationen über eine Verbindung zurück.</span><span class="sxs-lookup"><span data-stu-id="953e0-117">Returns information about a connection.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="953e0-118">**NPGetConnection3**</span><span class="sxs-lookup"><span data-stu-id="953e0-118">**NPGetConnection3**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetconnection3)                     | <span data-ttu-id="953e0-119">Gibt Informationen zu einer Verbindung zurück, auch wenn die Verbindung zurzeit getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="953e0-119">Returns information about a connection, even if the connection is currently disconnected.</span></span><br/>                                                                                                |
| [<span data-ttu-id="953e0-120">**Npgetconnectionperformance**</span><span class="sxs-lookup"><span data-stu-id="953e0-120">**NPGetConnectionPerformance**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetconnectionperformance) | <span data-ttu-id="953e0-121">Gibt Leistungsinformationen zu einer Verbindung zurück.</span><span class="sxs-lookup"><span data-stu-id="953e0-121">Returns performance information about a connection.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="953e0-122">**Npgetuniversalname**</span><span class="sxs-lookup"><span data-stu-id="953e0-122">**NPGetUniversalName**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetuniversalname)                 | <span data-ttu-id="953e0-123">Gibt den Remote-oder lokalen universellen Namen in dem während des Funktions Aufrufes angegebenen Format zurück.</span><span class="sxs-lookup"><span data-stu-id="953e0-123">Returns the remote or local universal name, in the format specified during the function call.</span></span><br/>                                                                                            |



 

 

 




