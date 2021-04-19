---
description: Die Microsoft Web Services on Devices-API (WSDAPI) unterstützt die Implementierung von Client gesteuerten Geräten und Diensten sowie Geräte Hosts, die dem Geräte Profil für Webdienste (DPWS) entsprechen.
ms.assetid: 590e0b0b-763c-44fb-a49f-606415f57b26
title: Webdienste auf Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10d8b5812983e7102093234458c94b475bb6a503
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345236"
---
# <a name="web-services-on-devices"></a><span data-ttu-id="967c7-103">Webdienste auf Geräten</span><span class="sxs-lookup"><span data-stu-id="967c7-103">Web Services on Devices</span></span>

## <a name="purpose"></a><span data-ttu-id="967c7-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="967c7-104">Purpose</span></span>

<span data-ttu-id="967c7-105">Die Microsoft Web Services on Devices-API (WSDAPI) unterstützt die Implementierung von Client gesteuerten Geräten und Diensten sowie Geräte Hosts, die dem [Geräte Profil für Webdienste](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="967c7-105">The Microsoft Web Services on Devices API (WSDAPI) supports the implementation of client-controlled devices and services, and device hosts conforming to the [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span></span> <span data-ttu-id="967c7-106">WSDAPI verwendet [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) für die Geräte Ermittlung.</span><span class="sxs-lookup"><span data-stu-id="967c7-106">WSDAPI uses [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) for device discovery.</span></span>

<span data-ttu-id="967c7-107">WSDAPI kann für die Entwicklung von Client-und Dienst Implementierungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="967c7-107">WSDAPI may be used for the development of both client and service implementations.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="967c7-108">Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="967c7-108">Where applicable</span></span>

<span data-ttu-id="967c7-109">Mithilfe von Webdiensten auf Geräten kann ein Client ein Remote Gerät und seine zugeordneten Dienste über ein Netzwerk ermitteln und darauf zugreifen.</span><span class="sxs-lookup"><span data-stu-id="967c7-109">Web Services on Devices allows a client to discover and access a remote device and its associated services across a network.</span></span> <span data-ttu-id="967c7-110">Es unterstützt Geräte Ermittlung, Beschreibung, Kontrolle und Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="967c7-110">It supports device discovery, description, control, and eventing.</span></span> <span data-ttu-id="967c7-111">Entwickler können WSDAPI-Client Proxys und entsprechende stusb für Geräte Hosts erstellen.</span><span class="sxs-lookup"><span data-stu-id="967c7-111">Developers can create WSDAPI client proxies and corresponding stubs for device hosts.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="967c7-112">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="967c7-112">Developer audience</span></span>

<span data-ttu-id="967c7-113">Die Dokumentation zu Webdiensten auf Geräten richtet sich an C/C++-Programmierer und Gerätehersteller, die DPWS-kompatible Produkte erstellen.</span><span class="sxs-lookup"><span data-stu-id="967c7-113">The Web Services on Devices documentation is intended for C/C++ programmers and device vendors creating DPWS-compliant products.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="967c7-114">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="967c7-114">Run-time requirements</span></span>

<span data-ttu-id="967c7-115">Client Anwendungen, die WSDAPI verwenden, werden ab Windows Vista und Windows Server 2008 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="967c7-115">Client applications that use WSDAPI are supported starting with Windows Vista and Windows Server 2008.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="967c7-116">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="967c7-116">In this section</span></span>



| <span data-ttu-id="967c7-117">Thema</span><span class="sxs-lookup"><span data-stu-id="967c7-117">Topic</span></span>                                                                                  | <span data-ttu-id="967c7-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="967c7-118">Description</span></span>                                                                                  |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="967c7-119">Informationen zu Webdiensten auf Geräten</span><span class="sxs-lookup"><span data-stu-id="967c7-119">About Web Services on Devices</span></span>](about-web-services-for-devices.md)<br/>         | <span data-ttu-id="967c7-120">Architektur und allgemeine Informationen zu Webdiensten auf Geräten.</span><span class="sxs-lookup"><span data-stu-id="967c7-120">Architectural and general information about Web Services on Devices.</span></span><br/>              |
| [<span data-ttu-id="967c7-121">Verwenden von Webdiensten auf Geräten</span><span class="sxs-lookup"><span data-stu-id="967c7-121">Using Web Services on Devices</span></span>](using-web-services-on-devices.md)<br/>          | <span data-ttu-id="967c7-122">Informationen zum Erstellen von Code, zum Konfigurieren von Anwendungen und zur Problembehandlung.</span><span class="sxs-lookup"><span data-stu-id="967c7-122">Information about generating code, configuring applications, and troubleshooting.</span></span><br/> |
| [<span data-ttu-id="967c7-123">Referenz zu Webdiensten auf Geräten</span><span class="sxs-lookup"><span data-stu-id="967c7-123">Web Services on Devices Reference</span></span>](web-services-for-devices-reference.md)<br/> | <span data-ttu-id="967c7-124">Referenz Dokumentation für die API für Webdienste auf Geräten.</span><span class="sxs-lookup"><span data-stu-id="967c7-124">Reference documentation for the Web Services on Devices API.</span></span><br/>                      |



 

## <a name="related-topics"></a><span data-ttu-id="967c7-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="967c7-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="967c7-126">Dan Driscoll Blog</span><span class="sxs-lookup"><span data-stu-id="967c7-126">Dan Driscoll's Blog</span></span>](/archive/blogs/dandris/)
</dt> </dl>

 

