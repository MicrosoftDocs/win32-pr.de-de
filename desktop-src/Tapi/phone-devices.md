---
description: Die Unterstützung von Telefongeräten ist ergänzend und nicht einfach, sodass Dienstanbieter keine Telefongeräte unterstützen müssen.
ms.assetid: 4d9f3b32-20d0-4550-9b3d-db97df8ea289
title: Telefongeräte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f406442e43d8d4f31a89bfc0ccb1e59916d33e0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959102"
---
# <a name="phone-devices"></a><span data-ttu-id="d8631-103">Telefongeräte</span><span class="sxs-lookup"><span data-stu-id="d8631-103">Phone Devices</span></span>

<span data-ttu-id="d8631-104">Die Unterstützung von Telefongeräten ist ergänzend und nicht einfach, sodass Dienstanbieter keine Telefongeräte unterstützen müssen.</span><span class="sxs-lookup"><span data-stu-id="d8631-104">Phone device support is supplementary rather than basic, so service providers are not required to support phone devices.</span></span>

<span data-ttu-id="d8631-105">Ebenso wie eine Line-Device-Klasse eine Abstraktion eines physischen Geräte Geräts ist, stellt die Phone-Geräteklasse eine geräteunabhängige Abstraktion eines Telefon Sets dar.</span><span class="sxs-lookup"><span data-stu-id="d8631-105">Just as a line device class is an abstraction of a physical line device, the phone device class represents a device-independent abstraction of a telephone set.</span></span> <span data-ttu-id="d8631-106">TAPI behandelt Linien-und Telefongeräte als Geräte, die unabhängig voneinander sind.</span><span class="sxs-lookup"><span data-stu-id="d8631-106">TAPI treats line and phone devices as devices that are independent of each other.</span></span> <span data-ttu-id="d8631-107">Anders ausgedrückt: Sie können ein Telefon (Gerät) verwenden, ohne eine zugehörige Zeile zu verwenden, und Sie können eine Linie (Gerät) ohne Telefon verwenden.</span><span class="sxs-lookup"><span data-stu-id="d8631-107">In other words, you can use a phone (device) without using an associated line, and you can use a line (device) without using a phone.</span></span>

<span data-ttu-id="d8631-108">Dienstanbieter, die diese Unabhängigkeit vollständig implementieren, können für diese Geräte verwendet werden, die nicht durch herkömmliche Telefonieprotokolle definiert werden.</span><span class="sxs-lookup"><span data-stu-id="d8631-108">Service providers that fully implement this independence can offer uses for these devices not defined by traditional telephony protocols.</span></span> <span data-ttu-id="d8631-109">Eine Person kann z. b. das Mobiltelefon des Desktops als Wellenform-Audiogerät für die Sprachaufzeichnung oder Wiedergabe verwenden, möglicherweise ohne das Wissen des Schalters, dass das Telefon verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d8631-109">For example, a person can use the handset of the desktop's phone as a waveform audio device for voice recording or playback, perhaps without the switch's knowledge that the phone is in use.</span></span> <span data-ttu-id="d8631-110">In einer solchen Implementierung muss bei der Aufhebung des lokalen Telefon Telefons nicht automatisch ein OFFHOOK-Signal an den Switch gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="d8631-110">In such an implementation, lifting the local phone handset need not automatically send an offhook signal to the switch.</span></span>

<span data-ttu-id="d8631-111">Diese Unabhängigkeit ermöglicht es einer Anwendung auch, das lokale Telefon auf eine Weise zu klingeln, die von eingehenden aufrufen unabhängig ist.</span><span class="sxs-lookup"><span data-stu-id="d8631-111">This independence also allows an application to ring the local telephone in a manner that is independent of incoming calls.</span></span> <span data-ttu-id="d8631-112">Die Funktionen von Dienstanbietern sind durch die Funktionen der Hardware und Software beschränkt, die für die Verbindung zwischen dem Switch, dem Telefon und dem Computer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d8631-112">The capabilities of service providers are limited by the capabilities of the hardware and software used to interconnect the switch, the phone, and the computer.</span></span>

<span data-ttu-id="d8631-113">TAPI umfasst Funktionen zum Abrufen von Gerätefunktionen, mit denen Clients ermitteln können, ob ein solches Verwendungs Modell unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="d8631-113">TAPI includes functions to retrieve device capabilities that allow clients to determine whether such a usage model is supported.</span></span>

<span data-ttu-id="d8631-114">In diesem Abschnitt werden Telefongeräte beschrieben und erläutert, wie die TAPI-Telefonfunktionen für den Zugriff auf diese Geräte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d8631-114">This section describes phone devices and explains how to use the TAPI phone functions to access these devices.</span></span>

-   [<span data-ttu-id="d8631-115">Telefongerät</span><span class="sxs-lookup"><span data-stu-id="d8631-115">Phone Device</span></span>](phone-device-elements.md)
-   [<span data-ttu-id="d8631-116">Initialisierung und Herunterfahren</span><span class="sxs-lookup"><span data-stu-id="d8631-116">Initialization and Shutdown</span></span>](initialization-and-shutdown.md)

 

 



