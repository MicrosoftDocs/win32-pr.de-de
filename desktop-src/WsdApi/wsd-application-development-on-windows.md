---
description: Die Microsoft Web Services on Devices-API (WSDAPI) unterstützt die Implementierung von Client gesteuerten Geräten und Diensten sowie Geräte Hosts, die dem Geräte Profil für Webdienste (DPWS) entsprechen.
ms.assetid: 88de8dea-56d5-4bfc-8837-03da81b7d0f9
title: WSD-Anwendungsentwicklung unter Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e33976a1903c87ffb6c577cd5a451a3b772a67a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358482"
---
# <a name="wsd-application-development-on-windows"></a><span data-ttu-id="42eba-103">WSD-Anwendungsentwicklung unter Windows</span><span class="sxs-lookup"><span data-stu-id="42eba-103">WSD Application Development on Windows</span></span>

<span data-ttu-id="42eba-104">Die Microsoft Web Services on Devices-API (WSDAPI) unterstützt die Implementierung von Client gesteuerten Geräten und Diensten sowie Geräte Hosts, die dem [Geräte Profil für Webdienste](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="42eba-104">The Microsoft Web Services on Devices API (WSDAPI) supports the implementation of client-controlled devices and services, and device hosts conforming to the [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span></span> <span data-ttu-id="42eba-105">WSDAPI kann für die Entwicklung von Client-und Server-(Geräte-) Implementierungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="42eba-105">WSDAPI may be used for the development of both client and server (device) implementations.</span></span>

<span data-ttu-id="42eba-106">Häufig wird der WSDAPI-Code für diese Anwendungen mithilfe von [wsdcodegen](web-services-for-devices-code-generator.md)generiert.</span><span class="sxs-lookup"><span data-stu-id="42eba-106">Quite often, WSDAPI code for these applications is generated using [WsdCodeGen](web-services-for-devices-code-generator.md).</span></span> <span data-ttu-id="42eba-107">Einige WSDAPI-Funktionen und-Methoden sollen nur von generiertem Code aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="42eba-107">Some WSDAPI functions and methods are intended to be called only by generated code.</span></span> <span data-ttu-id="42eba-108">Die API-Referenz Dokumentation zeigt an, wann eine Funktion oder Methode nur durch generierten Code verwendet oder implementiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="42eba-108">The API reference documentation indicates when a function or method should be used or implemented only by generated code.</span></span>

<span data-ttu-id="42eba-109">Die Windows SDK umfasst einige WSDL-Beispieldateien, wsdcodegen-Konfigurationsdateien und generierten Code.</span><span class="sxs-lookup"><span data-stu-id="42eba-109">The Windows SDK includes some sample WSDL files, WsdCodeGen configuration files, and generated code.</span></span> <span data-ttu-id="42eba-110">Weitere Informationen finden Sie unter [WSDAPI Samples](wsdapi-samples.md).</span><span class="sxs-lookup"><span data-stu-id="42eba-110">For more information, see [WSDAPI Samples](wsdapi-samples.md).</span></span>

<span data-ttu-id="42eba-111">Wenn Sie Geräte mithilfe des WSD-Protokolls auflisten und WSD-Geräte Metadaten abfragen möchten, können Sie stattdessen die [funktionsermittlungs](/previous-versions/windows/desktop/fundisc/fd-portal) -API verwenden.</span><span class="sxs-lookup"><span data-stu-id="42eba-111">If you want to enumerate devices using the WSD protocol and query WSD device metadata, you can use the [Function Discovery](/previous-versions/windows/desktop/fundisc/fd-portal) API instead.</span></span>

<span data-ttu-id="42eba-112">Wenn Sie ein WSD-Gerät implementieren möchten, das nicht Windows ausgeführt wird, finden Sie weitere Informationen unter [WSD-Geräteentwicklung](wsd-device-development.md).</span><span class="sxs-lookup"><span data-stu-id="42eba-112">If you want to implement a WSD device that does not run Windows, see [WSD Device Development](wsd-device-development.md).</span></span>
