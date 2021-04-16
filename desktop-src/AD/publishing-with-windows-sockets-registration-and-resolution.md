---
title: Veröffentlichung mit Windows Sockets-Registrierungs & Auflösung
description: Windows Sockets-Dienste können die APIs für die Registrierung und Auflösung (RNR) verwenden, um Dienste zu veröffentlichen und mit RNR veröffentlichte Dienste zu suchen.
ms.assetid: 95c16d0b-abbc-4407-ac31-d7de0b25bd74
ms.tgt_platform: multiple
keywords:
- Windows Sockets-Registrierung und-Auflösung, Veröffentlichung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e722d83447bd97e3964a9a0cc85df45ffd27faba
ms.sourcegitcommit: 460af18ea55f4b12d47d5b8d4b883896e21adf00
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/04/2019
ms.locfileid: "104472092"
---
# <a name="publishing-with-windows-sockets-registration--resolution"></a><span data-ttu-id="098ff-104">Veröffentlichung mit Windows Sockets-Registrierungs & Auflösung</span><span class="sxs-lookup"><span data-stu-id="098ff-104">Publishing with Windows Sockets Registration & Resolution</span></span>

<span data-ttu-id="098ff-105">Windows Sockets-Dienste können die APIs für die Registrierung und Auflösung (RNR) verwenden, um Dienste zu veröffentlichen und mit RNR veröffentlichte Dienste zu suchen.</span><span class="sxs-lookup"><span data-stu-id="098ff-105">Windows Sockets services can use the Registration and Resolution (RnR) APIs to publish services and look up services published with RnR.</span></span> <span data-ttu-id="098ff-106">Die RNR-Veröffentlichung erfolgt in zwei Schritten.</span><span class="sxs-lookup"><span data-stu-id="098ff-106">RnR publication occurs in two steps.</span></span> <span data-ttu-id="098ff-107">Im ersten Schritt wird eine Dienstklasse installiert, die eine GUID mit einem Namen für den Dienst verknüpft.</span><span class="sxs-lookup"><span data-stu-id="098ff-107">The first step installs a service class that associates a GUID with a name for the service.</span></span> <span data-ttu-id="098ff-108">Die Dienstklasse kann Dienst spezifische Konfigurationsdaten enthalten.</span><span class="sxs-lookup"><span data-stu-id="098ff-108">The service class can hold service-specific configuration data.</span></span> <span data-ttu-id="098ff-109">Dienste können sich dann selbst als Instanzen der Dienstklasse veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="098ff-109">Services can then publish themselves as instances of the service class.</span></span> <span data-ttu-id="098ff-110">Bei der Veröffentlichung können Clients den Verzeichnisdienst nach Instanzen einer bestimmten Klasse Abfragen, indem Sie die RNR-APIs verwenden und eine Instanz auswählen, an die eine Bindung erfolgen soll.</span><span class="sxs-lookup"><span data-stu-id="098ff-110">When published, clients can query the directory service for instances of a given class using the RnR APIs and select an instance to bind to.</span></span> <span data-ttu-id="098ff-111">Wenn eine Klasse nicht mehr benötigt wird, kann Sie entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="098ff-111">When a class is no longer required, it can be removed.</span></span>

 

 




