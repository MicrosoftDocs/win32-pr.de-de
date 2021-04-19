---
title: Schreiben eines Client-DVC-Moduls
description: Zum Schreiben eines c#-Client Moduls (Dynamic Virtual Channel) müssen Sie zuerst ein Remotedesktopverbindung-Client-Plug-in (RDC) implementieren und registrieren.
ms.assetid: b6f475d4-d2ad-41ce-b3b9-d844fbd23cf0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcb881fd057132eb416066ffac050f75f4df1b12
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339421"
---
# <a name="writing-a-client-dvc-module"></a><span data-ttu-id="18b39-103">Schreiben eines Client-DVC-Moduls</span><span class="sxs-lookup"><span data-stu-id="18b39-103">Writing a Client DVC Module</span></span>

<span data-ttu-id="18b39-104">Zum Schreiben eines c#-Client Moduls (Dynamic Virtual Channel) müssen Sie zuerst ein Remotedesktopverbindung-Client-Plug-in (RDC) implementieren und registrieren.</span><span class="sxs-lookup"><span data-stu-id="18b39-104">To write a dynamic virtual channel (DVC) client module, you must first implement and register a Remote Desktop Connection (RDC) client plug-in.</span></span> <span data-ttu-id="18b39-105">Das DVC-Plug-in ist eine Implementierung von [**iwtsplugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin), die als Component Object Model (com)-Objekt registriert ist.</span><span class="sxs-lookup"><span data-stu-id="18b39-105">The DVC plug-in is an implementation of [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin), registered as a Component Object Model (COM) object.</span></span>

> [!Note]  
> <span data-ttu-id="18b39-106">Das Plug-in muss in einem kostenlosen Threading Modell implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="18b39-106">The plug-in must be implemented in a free-threading model.</span></span> <span data-ttu-id="18b39-107">Die Implementierung von Apartment Modellen wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="18b39-107">Apartment-model implementation is not supported.</span></span>

 

<span data-ttu-id="18b39-108">Im folgenden finden Sie eine Liste der Schnittstellen, die von Objekten implementiert werden, die durch das-Plug-in instanziiert werden.</span><span class="sxs-lookup"><span data-stu-id="18b39-108">The following is a list of interfaces that are implemented by objects that are instantiated by the plug-in.</span></span>



| <span data-ttu-id="18b39-109">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="18b39-109">Interface</span></span>                                                        | <span data-ttu-id="18b39-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="18b39-110">Description</span></span>                                                                                                                                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="18b39-111">**Iwtsplugin**</span><span class="sxs-lookup"><span data-stu-id="18b39-111">**IWTSPlugin**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin)                                 | <span data-ttu-id="18b39-112">Ermöglicht das Laden des-Remotedesktopverbindung (RDC)-Client-Plug-ins durch den Remotedesktopverbindung-Client (RDC).</span><span class="sxs-lookup"><span data-stu-id="18b39-112">Allows for the Remote Desktop Connection (RDC) client plug-in to be loaded by the Remote Desktop Connection (RDC) client.</span></span><br/>                                                                 |
| [<span data-ttu-id="18b39-113">**Iwtilistenercallback**</span><span class="sxs-lookup"><span data-stu-id="18b39-113">**IWTSListenerCallback**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)             | <span data-ttu-id="18b39-114">Benachrichtigt das Remotedesktopverbindung (RDC)-Client-Plug-in über eingehende Anforderungen für einen bestimmten Listener.</span><span class="sxs-lookup"><span data-stu-id="18b39-114">Notifies the Remote Desktop Connection (RDC) client plug-in about incoming requests on a particular listener.</span></span><br/>                                                                             |
| [<span data-ttu-id="18b39-115">**Iwout virtualchannelcallback**</span><span class="sxs-lookup"><span data-stu-id="18b39-115">**IWTSVirtualChannelCallback**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback) | <span data-ttu-id="18b39-116">Empfängt Benachrichtigungen über Kanalstatus Änderungen oder empfangene Daten.</span><span class="sxs-lookup"><span data-stu-id="18b39-116">Receives notifications about channel state changes or data received.</span></span> <span data-ttu-id="18b39-117">Jede Instanz dieser Schnittstelle ist einer Instanz von [**iwtionvirtualchannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="18b39-117">Each instance of this interface is associated with one instance of [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel).</span></span><br/> |



 

<span data-ttu-id="18b39-118">Im folgenden finden Sie eine Liste der Schnittstellen, die von Objekten implementiert werden, die vom-Remotedesktopverbindung (RDC)-Client instanziiert werden und Teil des-Frameworks sind.</span><span class="sxs-lookup"><span data-stu-id="18b39-118">The following is a list of interfaces that are implemented by objects that are instantiated by the Remote Desktop Connection (RDC) client, and are part of the framework.</span></span>



| <span data-ttu-id="18b39-119">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="18b39-119">Interface</span></span>                                                      | <span data-ttu-id="18b39-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="18b39-120">Description</span></span>                                                                                                        |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="18b39-121">**Iwout virtualchannelmanager**</span><span class="sxs-lookup"><span data-stu-id="18b39-121">**IWTSVirtualChannelManager**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager) | <span data-ttu-id="18b39-122">Verwaltet alle Remotedesktopverbindung (RDC)-Client-Plug-ins, DVC-Listener oder statische virtuelle Kanäle.</span><span class="sxs-lookup"><span data-stu-id="18b39-122">Manages all Remote Desktop Connection (RDC) client plug-ins, DVC listeners, or static virtual channels.</span></span><br/> |
| [<span data-ttu-id="18b39-123">**Iwunglistener**</span><span class="sxs-lookup"><span data-stu-id="18b39-123">**IWTSListener**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener)                           | <span data-ttu-id="18b39-124">Verwaltet die Konfigurationseinstellungen für jeden Listener für die DVC-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="18b39-124">Manages configuration settings for each listener for the DVC connection.</span></span><br/>                                |
| [<span data-ttu-id="18b39-125">**Iwungvirtualchannel**</span><span class="sxs-lookup"><span data-stu-id="18b39-125">**IWTSVirtualChannel**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)               | <span data-ttu-id="18b39-126">Steuert den Kanalstatus und Schreibvorgänge auf dem Kanal.</span><span class="sxs-lookup"><span data-stu-id="18b39-126">Controls the channel state, as well as writes on the channel.</span></span><br/>                                           |



 

<span data-ttu-id="18b39-127">In der folgenden Abbildung wird die Beziehung zwischen dem Remotedesktopverbindung-Client (RDC) und dem-Remotedesktopverbindung (RDC)-Client-Plug-in dargestellt.</span><span class="sxs-lookup"><span data-stu-id="18b39-127">The following illustration shows the relationship between the Remote Desktop Connection (RDC) client and the Remote Desktop Connection (RDC) client plug-in.</span></span>

![Beziehung zwischen Client und Plug-in](images/tsclient.png)

 

 





