---
title: Präsentation
description: Präsentation ist der letzte Schritt im UPnP-Prozess.
ms.assetid: e8d20ae6-2dd8-4de2-b07b-6cf4e725735e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 195399316882de71c148f2369dd2978c4cfbd728
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855959"
---
# <a name="presentation"></a><span data-ttu-id="09f30-103">Präsentation</span><span class="sxs-lookup"><span data-stu-id="09f30-103">Presentation</span></span>

<span data-ttu-id="09f30-104">Präsentation ist der letzte Schritt im UPnP-Prozess.</span><span class="sxs-lookup"><span data-stu-id="09f30-104">Presentation is the final step in the UPnP process.</span></span> <span data-ttu-id="09f30-105">Wenn ein Gerät über eine URL zur Darstellung verfügt, kann ein Kontrollpunkt eine Seite aus dieser URL abrufen und die Seite in einen Browser laden.</span><span class="sxs-lookup"><span data-stu-id="09f30-105">If a device has a URL for presentation, a control point can retrieve a page from this URL and load the page into a browser.</span></span> <span data-ttu-id="09f30-106">Abhängig von den Funktionen der Präsentationsseite und des Geräts kann der Steuerungspunkt das Gerät steuern und den Status des Geräts anzeigen.</span><span class="sxs-lookup"><span data-stu-id="09f30-106">Depending on the capabilities of the presentation page and the device, the control point can control the device and view the status of the device.</span></span>

<span data-ttu-id="09f30-107">Der Ressourcen Pfad, der während der Registrierung an [**iupnpregistrinar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) übermittelt wird, ist der Ort, an dem alle für die Darstellung des Geräts relevanten Dateien gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="09f30-107">The resource path, which is passed to [**IUPnPRegistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) during registration, is where all the files relevant to the presentation of the device are located.</span></span> <span data-ttu-id="09f30-108">Geräte Entwickler können für jedes eingebettete Gerät separate Seiten bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="09f30-108">Device developers can provide separate pages for each embedded device.</span></span> <span data-ttu-id="09f30-109">Die Präsentations-URL in der Geräte Beschreibungs Vorlage kann entweder ein absolute URL oder ein relative URL sein.</span><span class="sxs-lookup"><span data-stu-id="09f30-109">The presentation URL in the device description template can either be an absolute URL or a relative URL.</span></span> <span data-ttu-id="09f30-110">Bei relativen URLs, die relativ zum Ressourcen Pfad sind, sollte die Vorlage für die Geräte Beschreibung einen Dateinamen enthalten.</span><span class="sxs-lookup"><span data-stu-id="09f30-110">For relative URLs, which are relative to the resource path, the device description template should contain a file name.</span></span> <span data-ttu-id="09f30-111">**Iupnpregistrinar** konvertiert diese in eine URL mit dem tatsächlichen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="09f30-111">**IUPnPRegistrar** converts this to a URL with the actual location.</span></span> <span data-ttu-id="09f30-112">Bei absoluten URLs wird der Speicherort nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="09f30-112">For absolute URLs, the location is not modified.</span></span>

<span data-ttu-id="09f30-113">Zur Unterstützung von Client seitigen Skripts auf einer Präsentationsseite werden in der Regel zusätzliche Informationen in Form einer "Abfrage Zeichenfolge" an die URL angehängt.</span><span class="sxs-lookup"><span data-stu-id="09f30-113">To support client side scripts within a presentation page, extra information is normally appended to the URL in the form of a "query string".</span></span> <span data-ttu-id="09f30-114">Die zusätzlichen Informationen, die angefügt werden, sind die URL zum Dokument mit der Geräte Beschreibung und der udn des Geräts oder eingebetteten Geräts.</span><span class="sxs-lookup"><span data-stu-id="09f30-114">The extra information that is appended is the URL to the device description document, and the UDN of the device or embedded device.</span></span> <span data-ttu-id="09f30-115">Die URL für die Geräte Beschreibung kann verwendet werden, um ein Beschreibungs Dokument in das Skript zu laden und das Gerät dann über seine Dienste zu steuern.</span><span class="sxs-lookup"><span data-stu-id="09f30-115">The device description URL can be used to load a description document in the script, and then control the device through its services.</span></span> <span data-ttu-id="09f30-116">Der udn wird verwendet, um ein eingebettetes Gerät aus dem Stamm Gerät auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="09f30-116">The UDN is used to select an embedded device from the root device.</span></span>

<span data-ttu-id="09f30-117">Das Format der geänderten Präsentations-URL lautet: die tatsächliche Präsentations-URL, ein Fragezeichen ("?"), die URL für die Geräte Beschreibung, ein Pluszeichen ("+"), das udn des Geräts.</span><span class="sxs-lookup"><span data-stu-id="09f30-117">The format of the modified presentation URL is: the actual presentation URL, a question mark ("?"), the device description URL, a plus sign ("+"), the device UDN.</span></span> <span data-ttu-id="09f30-118">Das Fragezeichen gibt den Anfang der Abfrage Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="09f30-118">The question mark denotes the start of the query string.</span></span>

