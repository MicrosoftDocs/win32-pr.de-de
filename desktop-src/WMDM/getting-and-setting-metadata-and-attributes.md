---
title: Erhalten und Festlegen von Metadaten und Attributen
description: Erhalten und Festlegen von Metadaten und Attributen
ms.assetid: 83534998-4e7d-49b6-a160-ef9a0ddea5db
keywords:
- Windows Media-Device Manager, Attribute
- Device Manager, Attribute
- Desktop Anwendungen, Attribute
- Dienstanbieter, Attribute
- Programmier Handbuch, Attribute
- attributes
- Windows Media-Device Manager, Metadaten
- Device Manager, Metadaten
- Desktop Anwendungen, Metadaten
- Dienstanbieter, Metadaten
- Programmier Handbuch, Metadaten
- metadata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8697f62dac44f5aab4b08aa4f6c516ac35a17e4e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856351"
---
# <a name="getting-and-setting-metadata-and-attributes"></a><span data-ttu-id="fae00-115">Erhalten und Festlegen von Metadaten und Attributen</span><span class="sxs-lookup"><span data-stu-id="fae00-115">Getting and Setting Metadata and Attributes</span></span>

<span data-ttu-id="fae00-116">Eine Anwendung kann zwei Arten von Informationen über einen Speicher oder ein Gerät erhalten: Attribute und Metadaten.</span><span class="sxs-lookup"><span data-stu-id="fae00-116">An application can get two kinds of information about a storage or device: attributes and metadata.</span></span> <span data-ttu-id="fae00-117">Attribute sind einfachere boolesche Werte, die in der Regeldatei Systeminformationen beschreiben, z. b. ob ein Speicher über untergeordnete Objekte verfügt, ob er umbenannt, gelesen oder gelöscht werden kann usw.</span><span class="sxs-lookup"><span data-stu-id="fae00-117">Attributes are simpler Boolean values that generally describe file system information, such as whether a storage has child objects, whether it can be renamed, read, or deleted, and so on.</span></span> <span data-ttu-id="fae00-118">Attribute werden durch den Aufruf von [**iwmdmstorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) oder [**IWMDMStorage2:: GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2)als Flags-Werte abgerufen.</span><span class="sxs-lookup"><span data-stu-id="fae00-118">Attributes are retrieved as flags values by calling [**IWMDMStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) or [**IWMDMStorage2::GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2).</span></span> <span data-ttu-id="fae00-119">Attribute werden durch Aufrufen von [**IWMDMStorage3:: SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata)festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fae00-119">Attributes are set by calling [**IWMDMStorage3::SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata).</span></span>

<span data-ttu-id="fae00-120">Eine Anwendung kann auch komplexere Daten (numerisch, Zeichenfolge oder andere Datentypen) als *Metadaten* anfordern.</span><span class="sxs-lookup"><span data-stu-id="fae00-120">An application can also request more complex data (numeric, string, or other data types) as *metadata*.</span></span> <span data-ttu-id="fae00-121">Metadatenwerte werden durch eindeutige Zeichen folgen Namen identifiziert.</span><span class="sxs-lookup"><span data-stu-id="fae00-121">Metadata values are identified by unique string names.</span></span> <span data-ttu-id="fae00-122">Windows Media Device Manager definiert eine Liste von Zeichen folgen Konstanten, die verwendet werden können, um Werte anzufordern. Diese definierten Werte sind unter [metadatenkonstanten](metadata-constants.md)aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="fae00-122">Windows Media Device Manager defines a list of string constants that can be used to request values; these defined values are listed in [Metadata Constants](metadata-constants.md).</span></span> <span data-ttu-id="fae00-123">Ein Dienstanbieter kann seine eigenen Konstanten definieren, aber eine aufrufende Anwendung muss diese Definitionen beachten, um diese benutzerdefinierten Metadatenwerte anzufordern oder festzulegen.</span><span class="sxs-lookup"><span data-stu-id="fae00-123">A service provider can define its own constants, but a calling application must be aware of these definitions in order to request or set these custom metadata values.</span></span> <span data-ttu-id="fae00-124">Die Anwendung fordert Metadaten durch Aufrufen von [**IWMDMStorage3:: GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) oder [**IWMDMStorage4:: getspecifiedmetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata)an.</span><span class="sxs-lookup"><span data-stu-id="fae00-124">The application requests metadata by calling [**IWMDMStorage3::GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) or [**IWMDMStorage4::GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata).</span></span>

<span data-ttu-id="fae00-125">Ein wichtiger Aspekt beim Abrufen und Festlegen von Metadaten und Attributen besteht darin, zu verstehen, woher die abgerufenen Werte stammen.</span><span class="sxs-lookup"><span data-stu-id="fae00-125">An important aspect of getting and setting metadata and attributes is understanding where the retrieved values come from.</span></span> <span data-ttu-id="fae00-126">Der Dienstanbieter oder das Gerät kann diese Werte von vielen verschiedenen Orten erhalten, einschließlich der folgenden:</span><span class="sxs-lookup"><span data-stu-id="fae00-126">The service provider or the device can get these values from many different places, including the following:</span></span>

