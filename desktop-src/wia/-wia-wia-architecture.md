---
description: WIA wird als Component Object Model (com) out-of-Process-Server implementiert, um den robusten Betrieb von Client Anwendungen zu gewährleisten.
ms.assetid: 9f3d1848-36ab-4e0f-a7f4-312bc85ecc00
title: WIA-Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09652258ee249fb3c68e65472e863ccd35154ee5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104560671"
---
# <a name="wia-architecture"></a><span data-ttu-id="1a8db-103">WIA-Architektur</span><span class="sxs-lookup"><span data-stu-id="1a8db-103">WIA Architecture</span></span>

<span data-ttu-id="1a8db-104">WIA wird als Component Object Model (com) out-of-Process-Server implementiert, um den robusten Betrieb von Client Anwendungen zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="1a8db-104">WIA is implemented as a Component Object Model (COM) out-of-process server to ensure the robust operation of client applications.</span></span> <span data-ttu-id="1a8db-105">Im Gegensatz zu den meisten Prozess Server Anwendungen vermeidet die Windows-Abbild Beschaffung (WIA) während der Abbild Datenübertragung durch die Bereitstellung eines eigenen Datenübertragungsmechanismus ( [**iwiadatatransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer)) Leistungseinbußen.</span><span class="sxs-lookup"><span data-stu-id="1a8db-105">Unlike most out of process server applications, Windows Image Acquisition (WIA) avoids performance penalties during image data transfer by providing its own data transfer mechanism, [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).</span></span> <span data-ttu-id="1a8db-106">Diese Hochleistungs Schnittstelle verwendet ein frei gegebenes Speicherfenster zum Übertragen von Daten an den Client.</span><span class="sxs-lookup"><span data-stu-id="1a8db-106">This high performance interface uses a shared memory window to transfer data to the client.</span></span>

<span data-ttu-id="1a8db-107">WIA umfasst drei Hauptkomponenten: eine Device Manager, eine Minidriver-Dienst Bibliothek und ein Geräte-Mini Treiber.</span><span class="sxs-lookup"><span data-stu-id="1a8db-107">WIA has three main components: a Device Manager, a Minidriver Service Library, and a Device Minidriver.</span></span>

-   <span data-ttu-id="1a8db-108">Der Device Manager listet Abbild Erstellungs Geräte auf, ruft Geräteeigenschaften ab, richtet Ereignisse für Geräte ein und erstellt Geräte Objekte.</span><span class="sxs-lookup"><span data-stu-id="1a8db-108">The Device Manager enumerates imaging devices, retrieves device properties, sets up events for devices, and creates device objects.</span></span>
-   <span data-ttu-id="1a8db-109">Die Minidriver-Dienst Bibliothek implementiert alle Dienste, die Geräte unabhängig sind.</span><span class="sxs-lookup"><span data-stu-id="1a8db-109">The Minidriver Service Library implements all services that are device independent.</span></span>
-   <span data-ttu-id="1a8db-110">Der Geräte-Mini Treiber ordnet einem bestimmten Gerät WIA-Eigenschaften und-Befehle zu.</span><span class="sxs-lookup"><span data-stu-id="1a8db-110">The Device Minidriver maps WIA properties and commands to the specific device.</span></span>

<span data-ttu-id="1a8db-111">Das folgende Diagramm veranschaulicht die WIA-Architektur:</span><span class="sxs-lookup"><span data-stu-id="1a8db-111">The following diagram illustrates the WIA architecture:</span></span>

![WIA-Architektur](images/wiarch.gif)

 

 



