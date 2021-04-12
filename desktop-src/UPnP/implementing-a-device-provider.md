---
title: Implementieren eines Geräte Anbieters
description: Um einen Geräte Anbieter zu implementieren, erstellen Sie ein Objekt, das die iupnpdeviceprovider-Schnittstelle verfügbar macht.
ms.assetid: 3ba1200d-68d4-4f03-805c-7fff2d76b16f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb8cd2bea433b884bf6ddf3828fb148c726cd867
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471725"
---
# <a name="implementing-a-device-provider"></a><span data-ttu-id="4de8a-103">Implementieren eines Geräte Anbieters</span><span class="sxs-lookup"><span data-stu-id="4de8a-103">Implementing a Device Provider</span></span>

<span data-ttu-id="4de8a-104">Um einen Geräte Anbieter zu implementieren, erstellen Sie ein Objekt, das die [**iupnpdeviceprovider**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdeviceprovider) -Schnittstelle verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="4de8a-104">To implement a device provider, create an object that exposes the [**IUPnPDeviceProvider**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdeviceprovider) interface.</span></span> <span data-ttu-id="4de8a-105">Dieses Objekt muss beim Geräte Host mit der [**iupnpregistrinnerpregistrinsterdeviceprovider**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdeviceprovider) -Methode registriert werden.</span><span class="sxs-lookup"><span data-stu-id="4de8a-105">This object must be registered with the device host using the [**IUPnPRegistrar::RegisterDeviceProvider**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdeviceprovider) method.</span></span> <span data-ttu-id="4de8a-106">Diese Methode übernimmt die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="4de8a-106">This method takes the following parameters:</span></span>

-   <span data-ttu-id="4de8a-107">Der Name des Anbieters, der auf dem Computer eindeutig sein muss.</span><span class="sxs-lookup"><span data-stu-id="4de8a-107">The name of the provider, which must be unique on the computer.</span></span>
-   <span data-ttu-id="4de8a-108">Die ProgID der Klasse, die den Geräte Anbieter implementiert.</span><span class="sxs-lookup"><span data-stu-id="4de8a-108">The ProgID of the class that implements the device provider.</span></span>
-   <span data-ttu-id="4de8a-109">Eine Initialisierungs Zeichenfolge, die beim Starten an den Geräte Anbieter übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="4de8a-109">An initialization string that is passed to the device provider when it is started.</span></span>
-   <span data-ttu-id="4de8a-110">Eine Container-ID.</span><span class="sxs-lookup"><span data-stu-id="4de8a-110">A container ID.</span></span> <span data-ttu-id="4de8a-111">Eine Container-ID ist eine Zeichenfolge, die die Gruppe identifiziert, zu der das Gerät gehört.</span><span class="sxs-lookup"><span data-stu-id="4de8a-111">A container ID is a string that identifies the group to which the device belongs.</span></span> <span data-ttu-id="4de8a-112">Alle Geräte mit demselben Container Bezeichner werden im gleichen Prozess gehostet.</span><span class="sxs-lookup"><span data-stu-id="4de8a-112">All devices with the same container identifier are hosted in the same process.</span></span>

 

 




