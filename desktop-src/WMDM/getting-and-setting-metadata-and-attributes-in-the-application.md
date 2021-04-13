---
title: Zugreifen auf Metadaten und Attribute in der APP
description: Erhalten und Festlegen von Metadaten und Attributen in der Anwendung
ms.assetid: 308a722d-1c65-41eb-a0e2-21171eb410d5
keywords:
- Windows Media-Device Manager, Metadaten
- Device Manager, Metadaten
- Programmier Handbuch, Metadaten
- Desktop Anwendungen, Metadaten
- Erstellen von Windows Media Device Manager-Anwendungen, Metadaten
- metadata
- Windows Media-Device Manager, Attribute
- Device Manager, Attribute
- Programmier Handbuch, Attribute
- Desktop Anwendungen, Attribute
- Erstellen von Windows Media Device Manager-Anwendungen, Attributen
- attributes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a78dbb31ebcc5ec99b1db3503b386b09b5a3c05
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/27/2019
ms.locfileid: "104313853"
---
# <a name="accessing-metadata-and-attributes-in-the-app"></a><span data-ttu-id="1226e-115">Zugreifen auf Metadaten und Attribute in der APP</span><span class="sxs-lookup"><span data-stu-id="1226e-115">Accessing metadata and attributes in the app</span></span>

<span data-ttu-id="1226e-116">Eine allgemeine Erläuterung der Metadaten und Attribute finden Sie unter [erhalten und Festlegen von Metadaten und Attributen](getting-and-setting-metadata-and-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="1226e-116">A general discussion of metadata and attributes is available in [Getting and Setting Metadata and Attributes](getting-and-setting-metadata-and-attributes.md).</span></span> <span data-ttu-id="1226e-117">In diesem Abschnitt werden bestimmte Anwendungsmethoden Aufrufe zum Abrufen oder Festlegen von Werten behandelt.</span><span class="sxs-lookup"><span data-stu-id="1226e-117">This section covers specific application method calls to retrieve or set values.</span></span>

<span data-ttu-id="1226e-118">Anwendungen können Attribute oder Metadaten zu einem bestimmten Speicher abrufen, indem Sie [**iwmdmstorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes), [**IWMDMStorage2:: GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2), [**IWMDMStorage3:: GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) oder [**IWMDMStorage4:: getspecifiedmetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1226e-118">Applications can retrieve attributes or metadata about a specific storage by calling [**IWMDMStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes), [**IWMDMStorage2::GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2), [**IWMDMStorage3::GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) or [**IWMDMStorage4::GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata).</span></span> <span data-ttu-id="1226e-119">**GetMetadata** Ruft eine vollständige Auflistung aller Metadaten ab, die einem Speicher zugeordnet sind, und die Anwendung kann dann alle Werte durchlaufen oder bestimmte Werte aus der Sammlung anfordern.</span><span class="sxs-lookup"><span data-stu-id="1226e-119">**GetMetadata** retrieves a full collection of all the metadata associated with a storage, and the application can then enumerate through all values or request specific values from the collection.</span></span> <span data-ttu-id="1226e-120">**Getspecifiedmetadata** erstellt im Namen des Aufrufers ein Metadatenobjekt.</span><span class="sxs-lookup"><span data-stu-id="1226e-120">**GetSpecifiedMetadata** creates a metadata object on behalf of the caller.</span></span> <span data-ttu-id="1226e-121">Der Aufrufer kann eine Teilmenge der verfügbaren Daten anfordern, indem er den *ppwszpropnames* -Parameter mit einem Array der gewünschten Eigenschaften Zeichenfolgen für Windows Media Device Manager und die Anzahl dieses Arrays abfüllt.</span><span class="sxs-lookup"><span data-stu-id="1226e-121">The caller may request a subset of the available data by filling in the *ppwszPropNames* parameter with an array of the desired Windows Media Device Manager property strings, and the count of that array.</span></span> <span data-ttu-id="1226e-122">Das zurückgegebene Metadatenobjekt wird mit den Eigenschaften aufgefüllt, die abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="1226e-122">The returned metadata object will be filled with those properties that could be retrieved.</span></span> <span data-ttu-id="1226e-123">Die Eigenschaften, die nicht abgerufen werden konnten, sind nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1226e-123">Those properties that couldn't be retrieved will be absent.</span></span> <span data-ttu-id="1226e-124">Metadaten werden auf Grundlage der bestmöglichen Leistung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1226e-124">Metadata is returned on a best-effort basis.</span></span>

<span data-ttu-id="1226e-125">Ein Gerät kann Attribute oder Metadaten für einen Speicher durch Aufrufen von [**iwmdmstorage:: SetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-setattributes), [**IWMDMStorage2:: SetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-setattributes2)oder [**IWMDMStorage3:: SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata)festlegen.</span><span class="sxs-lookup"><span data-stu-id="1226e-125">A device can set attributes or metadata on a storage by calling [**IWMDMStorage::SetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-setattributes), [**IWMDMStorage2::SetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-setattributes2), or [**IWMDMStorage3::SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata).</span></span> <span data-ttu-id="1226e-126">Beachten Sie, dass es keine Garantie gibt, dass die festgelegten Werte beibehalten werden, da Sie möglicherweise in einem nicht persistenten externen Dateispeicher gespeichert werden. die Werte werden möglicherweise nicht unterstützt, oder das Gerät unterstützt die Eigenschaften möglicherweise nicht als beschreibbar.</span><span class="sxs-lookup"><span data-stu-id="1226e-126">Note that there is no guarantee that any values set will persist, because they may be stored in a non-persistent external file store, the values may not be supported, or, the device may not support the properties as writeable.</span></span>

<span data-ttu-id="1226e-127">Sie können auch Metadaten zu einem Gerät abrufen oder festlegen, indem Sie [**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) oder [**IWMDMDevice3:: SetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-setproperty)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1226e-127">You can also get or set metadata about a device by calling [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) or [**IWMDMDevice3::SetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-setproperty).</span></span> <span data-ttu-id="1226e-128">Am Ende der [metadatenkonstanten](metadata-constants.md)ist eine separate Tabelle mit gerätemetadatenkonstanten aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="1226e-128">There is a separate table of device metadata constants listed at the end of [Metadata Constants](metadata-constants.md).</span></span>

<span data-ttu-id="1226e-129">Beispiele für die Verwendung dieser Methoden finden Sie in der Referenz Dokumentation jeder Methode.</span><span class="sxs-lookup"><span data-stu-id="1226e-129">Examples of using these methods are given in each method's reference documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1226e-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1226e-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1226e-131">**Erstellen einer Windows Media Device Manager-Anwendung**</span><span class="sxs-lookup"><span data-stu-id="1226e-131">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> <dt>

[<span data-ttu-id="1226e-132">**Erhalten und Festlegen von Metadaten und Attributen**</span><span class="sxs-lookup"><span data-stu-id="1226e-132">**Getting and Setting Metadata and Attributes**</span></span>](getting-and-setting-metadata-and-attributes.md)
</dt> </dl>

 

 




