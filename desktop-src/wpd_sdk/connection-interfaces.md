---
description: MTP/Bluetooth-Verbindungs Schnittstellen
ms.assetid: 7bbd5fe3-85f1-4f0a-9d3e-22746bd23aae
title: MTP/Bluetooth-Verbindungs Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97e5194b8a6ababc05c36590ef30ae19ab185efe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050435"
---
# <a name="mtpbluetooth-connection-interfaces"></a><span data-ttu-id="8d0e3-103">MTP/Bluetooth-Verbindungs Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="8d0e3-103">MTP/Bluetooth Connection Interfaces</span></span>

<span data-ttu-id="8d0e3-104">Die folgenden Schnittstellen ermöglichen es Anwendungen, nur mit Geräten aufzulisten und eine Verbindung herzustellen, die das Media Transfer Protocol (MTP) über Bluetooth (MTP/Bluetooth) unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8d0e3-104">The following interfaces allow applications to enumerate and connect only to devices that support the Media Transfer Protocol (MTP) over Bluetooth (MTP/Bluetooth).</span></span> <span data-ttu-id="8d0e3-105">Die WPD-Treiber-, Sammlungs-und Client Schnittstellen sind nicht auf das MTP/Bluetooth-Protokoll beschränkt.</span><span class="sxs-lookup"><span data-stu-id="8d0e3-105">The WPD driver-, collection-, and client-interfaces are not restricted to the MTP/ Bluetooth protocol.</span></span>



| <span data-ttu-id="8d0e3-106">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="8d0e3-106">Interface</span></span>                                                              | <span data-ttu-id="8d0e3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8d0e3-107">Description</span></span>                                                                                                         |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8d0e3-108">**Iconnectionrequestcallback**</span><span class="sxs-lookup"><span data-stu-id="8d0e3-108">**IConnectionRequestCallback**</span></span>](iconnectionrequestcallback.md)       | <span data-ttu-id="8d0e3-109">Definiert eine einzelne Rückruf Methode, die von Anwendungen zum Empfangen von Benachrichtigungen über abgeschlossene und abgebrochene Anforderungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8d0e3-109">Defines a single callback method that applications use to receive notification of completed and cancelled requests.</span></span> |
| [<span data-ttu-id="8d0e3-110">**Ienumportablede viceconnectors**</span><span class="sxs-lookup"><span data-stu-id="8d0e3-110">**IEnumPortableDeviceConnectors**</span></span>](ienumportabledeviceconnectors.md) | <span data-ttu-id="8d0e3-111">Listet **iportabledeviceconnector** -Schnittstellen auf.</span><span class="sxs-lookup"><span data-stu-id="8d0e3-111">Enumerates **IPortableDeviceConnector** interfaces.</span></span>                                                                 |
| [<span data-ttu-id="8d0e3-112">**Iportablede viceconnector**</span><span class="sxs-lookup"><span data-stu-id="8d0e3-112">**IPortableDeviceConnector**</span></span>](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector)           | <span data-ttu-id="8d0e3-113">Unterstützt Methoden, die von Anwendungen zum Herstellen von Verbindungen mit MTP Bluetooth-Geräten aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="8d0e3-113">Supports methods that applications call to establish connections to MTP Bluetooth devices.</span></span>                          |



 

## <a name="related-topics"></a><span data-ttu-id="8d0e3-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8d0e3-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d0e3-115">**Programmierverzeichnis**</span><span class="sxs-lookup"><span data-stu-id="8d0e3-115">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 



