---
description: Proxy Unterstützung für Netzwerk Quellen
ms.assetid: e739746d-2a09-4237-a7c1-0aed4e4516d7
title: Proxy Unterstützung für Netzwerk Quellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97bc1172c072a54f9f76cbcd3a297a972efbde29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349083"
---
# <a name="proxy-support-for-network-sources"></a><span data-ttu-id="7f210-103">Proxy Unterstützung für Netzwerk Quellen</span><span class="sxs-lookup"><span data-stu-id="7f210-103">Proxy Support for Network Sources</span></span>

<span data-ttu-id="7f210-104">Bei einem Proxy Server handelt es sich um einen zwischengeschalteten Server zwischen Ihrem Intranet und dem Internet, der Anforderungen von der Client Anwendung an den Medienserver weiterleitet und Dateien vom Medienserver abruft.</span><span class="sxs-lookup"><span data-stu-id="7f210-104">A proxy server is an intermediate server between your intranet and the Internet, which routes requests from the client application to the media server and retrieves files from the media server.</span></span>

<span data-ttu-id="7f210-105">Media Foundation implizit ein *proxylocatorobjekt* erstellt, wenn eine Client Anwendung versucht, auf eine Quell-URL zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="7f210-105">Media Foundation implicitly creates a *proxy locator* object when a client application tries to access a source URL.</span></span> <span data-ttu-id="7f210-106">Das proxylocator-Objekt macht die [**IMF netproxylocator**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocator) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7f210-106">The proxy locator object exposes the [**IMFNetProxyLocator**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocator) interface.</span></span> <span data-ttu-id="7f210-107">Während der Quell Auflösung prüft Media Foundation den an die Quell Auflösungsmethode übergebenen Eigenschaften Speicher.</span><span class="sxs-lookup"><span data-stu-id="7f210-107">During source resolution, Media Foundation checks the property store passed to the source resolver method.</span></span>

<span data-ttu-id="7f210-108">Wenn der Eigenschaften Speicher die Eigenschaft " [mfnetsource \_ proxylocatorfactory](mfnetsource-proxylocatorfactory-property.md) " enthält, die auf ein von der Anwendung implementiertes proxylocatorfactoryobjekt festgelegt ist, ruft es die [**imfnetproxylocatorfactory::**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) -Methode zum Erstellen eines proxylocators mit benutzerdefinierten Konfigurationseinstellungen auf.</span><span class="sxs-lookup"><span data-stu-id="7f210-108">If the property store contains the [MFNETSOURCE\_PROXYLOCATORFACTORY](mfnetsource-proxylocatorfactory-property.md) property set to a proxy locator factory object implemented by the application then, it invokes the [**IMFNetProxyLocatorFactory::CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) method to create a proxy locator with custom configuration settings.</span></span>

<span data-ttu-id="7f210-109">Wenn der Eigenschaften Speicher nicht festgelegt ist, erstellt Media Foundation den proxylocator mit der Standardkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="7f210-109">If the property store is not set, then Media Foundation creates the proxy locator with default configuration.</span></span> <span data-ttu-id="7f210-110">Diese Einstellungen lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7f210-110">These settings are as follows:</span></span>

-   <span data-ttu-id="7f210-111">Wenn die Benutzer Richtlinie festgelegt ist, verwendet der proxylocator die in der Registrierung angegebenen Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="7f210-111">If user policy is set, then the proxy locator uses settings specified in the registry.</span></span>

-   <span data-ttu-id="7f210-112">Für HTTP verwendet der proxylocator die Browser Proxy Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="7f210-112">For HTTP, the proxy locator uses browser proxy settings.</span></span>

-   <span data-ttu-id="7f210-113">Bei RTSP ist der proxylocator so konfiguriert, dass Proxy Server beim Herstellen einer Verbindung mit dem Medienserver umgangen werden.</span><span class="sxs-lookup"><span data-stu-id="7f210-113">For RTSP, the proxy locator is configured to bypass proxy servers when connecting to the media server.</span></span>

<span data-ttu-id="7f210-114">Diese Standardkonfiguration kann von der Anwendung geändert werden.</span><span class="sxs-lookup"><span data-stu-id="7f210-114">This default configuration can be changed by the application.</span></span> <span data-ttu-id="7f210-115">Die folgenden Themen enthalten Informationen zu den Konfigurationseinstellungen für einen proxylocator:</span><span class="sxs-lookup"><span data-stu-id="7f210-115">The following topics contain information about the configuration settings for a proxy locator:</span></span>

-   [<span data-ttu-id="7f210-116">Proxy Locator-Konfigurationseinstellungen</span><span class="sxs-lookup"><span data-stu-id="7f210-116">Proxy Locator Configuration Settings</span></span>](proxy-locator-configuration-settings.md)

-   [<span data-ttu-id="7f210-117">Konfigurieren des proxylocators</span><span class="sxs-lookup"><span data-stu-id="7f210-117">How to Configure the Proxy Locator</span></span>](how-to-configure-the-proxy-locator.md)

<span data-ttu-id="7f210-118">Media Foundation initialisiert den proxylocator für die Quell-URL, die für den [quellresolver](source-resolver.md)angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="7f210-118">Media Foundation initializes the proxy locator for the source URL specified to the [Source Resolver](source-resolver.md).</span></span> <span data-ttu-id="7f210-119">Der proxylocator erkennt einen Proxy Server, der auf der Grundlage der Konfigurationseinstellungen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7f210-119">The proxy locator detects a proxy server to use based on configuration settings.</span></span> <span data-ttu-id="7f210-120">Wenn der proxylocator versucht, den Proxy Server festzulegen, wird der Erfolg oder das Fehler Ergebnis in der Registrierung aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="7f210-120">When the proxy locator attempts the set a proxy server, it records the success or failure result in the registry.</span></span> <span data-ttu-id="7f210-121">Dieser Wert wird beim nächsten Proxy Erkennungsprozess geprüft.</span><span class="sxs-lookup"><span data-stu-id="7f210-121">This value is checked during the next proxy detection process.</span></span> <span data-ttu-id="7f210-122">Wenn ein bestimmter Proxy Server bekanntermaßen in der Vergangenheit Ausfälle verursacht hat, überspringt der proxylocator ihn.</span><span class="sxs-lookup"><span data-stu-id="7f210-122">If a certain proxy server is known to have caused failures in the past, the proxy locator skips it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f210-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7f210-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f210-124">Attribute und Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7f210-124">Attributes and Properties</span></span>](attributes-and-properties.md)
</dt> <dt>

[<span data-ttu-id="7f210-125">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7f210-125">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 



