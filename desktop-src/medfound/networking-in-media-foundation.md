---
description: Netzwerk in Media Foundation
ms.assetid: 59eec612-3b6d-400c-8190-1ae8675a2e1b
title: Netzwerk in Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3aff68ee1f9e124cda5dd01e82192078b41b0de
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103869427"
---
# <a name="networking-in-media-foundation"></a><span data-ttu-id="b0e18-103">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b0e18-103">Networking in Media Foundation</span></span>

<span data-ttu-id="b0e18-104">Anwendungen, die auf Media Foundation basieren, können Medienquellen über ein Netzwerk wiedergeben.</span><span class="sxs-lookup"><span data-stu-id="b0e18-104">Applications based on Media Foundation can play media sources over a network.</span></span> <span data-ttu-id="b0e18-105">Bei der Anwendung ähnelt der Prozess der Wiedergabe aus einer lokalen Datei.</span><span class="sxs-lookup"><span data-stu-id="b0e18-105">For the application, the process is similar to playing from a local file.</span></span>



| <span data-ttu-id="b0e18-106">Thema</span><span class="sxs-lookup"><span data-stu-id="b0e18-106">Topic</span></span>                                                                                      | <span data-ttu-id="b0e18-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b0e18-107">Description</span></span>                                                                                                                             |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b0e18-108">Netzwerk Quell Features</span><span class="sxs-lookup"><span data-stu-id="b0e18-108">Network Source Features</span></span>](network-source-features.md)                                     | <span data-ttu-id="b0e18-109">Beschreibt die von der Netzwerkquelle unterstützten Funktionen und die zugehörigen Konfigurationsoptionen.</span><span class="sxs-lookup"><span data-stu-id="b0e18-109">Describes the features supported by the network source and the associated configuration options.</span></span>                                        |
| [<span data-ttu-id="b0e18-110">Proxy Unterstützung für Netzwerk Quellen</span><span class="sxs-lookup"><span data-stu-id="b0e18-110">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)                 | <span data-ttu-id="b0e18-111">Enthält Informationen zur Verwendung des proxylocatorobjekts, das den Proxy bestimmt, der beim Herstellen einer Verbindung mit einem Server verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b0e18-111">Provides information about using the proxy locator object that determines the proxy to use when connecting to a server.</span></span>                 |
| [<span data-ttu-id="b0e18-112">Netzwerk Quellen Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="b0e18-112">Network Source Authentication</span></span>](network-source-authentication.md)                         | <span data-ttu-id="b0e18-113">Enthält Informationen zur Verwendung der Authentifizierungs Komponenten, z. b. des Anmelde Informations Caches und der Anmelde Informationsverwaltung.</span><span class="sxs-lookup"><span data-stu-id="b0e18-113">Provides information about using the authentication components such as the credential cache and the credential manager.</span></span>                 |
| [<span data-ttu-id="b0e18-114">So erhalten Sie Ereignisse aus der Netzwerkquelle</span><span class="sxs-lookup"><span data-stu-id="b0e18-114">How to Get Events from the Network Source</span></span>](how-to-get-events-from-the-network-source.md) | <span data-ttu-id="b0e18-115">Bietet Informationen zum Media Foundation Ereignissen während des Öffnens einer Verbindung und vor der Erstellung der Netzwerkquelle.</span><span class="sxs-lookup"><span data-stu-id="b0e18-115">Provides information about getting Media Foundation events during the opening of a connection and before the network source is created.</span></span> |
| [<span data-ttu-id="b0e18-116">Unterstützte Protokolle</span><span class="sxs-lookup"><span data-stu-id="b0e18-116">Supported Protocols</span></span>](supported-protocols.md)                                             | <span data-ttu-id="b0e18-117">Beschreibt die Protokolle, die von der Netzwerkquelle unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="b0e18-117">Describes the protocols that are supported by the network source.</span></span> <span data-ttu-id="b0e18-118">Bietet außerdem Informationen über die protokollrolloverprozedur.</span><span class="sxs-lookup"><span data-stu-id="b0e18-118">Also, provides information about the protocol rollover procedure.</span></span>     |
| [<span data-ttu-id="b0e18-119">Client Protokollierung</span><span class="sxs-lookup"><span data-stu-id="b0e18-119">Client Logging</span></span>](client-logging.md)                                                       | <span data-ttu-id="b0e18-120">Beschreibt die Client Protokollierungs Felder, die von der Anwendung konfiguriert werden können, und wie Sie Netzwerk Statistiken abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="b0e18-120">Describes the client logging fields that the application can configure and how it can retrieve network statistics.</span></span>                      |



 

## <a name="related-topics"></a><span data-ttu-id="b0e18-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b0e18-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0e18-122">Media Foundation-Programmier Handbuch</span><span class="sxs-lookup"><span data-stu-id="b0e18-122">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="b0e18-123">Medienquellen</span><span class="sxs-lookup"><span data-stu-id="b0e18-123">Media Sources</span></span>](media-sources.md)
</dt> <dt>

[<span data-ttu-id="b0e18-124">Verwenden von Medienquellen mit der Medien Sitzung</span><span class="sxs-lookup"><span data-stu-id="b0e18-124">Using Media Sources with the Media Session</span></span>](using-media-sources-with-the-media-session.md)
</dt> </dl>

 

 