<span data-ttu-id="09f30-119">Wenn die Präsentations-URL in der Geräte Beschreibungs Vorlage eine absolute URL ist, die bereits ein Fragezeichen ("?") enthielt, werden die zusätzlichen Informationen nicht der Präsentations-URL hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="09f30-119">If the presentation URL in the device description template was an absolute URL and it already contained a question mark ("?"), then the extra information is not added to the presentation URL.</span></span>



| <span data-ttu-id="09f30-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="09f30-120">Description</span></span>                        | <span data-ttu-id="09f30-121">URL</span><span class="sxs-lookup"><span data-stu-id="09f30-121">URL</span></span>                                                                                                                                               |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09f30-122">In der Vorlage Geräte Beschreibung</span><span class="sxs-lookup"><span data-stu-id="09f30-122">In the device description template</span></span> | <span data-ttu-id="09f30-123">**presentationurl** MyDevice.html **/presentationURL**</span><span class="sxs-lookup"><span data-stu-id="09f30-123">**presentationURL** MyDevice.html **/presentationURL**</span></span>                                                                                              |
| <span data-ttu-id="09f30-124">Vom Geräte Host generiert</span><span class="sxs-lookup"><span data-stu-id="09f30-124">Generated by the device host</span></span>       | <span data-ttu-id="09f30-125">**presentationurl** https://machinename/deviceID/MyDevice.html/?https://machine/upnphost/udhisapi.dll?content=uuid:487394 ...</span><span class="sxs-lookup"><span data-stu-id="09f30-125">**presentationURL**https://machinename/deviceID/MyDevice.html/?https://machine/upnphost/udhisapi.dll?content=uuid:487394…</span></span> <span data-ttu-id="09f30-126">+ Udn **/presentationURL**</span><span class="sxs-lookup"><span data-stu-id="09f30-126">+ UDN **/presentationURL**</span></span> |



 

<span data-ttu-id="09f30-127">Ein Client seitiges Skript muss möglicherweise die URL der Geräte Beschreibung aus der Präsentations-URL extrahieren, um das [**iupnpdescriptiondocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) -Objekt zu laden.</span><span class="sxs-lookup"><span data-stu-id="09f30-127">A client-side script may have to extract the device description URL from the presentation URL to load the [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) object.</span></span> <span data-ttu-id="09f30-128">Dies erfolgt durch das übernehmen der Abfrage Zeichenfolge und das Beenden des Plus Zeichens ("+").</span><span class="sxs-lookup"><span data-stu-id="09f30-128">This is done by taking the query string, and terminating it at the plus sign ("+").</span></span>


```VB
Dim QueryString
QueryString = window.location.search
Dim DescURLString
DescURLString = Trim(Mid(QueryString,2,Instr(QueryString,"+")-2))& vbCrLf

    Dim LightDesc
    Set LightDesc = CreateObject("UPnP.DescriptionDocument.1")
    LightDesc.Load(DescURLString)
```



<span data-ttu-id="09f30-129">Im Fall einer Präsentationsseite für ein eingebettetes Gerät sind einige zusätzliche Arbeitsschritte erforderlich.</span><span class="sxs-lookup"><span data-stu-id="09f30-129">In the case of a presentation page for an embedded device, some additional work is required.</span></span> <span data-ttu-id="09f30-130">Nach dem Laden von [**upnpdescriptiondocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument)muss das Skript die Sammlung eingebetteter Geräte abrufen und dann das Gerät auswählen, das mit dem udn in der Abfrage Zeichenfolge übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="09f30-130">After loading the [**UPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument), the script must obtain the collection of embedded devices, then select the device that matches the UDN in the query string.</span></span> <span data-ttu-id="09f30-131">Das folgende Skript zeigt, wie Sie das eingebettete Gerät für die aktuelle Präsentationsseite auswählen.</span><span class="sxs-lookup"><span data-stu-id="09f30-131">The following script shows how to select the embedded device for the current presentation page.</span></span> <span data-ttu-id="09f30-132">Es wird davon ausgegangen, dass lightdesc bereits geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="09f30-132">It assumes LightDesc is already loaded.</span></span>


```VB
Dim LightDevice
Set LightDevice = LightDesc.RootDevice

Dim EmbeddedDevices 
set EmbeddedDevices = LightDevice.Children

Dim DeviceUdnString
DeviceUdnString = Trim(Mid(QueryString,Instr(QueryString,"+")+1,Len(QueryString)))

Dim Item
set Item = EmbeddedDevices.Item(DeviceUdnString)
```



 

 




