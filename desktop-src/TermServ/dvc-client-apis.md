---
title: DVC-Client-APIs
description: Die DVC-Client-APIs (Dynamic Virtual Channel) werden speziell für den Remotedesktopverbindung-Client (RDC) der Verbindung implementiert.
ms.assetid: 976a6cc2-7bbe-4ecc-91b4-b7c659eca5ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25c29d360fb0ad4d6e31e828f9c62f42f64fb311
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309783"
---
# <a name="dvc-client-apis"></a><span data-ttu-id="4fe75-103">DVC-Client-APIs</span><span class="sxs-lookup"><span data-stu-id="4fe75-103">DVC Client APIs</span></span>

<span data-ttu-id="4fe75-104">Die DVC-Client-APIs (Dynamic Virtual Channel) werden speziell für den Remotedesktopverbindung-Client (RDC) der Verbindung implementiert.</span><span class="sxs-lookup"><span data-stu-id="4fe75-104">The dynamic virtual channel (DVC) client APIs are implemented specifically for the Remote Desktop Connection (RDC) client of the connection.</span></span> <span data-ttu-id="4fe75-105">Einige der APIs werden vom DVC-Framework implementiert, und einige werden vom Plug-in-Entwickler implementiert.</span><span class="sxs-lookup"><span data-stu-id="4fe75-105">Some of the APIs are implemented by the DVC framework, and some are implemented by the plug-in developer.</span></span> <span data-ttu-id="4fe75-106">Einige der APIs werden zur Unterstützung des-Client-Plug-Ins für Remotedesktopverbindung (RDC) verwendet und sind nicht direkt mit dem Datentransport verknüpft.</span><span class="sxs-lookup"><span data-stu-id="4fe75-106">Some of the APIs are used to support the Remote Desktop Connection (RDC) client plug-in, and are not directly related to data transport.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4fe75-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="4fe75-107">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="4fe75-108">**Iwtsplugin**</span><span class="sxs-lookup"><span data-stu-id="4fe75-108">**IWTSPlugin**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin)
</dt> <dd>

<span data-ttu-id="4fe75-109">Ermöglicht das Laden des-Remotedesktopverbindung (RDC)-Client-Plug-ins durch den Remotedesktopverbindung-Client (RDC).</span><span class="sxs-lookup"><span data-stu-id="4fe75-109">Allows for the Remote Desktop Connection (RDC) client plug-in to be loaded by the Remote Desktop Connection (RDC) client.</span></span>

</dd> <dt>

[<span data-ttu-id="4fe75-110">**Iwunglistener**</span><span class="sxs-lookup"><span data-stu-id="4fe75-110">**IWTSListener**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener)
</dt> <dd>

<span data-ttu-id="4fe75-111">Verwaltet die Konfigurationseinstellungen für jeden Listener für die Verbindung des dynamischen virtuellen Kanals (DVC).</span><span class="sxs-lookup"><span data-stu-id="4fe75-111">Manages configuration settings for each listener for the dynamic virtual channel (DVC) connection.</span></span>

</dd> <dt>

[<span data-ttu-id="4fe75-112">**Iwtilistenercallback**</span><span class="sxs-lookup"><span data-stu-id="4fe75-112">**IWTSListenerCallback**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)
</dt> <dd>

<span data-ttu-id="4fe75-113">Wird verwendet, um das Client-Plug-in für Remotedesktopverbindung (RDC) über eingehende Anforderungen für einen bestimmten Listener zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="4fe75-113">Used to notify the Remote Desktop Connection (RDC) client plug-in about incoming requests on a particular listener.</span></span>

</dd> <dt>

[<span data-ttu-id="4fe75-114">**Iwout virtualchannelmanager**</span><span class="sxs-lookup"><span data-stu-id="4fe75-114">**IWTSVirtualChannelManager**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager)
</dt> <dd>

<span data-ttu-id="4fe75-115">Verwaltet alle Remotedesktopverbindung (RDC)-Client-Plug-ins und-DVC-Listener (Dynamic Virtual Channel).</span><span class="sxs-lookup"><span data-stu-id="4fe75-115">Manages all Remote Desktop Connection (RDC) client plug-ins and dynamic virtual channel (DVC) listeners.</span></span>

</dd> <dt>

[<span data-ttu-id="4fe75-116">**Iwungvirtualchannel**</span><span class="sxs-lookup"><span data-stu-id="4fe75-116">**IWTSVirtualChannel**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)
</dt> <dd>

<span data-ttu-id="4fe75-117">Wird verwendet, um den Kanal Zustand zu steuern und auf dem Kanal zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="4fe75-117">Used to control the channel state, and writes on the channel.</span></span>

</dd> <dt>

[<span data-ttu-id="4fe75-118">**Iwout virtualchannelcallback**</span><span class="sxs-lookup"><span data-stu-id="4fe75-118">**IWTSVirtualChannelCallback**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback)
</dt> <dd>

<span data-ttu-id="4fe75-119">Empfängt Benachrichtigungen über Kanalstatus Änderungen oder empfangene Daten.</span><span class="sxs-lookup"><span data-stu-id="4fe75-119">Receives notifications about channel state changes or data received.</span></span>

</dd> <dt>

[<span data-ttu-id="4fe75-120">**IWTSVirtualChannelCallback2**</span><span class="sxs-lookup"><span data-stu-id="4fe75-120">**IWTSVirtualChannelCallback2**</span></span>](iwtsvirtualchannelcallback2.md)
</dt> <dd>

<span data-ttu-id="4fe75-121">Diese Schnittstelle wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4fe75-121">This interface is not supported.</span></span>

</dd> <dt>

[<span data-ttu-id="4fe75-122">**Virtualchannelgetinstance**</span><span class="sxs-lookup"><span data-stu-id="4fe75-122">**VirtualChannelGetInstance**</span></span>](virtualchannelgetinstance.md)
</dt> <dd>

<span data-ttu-id="4fe75-123">Wird aufgerufen, damit das Plug-in eine Instanz der [**iwtsplugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) -Schnittstelle für alle Plug-Ins erstellt, die von der dll implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="4fe75-123">Called to have the plug-in create an instance of the [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) interface for all plug-ins implemented by the DLL.</span></span>

</dd> </dl>

 

 




