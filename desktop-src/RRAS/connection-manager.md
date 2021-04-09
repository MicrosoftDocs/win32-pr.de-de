---
title: Verbindungs-Manager
description: Kunden, die benutzerdefinierte dzer mithilfe der RAS-Dienst-API entwickeln möchten, können den Microsoft-Verbindungs-Manager und das Verbindungs-Manager-Verwaltungskit untersuchen.
ms.assetid: c3227aea-ba36-44f6-b69d-2c6aa4be360e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7959482542630b6dc90149971df08f7944f83fc
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104038620"
---
# <a name="connection-manager"></a><span data-ttu-id="91544-103">Verbindungs-Manager</span><span class="sxs-lookup"><span data-stu-id="91544-103">Connection Manager</span></span>

<span data-ttu-id="91544-104">Kunden, die benutzerdefinierte dzer mithilfe der RAS-Dienst-API entwickeln möchten, können den Microsoft-Verbindungs-Manager und das Verbindungs-Manager-Verwaltungskit untersuchen.</span><span class="sxs-lookup"><span data-stu-id="91544-104">Customers who intend to develop custom dialers using the Remote Access Service API may want to investigate Microsoft Connection Manager and the Connection Manager Administration Kit.</span></span> <span data-ttu-id="91544-105">Der Verbindungs-Manager ist der verwaltete RAS-Client von Microsoft.</span><span class="sxs-lookup"><span data-stu-id="91544-105">Connection Manager is Microsoft's managed remote access client.</span></span> <span data-ttu-id="91544-106">Dadurch kann ein Administrator ein Remote Zugriffs-Konfigurations Paket erstellen, das an die Remote Benutzer des Administrators verteilt wird.</span><span class="sxs-lookup"><span data-stu-id="91544-106">It allows an administrator to build a remote access configuration package to be distributed to the administrator's remote users.</span></span> <span data-ttu-id="91544-107">Weitere Informationen zum Verbindungs-Manager und zum Verbindungs-Manager-Verwaltungskit finden Sie in der Online Hilfe für Microsoft Windows 2000 Server und spätere Betriebssysteme.</span><span class="sxs-lookup"><span data-stu-id="91544-107">For more information on Connection Manager and the Connection Manager Administration Kit, see the online help for Microsoft Windows 2000 Server and later operating systems.</span></span>

<span data-ttu-id="91544-108">Sie finden den Quellcode für eine benutzerdefinierte Aktion für einen Verbindungs-Manager im Complete Platform Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="91544-108">You can find the source code for a sample Connection Manager custom action in the complete Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="91544-109">Das Platform SDK kann auf der Microsoft- [Website](https://msdn.microsoft.com/windowsserver/bb980924.aspx)heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="91544-109">The Platform SDK can be downloaded at the [Microsoft Web site](https://msdn.microsoft.com/windowsserver/bb980924.aspx).</span></span> <span data-ttu-id="91544-110">Nach der Installation lautet der Pfad zum Beispielcode "% Install path% \\ Microsoft SDK \\ Samples \\ netds \\ RAS \\ ConnectionManager", wobei "% Install path%" das Basis Installationsverzeichnis des Platform SDK (z. b. "C: \\ Program Files") angibt.</span><span class="sxs-lookup"><span data-stu-id="91544-110">After installation, the path to the sample code is %Install Path%\\Microsoft SDK\\Samples\\netds\\Ras\\ConnectionManager, where %Install Path% designates the base installation directory of the Platform SDK (for example, C:\\Program Files).</span></span>

<span data-ttu-id="91544-111">Benutzerdefinierte Aktionen ermöglichen es dem RAS-Client, bestimmte Aktionen an verschiedenen Punkten im Verbindungsprozess auszuführen.</span><span class="sxs-lookup"><span data-stu-id="91544-111">Custom actions make it possible for the remote access client to take specific actions at various points in the connection process.</span></span> <span data-ttu-id="91544-112">Die im Beispiel gezeigte benutzerdefinierte Aktion passt automatisch die Proxy Serverkonfiguration für eine Verbindung basierend auf der Server Adresse der Verbindung an.</span><span class="sxs-lookup"><span data-stu-id="91544-112">The custom action demonstrated in the sample automatically adjusts the proxy server configuration for a connection based on the connection's server address.</span></span> <span data-ttu-id="91544-113">Kunden können dieses Beispiel als Ausgangspunkt für das Erstellen eigener benutzerdefinierter Aktionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="91544-113">Customers can use this sample as a starting point for creating their own custom actions.</span></span>

 

 




