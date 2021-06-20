---
description: Hier erfahren Sie, wie Sie die WSD-API (Microsoft Web Services on Devices) (WSDAPI) verwenden, um clientgesteuerte Geräte und Dienste sowie Gerätehosts zu implementieren, die DPWS entsprechen.
ms.assetid: 88de8dea-56d5-4bfc-8837-03da81b7d0f9
title: WSD-Anwendungsentwicklung unter Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 167cd1ad013ea387a6e33b6de449f3f84d49db13
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405783"
---
# <a name="wsd-application-development-on-windows"></a><span data-ttu-id="b712a-103">WSD-Anwendungsentwicklung unter Windows</span><span class="sxs-lookup"><span data-stu-id="b712a-103">WSD Application Development on Windows</span></span>

<span data-ttu-id="b712a-104">Die Microsoft Web Services on Devices-API (WSDAPI) unterstützt die Implementierung von clientgesteuerten Geräten und Diensten sowie Gerätehosts, die dem Geräteprofil für Webdienste (DEVICES [Profile for Web Services,](https://specs.xmlsoap.org/ws/2006/02/devprof/) DPWS) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b712a-104">The Microsoft Web Services on Devices API (WSDAPI) supports the implementation of client-controlled devices and services, and device hosts conforming to the [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span></span> <span data-ttu-id="b712a-105">WSDAPI kann für die Entwicklung von Client- und Serverimplementierung (Gerät) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b712a-105">WSDAPI may be used for the development of both client and server (device) implementations.</span></span>

<span data-ttu-id="b712a-106">Häufig wird WSDAPI-Code für diese Anwendungen mit [WsdCodeGen generiert.](web-services-for-devices-code-generator.md)</span><span class="sxs-lookup"><span data-stu-id="b712a-106">Quite often, WSDAPI code for these applications is generated using [WsdCodeGen](web-services-for-devices-code-generator.md).</span></span> <span data-ttu-id="b712a-107">Einige WSDAPI-Funktionen und -Methoden sind nur für den Aufruf durch generierten Code vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="b712a-107">Some WSDAPI functions and methods are intended to be called only by generated code.</span></span> <span data-ttu-id="b712a-108">Die API-Referenzdokumentation gibt an, wann eine Funktion oder Methode nur von generierten Code verwendet oder implementiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b712a-108">The API reference documentation indicates when a function or method should be used or implemented only by generated code.</span></span>

<span data-ttu-id="b712a-109">Die Windows SDK enthält einige WSDL-Beispieldateien, WsdCodeGen-Konfigurationsdateien und generierten Code.</span><span class="sxs-lookup"><span data-stu-id="b712a-109">The Windows SDK includes some sample WSDL files, WsdCodeGen configuration files, and generated code.</span></span> <span data-ttu-id="b712a-110">Weitere Informationen finden Sie unter [WSDAPI-Beispiele.](wsdapi-samples.md)</span><span class="sxs-lookup"><span data-stu-id="b712a-110">For more information, see [WSDAPI Samples](wsdapi-samples.md).</span></span>

<span data-ttu-id="b712a-111">Wenn Sie Geräte mithilfe des WSD-Protokolls aufzählen und WSD-Gerätemetadaten abfragen möchten, können Sie stattdessen die Funktionsermittlungs-API [](/previous-versions/windows/desktop/fundisc/fd-portal) verwenden.</span><span class="sxs-lookup"><span data-stu-id="b712a-111">If you want to enumerate devices using the WSD protocol and query WSD device metadata, you can use the [Function Discovery](/previous-versions/windows/desktop/fundisc/fd-portal) API instead.</span></span>

<span data-ttu-id="b712a-112">Wenn Sie ein WSD-Gerät implementieren möchten, auf dem Windows nicht ausgeführt wird, finden Sie weitere Informationen unter [WSD Device Development (WSD-Geräteentwicklung).](wsd-device-development.md)</span><span class="sxs-lookup"><span data-stu-id="b712a-112">If you want to implement a WSD device that does not run Windows, see [WSD Device Development](wsd-device-development.md).</span></span>
