---
title: Verwalten von Bluetooth-Geräten und-Diensten
description: Zwei primäre Bluetooth-Programmier Ansätze für die Windows-Programmierung mit der Windows Sockets-Schnittstelle und die direkte Verwaltung von Geräten mit nicht Socket-Bluetooth-Schnittstellen
ms.assetid: 0eb7d339-6d23-4313-b1ed-7ab403a5a81d
keywords:
- Verwalten von Bluetooth-Geräten und-Diensten
- Bluetooth-Geräte und-Dienste, verwalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61cf3657dff2091eda4b26d14f6504b74f943983
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101698"
---
# <a name="managing-bluetooth-devices-and-services"></a><span data-ttu-id="5a7ff-105">Verwalten von Bluetooth-Geräten und-Diensten</span><span class="sxs-lookup"><span data-stu-id="5a7ff-105">Managing Bluetooth Devices and Services</span></span>

<span data-ttu-id="5a7ff-106">In diesem Abschnitt wird beschrieben, wie Sie mit der Bluetooth-API Bluetooth-Geräte und-Dienste direkt steuern können.</span><span class="sxs-lookup"><span data-stu-id="5a7ff-106">This section describes how to use the Bluetooth API to directly control Bluetooth devices and services.</span></span>

<span data-ttu-id="5a7ff-107">Informationen zur Verwendung der Windows Sockets-Schnittstelle zum Programmieren von Bluetooth unter Windows finden Sie [unter Windows Sockets-Unterstützung für Bluetooth](windows-sockets-support-for-bluetooth.md).</span><span class="sxs-lookup"><span data-stu-id="5a7ff-107">For information about using the Windows Sockets interface to program Bluetooth on Windows, see [Windows Sockets Support for Bluetooth](windows-sockets-support-for-bluetooth.md).</span></span>

> [!Note]  
> <span data-ttu-id="5a7ff-108">Bluetooth hindert keine Energie Verwaltungsfunktionen daran, Bluetooth-Übertragungen zu unterbrechen.</span><span class="sxs-lookup"><span data-stu-id="5a7ff-108">Bluetooth does not prevent power management features from interrupting Bluetooth transmissions.</span></span> <span data-ttu-id="5a7ff-109">Für Bluetooth aktivierte Anwendungen können Strom Meldungen überwachen, um eine solche Unterbrechung zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="5a7ff-109">Bluetooth-enabled applications can monitor power messages to prevent such interruption.</span></span> <span data-ttu-id="5a7ff-110">Weitere Informationen finden Sie unter [Verwenden der Energie Verwaltung](/windows/desktop/Power/using-power-management).</span><span class="sxs-lookup"><span data-stu-id="5a7ff-110">For more information, see [Using Power Management](/windows/desktop/Power/using-power-management).</span></span>

 

<span data-ttu-id="5a7ff-111">In diesem Abschnitt werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="5a7ff-111">This section contains the following topics.</span></span>

| <span data-ttu-id="5a7ff-112">`Section`</span><span class="sxs-lookup"><span data-stu-id="5a7ff-112">Section</span></span>                                                                               | <span data-ttu-id="5a7ff-113">Inhalt</span><span class="sxs-lookup"><span data-stu-id="5a7ff-113">Content</span></span>                                                                       |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="5a7ff-114">Auswählen eines Bluetooth-Geräts</span><span class="sxs-lookup"><span data-stu-id="5a7ff-114">Selecting a Bluetooth Device</span></span>](selecting-a-bluetooth-device.md)                      | <span data-ttu-id="5a7ff-115">Hier wird beschrieben, wie ein Bluetooth-Gerät ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="5a7ff-115">Describes how to select a Bluetooth device.</span></span>                                   |
| [<span data-ttu-id="5a7ff-116">Bluetooth-und WM- \_ devicechange-Meldungen</span><span class="sxs-lookup"><span data-stu-id="5a7ff-116">Bluetooth and WM\_DEVICECHANGE Messages</span></span>](bluetooth-and-wm-devicechange-messages.md) | <span data-ttu-id="5a7ff-117">Erläutert die Interaktion zwischen Bluetooth-und **WM \_ devicechange** -Meldungen.</span><span class="sxs-lookup"><span data-stu-id="5a7ff-117">Explains the interaction between Bluetooth and **WM\_DEVICECHANGE** messages.</span></span> |



 

 

 