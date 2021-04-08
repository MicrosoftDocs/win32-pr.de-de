---
description: Netzwerk Paketanbieter (NPPs) machen die Schnittstellen idelta aydc, iESP, iritc und iStats verfügbar.
ms.assetid: 269b26f5-b794-4920-98da-505eda83c990
title: Auswählen einer NPP-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8dba919302190e1fd89c859f61fca14aaf7d6e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864059"
---
# <a name="selecting-an-npp-interface"></a><span data-ttu-id="3df50-103">Auswählen einer NPP-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="3df50-103">Selecting an NPP Interface</span></span>

<span data-ttu-id="3df50-104">Netzwerk Paketanbieter (NPPs) machen die Schnittstellen [**idelta aydc**](idelaydc.md), [**iESP**](iesp.md), [**iritc**](irtc.md)und [**iStats**](istats.md) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3df50-104">Network packet providers (NPPs) expose the [**IDelaydC**](idelaydc.md), [**IESP**](iesp.md), [**IRTC**](irtc.md), and [**IStats**](istats.md) interfaces.</span></span> <span data-ttu-id="3df50-105">Jede dieser Schnittstellen bietet ähnliche Methoden zum Verbinden des NPP mit dem Netzwerk, zum Erfassen von Netzwerk Datenverkehr und zum Sammeln statistischer Informationen zu den erfassten Daten.</span><span class="sxs-lookup"><span data-stu-id="3df50-105">Each of these interfaces provides similar methods for connecting the NPP to the network, capturing network traffic, and collecting statistical information about the captured data.</span></span> <span data-ttu-id="3df50-106">Informationen zu den zu verwendenden Schnittstellen finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="3df50-106">To choose which interface to use, refer to the following table.</span></span>

> [!Note]  
> <span data-ttu-id="3df50-107">Wenn Sie eine NPP mit dem Netzwerk verbinden, können Sie nur die Methoden verwenden, die von dieser Schnittstelle bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="3df50-107">When you connect an NPP to the network with one of these interfaces, you can only use the methods provided by that interface.</span></span> <span data-ttu-id="3df50-108">Wenn Sie z. b. eine Verbindung mit dem Netzwerk über die [**untc**](irtc.md) -Schnittstelle herstellen und dann versuchen, eine Erfassung mit [**idelta aydc**](idelaydc.md)zu starten, schlägt der Start der Erfassung fehl, und es wird ein Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3df50-108">For example, if you connect to the network using the [**IRTC**](irtc.md) interface and then try to start a capture with [**IDelaydC**](idelaydc.md), your call to start the capture will fail, and an error code will be returned.</span></span>

 



| <span data-ttu-id="3df50-109">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="3df50-109">Interface</span></span>                    | <span data-ttu-id="3df50-110">Verwendung</span><span class="sxs-lookup"><span data-stu-id="3df50-110">When to use</span></span>                                                                                                                                                                                                                                                                                                                                     |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3df50-111">**Idelta-DC**</span><span class="sxs-lookup"><span data-stu-id="3df50-111">**IDelaydC**</span></span>](idelaydc.md) | <span data-ttu-id="3df50-112">Verwenden Sie, um Netzwerk Datenverkehr zu erfassen und in einer Erfassungs Datei zu speichern.</span><span class="sxs-lookup"><span data-stu-id="3df50-112">Use to capture network traffic and store it in a capture file.</span></span> <span data-ttu-id="3df50-113">Diese Schnittstelle wird von der Netzwerkmonitor-Benutzeroberfläche und anderen NPP-Anwendungen verwendet, bei denen erfasste Netzwerkinformationen gespeichert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="3df50-113">This interface is used by the Network Monitor UI and other NPP applications, which require storing captured network information.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="3df50-114">**IESP**</span><span class="sxs-lookup"><span data-stu-id="3df50-114">**IESP**</span></span>](iesp.md)         | <span data-ttu-id="3df50-115">Wird verwendet, um Erweiterte Statistiken in einem speziellen ESP-Dateiformat bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="3df50-115">Used to provide enhanced statistics in a special ESP file format.</span></span> <span data-ttu-id="3df50-116">Diese Schnittstelle wird von NPP-Anwendungen verwendet, die die im ESP-Format bereitgestellte erweiterte Statistik erfordern.</span><span class="sxs-lookup"><span data-stu-id="3df50-116">This interface is used by NPP applications that require the enhanced statistics provided by the ESP format.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="3df50-117">**"Iran"**</span><span class="sxs-lookup"><span data-stu-id="3df50-117">**IRTC**</span></span>](irtc.md)         | <span data-ttu-id="3df50-118">Verwenden Sie, um den Netzwerk Datenverkehr in Echtzeit aufzuzeichnen und Ereignisse bei Auftreten zu Triggern aufzurufenden.</span><span class="sxs-lookup"><span data-stu-id="3df50-118">Use to capture real-time network traffic and to trigger events when they occur.</span></span> <span data-ttu-id="3df50-119">Diese Schnittstelle wird von NPP-Anwendungen verwendet, die Lauf Zeitaufzeichnungen erfordern.</span><span class="sxs-lookup"><span data-stu-id="3df50-119">This interface is used by NPP applications that require run-time captures.</span></span> <span data-ttu-id="3df50-120">Beachten Sie, dass diese Schnittstelle nicht die Statistiken bereitstellt, die von den anderen NPP-Schnittstellen bereitgestellt werden, und Sie können keine Frames in den erfassten Netzwerk Datenverkehr einfügen.</span><span class="sxs-lookup"><span data-stu-id="3df50-120">Note that this interface does not provide the statistics that the other NPP interfaces provide, nor does it allow you to insert frames into the captured network traffic.</span></span><br/> |
| [<span data-ttu-id="3df50-121">**IStats**</span><span class="sxs-lookup"><span data-stu-id="3df50-121">**IStats**</span></span>](istats.md)     | <span data-ttu-id="3df50-122">Verwenden Sie, um Aufzeichnungs Statistiken, aber nicht die erfassten Frames abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3df50-122">Use to retrieve capture statistics but not the captured frames.</span></span>                                                                                                                                                                                                                                                                                 |



 

 

 




