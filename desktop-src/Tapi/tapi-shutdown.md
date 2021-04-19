---
description: Das ordnungsgemäße Herunterfahren von Kommunikationssitzungen und einer gesamten Anwendung ist erforderlich, um zu verhindern, dass Ressourcen in aufrufen oder Anwendungen, die Sie nicht mehr benötigen, gebunden bleiben.
ms.assetid: 40694b7f-474b-41aa-be3f-48e4ca517a6f
title: TAPI Herunterfahren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 661273a3d72559d965fa1ea6066f1090f8e6b6e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357014"
---
# <a name="tapi-shutdown"></a><span data-ttu-id="e9b60-103">TAPI Herunterfahren</span><span class="sxs-lookup"><span data-stu-id="e9b60-103">TAPI Shutdown</span></span>

<span data-ttu-id="e9b60-104">Das ordnungsgemäße Herunterfahren von Kommunikationssitzungen und einer gesamten Anwendung ist erforderlich, um zu verhindern, dass Ressourcen in aufrufen oder Anwendungen, die Sie nicht mehr benötigen, gebunden bleiben.</span><span class="sxs-lookup"><span data-stu-id="e9b60-104">Proper shutdown of communications sessions and of an entire application is required to prevent resources from remaining tied up in calls or applications that no longer need them.</span></span>

<span data-ttu-id="e9b60-105">TAPI stellt eine Reihe von Funktionen und Methoden bereit, um den Prozess zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="e9b60-105">TAPI provides a series of functions and methods to assist in the process.</span></span> <span data-ttu-id="e9b60-106">Natürlich muss die Anwendung auch die Verantwortung für die ordnungsgemäße Freigabe von zugewiesener Speicher übernehmen, egal ob in Form von Datenstrukturen oder com-verweisen.</span><span class="sxs-lookup"><span data-stu-id="e9b60-106">Obviously, the application must also take responsibility for properly releasing allocated memory, whether in the form of data structures or COM references.</span></span>



| <span data-ttu-id="e9b60-107">TAPI 2. x-Funktionen</span><span class="sxs-lookup"><span data-stu-id="e9b60-107">TAPI 2.x functions</span></span>                                                            | <span data-ttu-id="e9b60-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e9b60-108">Description</span></span>                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="e9b60-109">**lineregisterrequestrecipient**</span><span class="sxs-lookup"><span data-stu-id="e9b60-109">**lineRegisterRequestRecipient**</span></span>](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient) | <span data-ttu-id="e9b60-110">Hebt die Registrierung der Anwendung als Handler für unterstützte telefonieaufrufe auf.</span><span class="sxs-lookup"><span data-stu-id="e9b60-110">Unregisters the application as a handler for assisted telephony calls.</span></span> |
| [<span data-ttu-id="e9b60-111">**lineclose**</span><span class="sxs-lookup"><span data-stu-id="e9b60-111">**lineClose**</span></span>](/windows/win32/api/tapi/nf-tapi-lineclose)                                       | <span data-ttu-id="e9b60-112">Trennt die Anwendung als Manager für Aufrufe in der angegebenen Zeile.</span><span class="sxs-lookup"><span data-stu-id="e9b60-112">Disconnects the application as a manager for calls on the given line.</span></span>  |
| [<span data-ttu-id="e9b60-113">**LineShutdown**</span><span class="sxs-lookup"><span data-stu-id="e9b60-113">**lineShutdown**</span></span>](/windows/win32/api/tapi/nf-tapi-lineshutdown)                                 | <span data-ttu-id="e9b60-114">Fährt die Verwendung der Zeilen Abstraktion durch die Anwendung herunter.</span><span class="sxs-lookup"><span data-stu-id="e9b60-114">Shuts down the application's usage of the line abstraction.</span></span>            |



 



| <span data-ttu-id="e9b60-115">TAPI 3. x-Schnittstellen oder-Methoden</span><span class="sxs-lookup"><span data-stu-id="e9b60-115">TAPI 3.x interfaces or methods</span></span>                                            | <span data-ttu-id="e9b60-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e9b60-116">Description</span></span>                                                                |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="e9b60-117">**Ittapi:: UnregisterNotification**</span><span class="sxs-lookup"><span data-stu-id="e9b60-117">**ITTAPI::UnregisterNotifications**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-unregisternotifications) | <span data-ttu-id="e9b60-118">Entfernt alle Ereignis Benachrichtigungs Registrierungen, die von der Anwendung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e9b60-118">Removes any event notification registrations performed by the application.</span></span> |
| [<span data-ttu-id="e9b60-119">**Ittapi:: Shutdown**</span><span class="sxs-lookup"><span data-stu-id="e9b60-119">**ITTAPI::Shutdown**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-shutdown)                               | <span data-ttu-id="e9b60-120">Trennt die Anwendung als einen-Callcenter.</span><span class="sxs-lookup"><span data-stu-id="e9b60-120">Disconnects the application as a call manager.</span></span>                             |



 

 

 
