---
description: Dieses Thema gilt für Windows Vista und höher.
ms.assetid: 4d88806a-68a6-4394-a704-c7a47a0fdc70
title: Integration in Windows Photo Gallery und Windows-Explorer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b2ab2bb725b151a069f53a94a8fb2e31766132d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349973"
---
# <a name="integration-with-windows-photo-gallery-and-windows-explorer"></a><span data-ttu-id="ef4f5-103">Integration in Windows Photo Gallery und Windows-Explorer</span><span class="sxs-lookup"><span data-stu-id="ef4f5-103">Integration with Windows Photo Gallery and Windows Explorer</span></span>

<span data-ttu-id="ef4f5-104">Dieses Thema gilt für Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-104">This topic applies to Windows Vista and later.</span></span> <span data-ttu-id="ef4f5-105">Sie enthält die folgenden Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="ef4f5-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="ef4f5-106">Introduction (Einführung)</span><span class="sxs-lookup"><span data-stu-id="ef4f5-106">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="ef4f5-107">Integration in den Windows-Eigenschaften Speicher</span><span class="sxs-lookup"><span data-stu-id="ef4f5-107">Integration with the Windows Property Store</span></span>](#integration-with-the-windows-property-store)
-   [<span data-ttu-id="ef4f5-108">Integration in die Windows-Fotogalerie</span><span class="sxs-lookup"><span data-stu-id="ef4f5-108">Integration with the Windows Photo Gallery</span></span>](#integration-with-the-windows-photo-gallery)
-   [<span data-ttu-id="ef4f5-109">Integration in den Windows-Miniatur Ansichts Cache</span><span class="sxs-lookup"><span data-stu-id="ef4f5-109">Integration with the Windows Thumbnail Cache</span></span>](#integration-with-the-windows-thumbnail-cache)
-   [<span data-ttu-id="ef4f5-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ef4f5-110">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="ef4f5-111">Einführung</span><span class="sxs-lookup"><span data-stu-id="ef4f5-111">Introduction</span></span>

<span data-ttu-id="ef4f5-112">Um die Windows-Fotogalerie und Windows-Explorer zum Anzeigen von Miniaturansichten und zum Suchen und Aktualisieren von Standardbild Metadaten zu aktivieren, muss einem Codec eine Implementierung der [IThumbnailProvider](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) -und [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Schnittstellen zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-112">To enable Windows Photo Gallery and Windows Explorer to display thumbnails and search and update standard image metadata, a codec must have an implementation of the [IThumbnailProvider](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) and [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) interfaces associated with it.</span></span> <span data-ttu-id="ef4f5-113">Die IThumbnailProvider-Schnittstelle wird verwendet, um Miniaturansichten abzurufen und den Miniatur Ansichts Cache aufzufüllen, und die IPropertyStore-Schnittstelle wird zum Suchen und Aktualisieren von Metadaten verwendet, die einer Datei zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-113">The IThumbnailProvider interface is used to retrieve thumbnails and populate the thumbnail cache, and the IPropertyStore interface is used for searching and updating metadata associated with a file.</span></span> <span data-ttu-id="ef4f5-114">Ab Windows Vista verfügen alle Dateitypen über Miniaturansichten und Metadaten, aber für unterschiedliche Dateitypen sind unterschiedliche Implementierungen dieser Schnittstellen erforderlich, um die Miniaturansichten und Metadaten abzurufen oder zu generieren.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-114">As of Windows Vista, all file types have thumbnails and metadata, but different file types require different implementations of these interfaces to retrieve or generate the thumbnails and metadata for them.</span></span> <span data-ttu-id="ef4f5-115">Das System stellt Standard Implementierungen dieser Schnittstellen bereit.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-115">The system provides default implementations of these interfaces.</span></span> <span data-ttu-id="ef4f5-116">Die Standard Implementierung von IThumbnailProvider kann für alle Windows Imaging Component (WIC) – aktivierte Bildformate verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-116">The default implementation of IThumbnailProvider can be used for any Windows Imaging Component (WIC)–enabled image format.</span></span> <span data-ttu-id="ef4f5-117">Die Standard Implementierung von IPropertyStore kann mit jedem WIC-fähigen Bildformat verwendet werden, das auf einem Tagged Image File Format (TIFF)-oder JPEG-Container basiert.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-117">The default implementation of IPropertyStore can be used with any WIC-enabled image format that is based on a Tagged Image File Format (TIFF) or JPEG container.</span></span> <span data-ttu-id="ef4f5-118">Um das Bildformat den Standard Implementierungen dieser beiden Schnittstellen zuzuordnen, müssen Sie nur wenige Registrierungseinträge hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-118">To associate your image format with the default implementations of both of these interfaces, you must add just a few registry entries.</span></span>

<span data-ttu-id="ef4f5-119">In den folgenden Einträgen wird die Windows-Fotogalerie und der Windows-Explorer angezeigt, dass die Dateinamenerweiterung (. ext) und der zugehörige MIME-Typ einem Bildformat zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-119">The following entries indicate to the Windows Photo Gallery and Windows Explorer that a file name extension (.ext) and its associated MIME type are associated with an image format.</span></span>

<span data-ttu-id="ef4f5-120">Der folgende Eintrag zeigt Windows und Anwendungen an, die den Inhaltstyp (auch als MIME-Typ bezeichnet) verwenden, dass eine Datei mit einer bestimmten Erweiterung (. ext) ein Bildformat ist.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-120">The following entry indicates to Windows and applications that use content type (also known as mime type) that a file with a given extension (.ext) is an image format.</span></span> <span data-ttu-id="ef4f5-121">Der Dateityp Besitzer muss ein-Element auswählen `<image sub type value>` , das das Dateiformat eindeutig identifiziert, und dieser Inhaltstyp muss bei IANA registriert werden.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-121">The file type owner needs to choose a `<image sub type value>` that uniquely identifies the file format and this content type value needs to be register with IANA.</span></span>

```
HKEY_CLASSES_ROOT
   {.ext}
      ContentType = image/<image sub type>
```

<span data-ttu-id="ef4f5-122">Der folgende Eintrag zeigt Windows, Windows Search und Anwendungen, die [System. Kind](../properties/props-system-kind.md) verwenden, dass eine Dateinamenerweiterung (. ext) als Bild behandelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-122">The following entry indicates to Windows, Windows search and applications that use [System.Kind](../properties/props-system-kind.md) that a file name extension (.ext) should be treated as a picture.</span></span> <span data-ttu-id="ef4f5-123">Dies weist insbesondere darauf hin, dass die System. Kind-Eigenschaft der Dateierweiterung auf "Bild" festgelegt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-123">Specifically, it indicates that the file extension’s System.Kind property should be set to Picture.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  KindMap
                     {.ext} = Picture
```

## <a name="integration-with-the-windows-property-store"></a><span data-ttu-id="ef4f5-124">Integration in den Windows-Eigenschaften Speicher</span><span class="sxs-lookup"><span data-stu-id="ef4f5-124">Integration with the Windows Property Store</span></span>

<span data-ttu-id="ef4f5-125">Manchmal werden dieselben Metadateneigenschaften in verschiedenen Metadatenschemas verfügbar gemacht, häufig mit unterschiedlichen Eigenschaftsnamen.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-125">Sometimes the same metadata properties are exposed in different metadata schemas, often with different property names.</span></span> <span data-ttu-id="ef4f5-126">Wenn eine dieser Eigenschaften aktualisiert wird, die anderen aber nicht, können die Metadaten in der Datei nicht synchronisiert werden. Der Photo-Eigenschaften Handler stellt die Standard Implementierung von **IPropertyStore** für Images bereit und wird von Anwendungen sowie von der Windows-Fotogalerie und Windows-Explorer verwendet, um sicherzustellen, dass alle Metadaten in einem Image synchron bleiben und dass die von den Anwendungen angezeigten Eigenschaften mit den von der Windows-Fotogalerie und Windows-Explorer angezeigten Eigenschaften konsistent sind.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-126">When one of these properties is updated, but the others are not, the metadata within the file can get out of sync. The photo property handler provides the default **IPropertyStore** implementation for images, and is used by applications as well as by the Windows Photo Gallery and Windows Explorer to ensure that all the metadata in an image stays in sync, and that the properties displayed by applications are consistent with those displayed by the Windows Photo Gallery and Windows Explorer.</span></span> <span data-ttu-id="ef4f5-127">Wenn der Photo-Eigenschaften Handler Metadaten aktualisiert, stellt er sicher, dass diese Eigenschaften konsistent über alle gängigen Metadatenformate hinweg aktualisiert werden, die in der Datei vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-127">When the photo property handler updates metadata, it makes sure that these properties are updated consistently across all the common metadata formats that are present in the file.</span></span>

<span data-ttu-id="ef4f5-128">Der Foto Eigenschaften Handler muss das Containerformat verstehen und die verschiedenen darin enthaltenen Eigenschaften finden.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-128">The photo property handler must understand the container format and how to locate the various properties within it.</span></span> <span data-ttu-id="ef4f5-129">Im Allgemeinen ist es nicht möglich, dass der Foto-Eigenschaften Handler weiß, wie die verschiedenen Metadatenblöcke in einem proprietären Containerformat angeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-129">In general, it isn’t possible for the photo property handler to know how the various metadata blocks are laid out in a proprietary container format.</span></span> <span data-ttu-id="ef4f5-130">Wenn die Metadaten im Containerformat aber auf die gleiche Weise wie die Metadaten in einem TIFF-Container-oder JPEG-Containerformat angeordnet sind, kann der Foto Eigenschaften Handler dieses Wissen nutzen, um die Metadaten konsistent in Ihrem Containerformat zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-130">However, if the metadata in your container format is laid out the same way as the metadata in either a TIFF container format or a JPEG container format, the photo property handler can take advantage of that knowledge to update metadata consistently in your container format as well.</span></span>

<span data-ttu-id="ef4f5-131">Sie können diese Zuordnung registrieren, indem Sie den folgenden Registrierungs Eintrag erstellen.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-131">You can register this association by creating the following registry entry.</span></span> <span data-ttu-id="ef4f5-132">Dieser Eintrag benachrichtigt den Photo-Eigenschaften Handler, dass das von dieser GUID identifizierte Containerformat dieselben Metadatenabfrage-sprach Pfade wie das Containerformat mit der GUID 163bcc30e2e9-4s0b-961d-a3e9sdb788a3 versteht.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-132">This entry notifies the photo property handler that the container format identified by this GUID understands the same metadata query language paths as the container format with the GUID 163bcc30-e2e9-4f0b-961d-a3e9fdb788a3.</span></span> <span data-ttu-id="ef4f5-133">(163bcc30e2e9-4f 0B-961d-a3e9f db788a3 ist die GUID für das TIFF-Containerformat.)</span><span class="sxs-lookup"><span data-stu-id="ef4f5-133">(163bcc30-e2e9-4f0b-961d-a3e9fdb788a3 is the GUID for the TIFF container format.)</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PhotoPropertyHandler
                  ContainerAssociations
                     {Container Format GUID} = {163bcc30-e2e9-4f0b-961d-a3e9fdb788a3}
```

<span data-ttu-id="ef4f5-134">Im folgenden Eintrag wird die Standard Implementierung von " **IPropertyStore** " für den Photo-Eigenschaftenhandler mit Dateien mit der Erweiterung ". ext" verknüpft.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-134">The following entry associates the photo property handler’s default implementation of **IPropertyStore** with files that have the extension ".ext".</span></span> <span data-ttu-id="ef4f5-135">Die erste GUID ist die IID der **IPropertyStore** -Schnittstelle, die zweite ist die GUID der Implementierung des Foto-Eigenschafts Handlers.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-135">The first GUID is the IID of the **IPropertyStore** interface, and the second is the GUID of the photo property handler’s implementation of it.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PhotoPropertyHandler
                  {.ext}
                     (Default) = {a38b883c-1682-497e-97b0-0a3a9e801682}
```

<span data-ttu-id="ef4f5-136">Codecs, die ein proprietäres Format verwenden, das nicht mit dem TIFF-oder JPEG-Containerformat kompatibel ist, müssen ihre eigene **IPropertyStore** -Implementierung schreiben.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-136">Codecs that use a proprietary format that is not compatible with either the TIFF or JPEG container format must write their own **IPropertyStore** implementation.</span></span>

## <a name="integration-with-the-windows-photo-gallery"></a><span data-ttu-id="ef4f5-137">Integration in die Windows-Fotogalerie</span><span class="sxs-lookup"><span data-stu-id="ef4f5-137">Integration with the Windows Photo Gallery</span></span>

<span data-ttu-id="ef4f5-138">Die Windows-Fotogalerie basiert auf WIC und kann jedes WIC-fähige Bildformat anzeigen, für das der Codec installiert ist.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-138">Windows Photo Gallery is built on WIC and can display any WIC-enabled image format for which the codec is installed.</span></span> <span data-ttu-id="ef4f5-139">Um das System zu benachrichtigen, dass das Bildformat in der Windows-Fotogalerie geöffnet werden kann, müssen Sie eine Datei Zuordnung erstellen, indem Sie die folgenden Registrierungseinträge erstellen.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-139">To notify the system that your image format can be opened in Windows Photo Gallery, you need to create a file association by creating the following registry entries.</span></span>

```
HKEY_CLASSES_ROOT
   {.ext}
      (Default) = {ProgID} for example, jpegfile)
      OpenWithProgids
         {ProgID}
      OpenWithList
         PhotoViewer.dll
      ShellEx
         ContextMenuHandlers
            ShellImagePreview
               (Default) = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
   SystemFileAssociations
      {.ext}
         OpenWithList
            PhotoViewer.dll
         ShellEx
            ContextMenuHandlers
               ShellImagePreview
                  (Default) = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
   {Image Format ProgID}
      (Default) = Name of Image Format
      DefaultIcon
         (Default) = Path to icon for type, icon index
      shell
         open
            MuiVerb = @%PROGRAMFILES%\Windows Photo Gallery\photoviewer.dll,-3043
            command
               (Default) = %SystemRoot%\System32\rundll32.exe "%ProgramFiles%\Windows Photo Gallery\PhotoViewer.dll", ImageView_Fullscreen %1
            DropTarget
               Clsid = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
         printo
            command
               (Default) = %SystemRoot%\System32\rundll32.exe "%SystemRoot%\System32\shimgvw.dll", ImageView_PrintTo /pt "%1" "%2" "%3" "%4"
```

<span data-ttu-id="ef4f5-140">Die ProgID ist normalerweise die Dateinamenerweiterung, die mit dem Wort "file" angehängt wird.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-140">The ProgID is usually the file name extension appended with the word "file".</span></span> <span data-ttu-id="ef4f5-141">(Wenn die Dateinamenerweiterung beispielsweise ". txt" lautet, wäre die ProgID normalerweise "txtfile".)</span><span class="sxs-lookup"><span data-stu-id="ef4f5-141">(For example, if the file name extension is .txt, the ProgID would usually be "txtfile".)</span></span>

<span data-ttu-id="ef4f5-142">Es gibt weitere Standard Registrierungseinträge, die Sie möglicherweise erstellen müssen, um Dateizuordnungen zu unterstützen. Da "y" nicht spezifisch für WIC ist, gehen Sie jedoch über den Rahmen dieses Themas hinaus.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-142">There are other standard registry entries you may need to create to support file associations; however, because the’y are not specific to WIC, they are beyond the scope of this topic.</span></span>

## <a name="integration-with-the-windows-thumbnail-cache"></a><span data-ttu-id="ef4f5-143">Integration in den Windows-Miniatur Ansichts Cache</span><span class="sxs-lookup"><span data-stu-id="ef4f5-143">Integration with the Windows Thumbnail Cache</span></span>

<span data-ttu-id="ef4f5-144">Die folgenden beiden Einträge geben an, dass die Standard Implementierung des WIC-Miniatur Ansichts Anbieters verwendet werden kann, um Miniaturansichten für Dateien mit dieser Erweiterung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-144">The following two entries indicate that the standard WIC thumbnail provider implementation can be used to retrieve thumbnails for files with this extension.</span></span> <span data-ttu-id="ef4f5-145">Die erste GUID ist die IID der [IThumbnailProvider](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) -Schnittstelle, die zweite ist die GUID der Standardsystem Implementierung dieser Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-145">The first GUID is the IID of the [IThumbnailProvider](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) interface, and the second is the GUID of the standard system implementation of this interface.</span></span> <span data-ttu-id="ef4f5-146">(Alle Einträge unter HLCR \\ . ext \\ shellex \\ werden unter HKCR \\ systemfileassociations \\ . ext \\ shellex wiederholt \\ .)</span><span class="sxs-lookup"><span data-stu-id="ef4f5-146">(All entries under HLCR\\.ext\\ShellEx\\ are repeated under HKCR\\SystemFileAssociations\\.ext\\ShellEx\\.)</span></span>

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      {.ext}
         ShellEx
            {e357fccd-a995-4576-b01f-234630154e96}
               (Default) = {C7657C4A-9F68-40fa-A4DF-96BC08EB3551}
```

## <a name="related-topics"></a><span data-ttu-id="ef4f5-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ef4f5-147">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ef4f5-148">**Licher**</span><span class="sxs-lookup"><span data-stu-id="ef4f5-148">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ef4f5-149">Codierungs spezifische Registrierungseinträge</span><span class="sxs-lookup"><span data-stu-id="ef4f5-149">Encoder-Specific Registry Entries</span></span>](-wic-decoderregentries.md)
</dt> <dt>

[<span data-ttu-id="ef4f5-150">Codec-Installation und-Registrierung</span><span class="sxs-lookup"><span data-stu-id="ef4f5-150">CODEC Installation and Registration</span></span>](-wic-codecinstallandreg.md)
</dt> <dt>

[<span data-ttu-id="ef4f5-151">Schreiben eines WIC-Enabled Codecs</span><span class="sxs-lookup"><span data-stu-id="ef4f5-151">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="ef4f5-152">Übersicht über die Windows Imaging-Komponente</span><span class="sxs-lookup"><span data-stu-id="ef4f5-152">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