-   <span data-ttu-id="fae00-127">Aus dem Dateiheader.</span><span class="sxs-lookup"><span data-stu-id="fae00-127">From the file header.</span></span> <span data-ttu-id="fae00-128">In einer ASF-Datei wird die Bitrate z. b. im Dateiheader gespeichert.</span><span class="sxs-lookup"><span data-stu-id="fae00-128">For example, in an ASF file, the bit rate is stored in the file header.</span></span>
-   <span data-ttu-id="fae00-129">Aus Werten, die explizit von der Anwendung festgelegt werden, wenn eine Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="fae00-129">From values set explicitly by the application when calling a method.</span></span> <span data-ttu-id="fae00-130">Diese Werte können in einem externen Metadatenspeicher im Dienstanbieter oder auf dem Gerät gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="fae00-130">These values may be saved in an external metadata store in the service provider or the device.</span></span> <span data-ttu-id="fae00-131">Dieser Speicher kann beibehalten werden, wenn das Gerät die Verbindung trennt oder ausgeschaltet wird.</span><span class="sxs-lookup"><span data-stu-id="fae00-131">This store may or may not persist when the device disconnects or turns off.</span></span> <span data-ttu-id="fae00-132">Beispielsweise werden der Wert für die Wiedergabe Anzahl und die Benutzer Sterne in der Regel in externen Stores auf dem Computer oder auf dem Gerät gespeichert.</span><span class="sxs-lookup"><span data-stu-id="fae00-132">For example, the play count and user star ratings are typically stored in external stores on the computer or device.</span></span>
-   <span data-ttu-id="fae00-133">Durch Untersuchen von Informationen, die vom Dateisystem bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="fae00-133">By examining information provided by the file system.</span></span> <span data-ttu-id="fae00-134">Beispielsweise, ob eine Datei schreibgeschützt ist oder ob ein Ordner über untergeordnete Elemente verfügt.</span><span class="sxs-lookup"><span data-stu-id="fae00-134">For example, whether a file is read-only or whether a folder has children.</span></span>
-   <span data-ttu-id="fae00-135">Durch Öffnen und übernehmen der Datei Daten.</span><span class="sxs-lookup"><span data-stu-id="fae00-135">By opening and parsing the file data.</span></span>

<span data-ttu-id="fae00-136">Es ist wichtig zu wissen, dass eine Eigenschaft möglicherweise an mehr als einem Speicherort (innerhalb des Datei Headers und auch in einem lokalen Speicher) gespeichert wird und dass Sie bearbeitet werden kann oder nicht.</span><span class="sxs-lookup"><span data-stu-id="fae00-136">It is important to realize that a property might be stored in more than one location (within the file header and also in a local store), and that it may or may not be editable.</span></span> <span data-ttu-id="fae00-137">Beispielsweise kann es sein, dass das Ändern einer Dateibeschreibung persistent ist. Wenn der Dienstanbieter die Beschreibung lokal speichert, wird er nicht auf dem Gerät gespeichert.</span><span class="sxs-lookup"><span data-stu-id="fae00-137">For example, changing a file description may or may not be persistent; if the service provider stores the description locally, it will not persist on the device.</span></span> <span data-ttu-id="fae00-138">Ebenso gilt: Wenn die Dateibeschreibung aus dem Dateiheader entnommen wird, ist eine Änderung der Datei nur persistent, wenn der Dienstanbieter oder das Gerät geöffnet wird und die Header Daten ändert.</span><span class="sxs-lookup"><span data-stu-id="fae00-138">Similarly, if the file description is taken from the file header, modifying this will only be persistent if the service provider or device opens and modifies the header data.</span></span> <span data-ttu-id="fae00-139">Die meisten Anwendungen haben einen optimalen Versuch, wenn Sie die gewünschten Werte ändern, aber nicht davon abhängen, dass Eigenschaften permanent geändert werden.</span><span class="sxs-lookup"><span data-stu-id="fae00-139">Most applications make a best attempt by changing desired values, but do not depend on any properties to be persistently changed.</span></span>

<span data-ttu-id="fae00-140">Weitere Informationen zum erhalten und Festlegen von Werten finden Sie in den entsprechenden Abschnitten für Anwendungsentwickler und Dienstanbieter Entwickler später in der-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="fae00-140">More information on getting and setting values is given in the appropriate sections for application developers and service provider developers later in the documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fae00-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fae00-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fae00-142">**Allgemeine Aufgaben für Anwendungen und Dienstanbieter**</span><span class="sxs-lookup"><span data-stu-id="fae00-142">**Tasks Common to Applications and Service Providers**</span></span>](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 




