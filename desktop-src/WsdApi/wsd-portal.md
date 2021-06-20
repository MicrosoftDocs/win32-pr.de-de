---
description: Erfahren Sie mehr über das Implementieren von Webdiensten auf Geräten (WSD). Verstehen des Zwecks, wo er anwendbar ist, der Zielgruppe des Entwicklers und der Laufzeitanforderungen.
ms.assetid: 590e0b0b-763c-44fb-a49f-606415f57b26
title: Webdienste auf Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 267f8dba0fd56c383dd3cecabb3c00959aa0d90c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405753"
---
# <a name="web-services-on-devices"></a><span data-ttu-id="5e752-104">Webdienste auf Geräten</span><span class="sxs-lookup"><span data-stu-id="5e752-104">Web Services on Devices</span></span>

## <a name="purpose"></a><span data-ttu-id="5e752-105">Zweck</span><span class="sxs-lookup"><span data-stu-id="5e752-105">Purpose</span></span>

<span data-ttu-id="5e752-106">Die Microsoft Web Services on Devices-API (WSDAPI) unterstützt die Implementierung von clientgesteuerten Geräten und Diensten sowie Gerätehosts, die dem Geräteprofil für Webdienste (DEVICES [Profile for Web Services,](https://specs.xmlsoap.org/ws/2006/02/devprof/) DPWS) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="5e752-106">The Microsoft Web Services on Devices API (WSDAPI) supports the implementation of client-controlled devices and services, and device hosts conforming to the [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span></span> <span data-ttu-id="5e752-107">WSDAPI verwendet [WS-Discovery für](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) die Geräteermittlung.</span><span class="sxs-lookup"><span data-stu-id="5e752-107">WSDAPI uses [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) for device discovery.</span></span>

<span data-ttu-id="5e752-108">WSDAPI kann für die Entwicklung von Client- und Dienstimplementierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5e752-108">WSDAPI may be used for the development of both client and service implementations.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="5e752-109">Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="5e752-109">Where applicable</span></span>

<span data-ttu-id="5e752-110">Webdienste auf Geräten ermöglichen es einem Client, ein Remotegerät und die zugehörigen Dienste über ein Netzwerk zu entdecken und darauf zu zugreifen.</span><span class="sxs-lookup"><span data-stu-id="5e752-110">Web Services on Devices allows a client to discover and access a remote device and its associated services across a network.</span></span> <span data-ttu-id="5e752-111">Es unterstützt die Geräteermittlung, Beschreibung, Steuerung und Ereignisermittlung.</span><span class="sxs-lookup"><span data-stu-id="5e752-111">It supports device discovery, description, control, and eventing.</span></span> <span data-ttu-id="5e752-112">Entwickler können WSDAPI-Clientproxies und entsprechende Stubs für Gerätehosts erstellen.</span><span class="sxs-lookup"><span data-stu-id="5e752-112">Developers can create WSDAPI client proxies and corresponding stubs for device hosts.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="5e752-113">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="5e752-113">Developer audience</span></span>

<span data-ttu-id="5e752-114">Die Dokumentation zu Webdiensten auf Geräten richtet sich an C/C++-Programmierer und Gerätehersteller, die DPWS-konforme Produkte erstellen.</span><span class="sxs-lookup"><span data-stu-id="5e752-114">The Web Services on Devices documentation is intended for C/C++ programmers and device vendors creating DPWS-compliant products.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="5e752-115">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="5e752-115">Run-time requirements</span></span>

<span data-ttu-id="5e752-116">Clientanwendungen, die WSDAPI verwenden, werden ab Windows Vista und Windows Server 2008 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5e752-116">Client applications that use WSDAPI are supported starting with Windows Vista and Windows Server 2008.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5e752-117">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="5e752-117">In this section</span></span>



| <span data-ttu-id="5e752-118">Thema</span><span class="sxs-lookup"><span data-stu-id="5e752-118">Topic</span></span>                                                                                  | <span data-ttu-id="5e752-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e752-119">Description</span></span>                                                                                  |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5e752-120">Informationen zu Webdiensten auf Geräten</span><span class="sxs-lookup"><span data-stu-id="5e752-120">About Web Services on Devices</span></span>](about-web-services-for-devices.md)<br/>         | <span data-ttu-id="5e752-121">Architekturinformationen und allgemeine Informationen zu Webdiensten auf Geräten.</span><span class="sxs-lookup"><span data-stu-id="5e752-121">Architectural and general information about Web Services on Devices.</span></span><br/>              |
| [<span data-ttu-id="5e752-122">Verwenden von Webdiensten auf Geräten</span><span class="sxs-lookup"><span data-stu-id="5e752-122">Using Web Services on Devices</span></span>](using-web-services-on-devices.md)<br/>          | <span data-ttu-id="5e752-123">Informationen zum Generieren von Code, Konfigurieren von Anwendungen und Problembehandlung.</span><span class="sxs-lookup"><span data-stu-id="5e752-123">Information about generating code, configuring applications, and troubleshooting.</span></span><br/> |
| [<span data-ttu-id="5e752-124">Referenz zu Webdiensten auf Geräten</span><span class="sxs-lookup"><span data-stu-id="5e752-124">Web Services on Devices Reference</span></span>](web-services-for-devices-reference.md)<br/> | <span data-ttu-id="5e752-125">Referenzdokumentation für die API "Webdienste auf Geräten".</span><span class="sxs-lookup"><span data-stu-id="5e752-125">Reference documentation for the Web Services on Devices API.</span></span><br/>                      |



 

## <a name="related-topics"></a><span data-ttu-id="5e752-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5e752-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e752-127">Dan Driscolls Blog</span><span class="sxs-lookup"><span data-stu-id="5e752-127">Dan Driscoll's Blog</span></span>](/archive/blogs/dandris/)
</dt> </dl>

 

