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
# <a name="integration-with-windows-photo-gallery-and-windows-explorer"></a>Integration in Windows Photo Gallery und Windows-Explorer

Dieses Thema gilt für Windows Vista und höher. Sie enthält die folgenden Abschnitte:

-   [Introduction (Einführung)](#introduction)
-   [Integration in den Windows-Eigenschaften Speicher](#integration-with-the-windows-property-store)
-   [Integration in die Windows-Fotogalerie](#integration-with-the-windows-photo-gallery)
-   [Integration in den Windows-Miniatur Ansichts Cache](#integration-with-the-windows-thumbnail-cache)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction"></a>Einführung

Um die Windows-Fotogalerie und Windows-Explorer zum Anzeigen von Miniaturansichten und zum Suchen und Aktualisieren von Standardbild Metadaten zu aktivieren, muss einem Codec eine Implementierung der [IThumbnailProvider](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) -und [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Schnittstellen zugeordnet werden. Die IThumbnailProvider-Schnittstelle wird verwendet, um Miniaturansichten abzurufen und den Miniatur Ansichts Cache aufzufüllen, und die IPropertyStore-Schnittstelle wird zum Suchen und Aktualisieren von Metadaten verwendet, die einer Datei zugeordnet sind. Ab Windows Vista verfügen alle Dateitypen über Miniaturansichten und Metadaten, aber für unterschiedliche Dateitypen sind unterschiedliche Implementierungen dieser Schnittstellen erforderlich, um die Miniaturansichten und Metadaten abzurufen oder zu generieren. Das System stellt Standard Implementierungen dieser Schnittstellen bereit. Die Standard Implementierung von IThumbnailProvider kann für alle Windows Imaging Component (WIC) – aktivierte Bildformate verwendet werden. Die Standard Implementierung von IPropertyStore kann mit jedem WIC-fähigen Bildformat verwendet werden, das auf einem Tagged Image File Format (TIFF)-oder JPEG-Container basiert. Um das Bildformat den Standard Implementierungen dieser beiden Schnittstellen zuzuordnen, müssen Sie nur wenige Registrierungseinträge hinzufügen.

In den folgenden Einträgen wird die Windows-Fotogalerie und der Windows-Explorer angezeigt, dass die Dateinamenerweiterung (. ext) und der zugehörige MIME-Typ einem Bildformat zugeordnet sind.

Der folgende Eintrag zeigt Windows und Anwendungen an, die den Inhaltstyp (auch als MIME-Typ bezeichnet) verwenden, dass eine Datei mit einer bestimmten Erweiterung (. ext) ein Bildformat ist. Der Dateityp Besitzer muss ein-Element auswählen `<image sub type value>` , das das Dateiformat eindeutig identifiziert, und dieser Inhaltstyp muss bei IANA registriert werden.

```
HKEY_CLASSES_ROOT
   {.ext}
      ContentType = image/<image sub type>
```

Der folgende Eintrag zeigt Windows, Windows Search und Anwendungen, die [System. Kind](../properties/props-system-kind.md) verwenden, dass eine Dateinamenerweiterung (. ext) als Bild behandelt werden soll. Dies weist insbesondere darauf hin, dass die System. Kind-Eigenschaft der Dateierweiterung auf "Bild" festgelegt werden sollte.

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

## <a name="integration-with-the-windows-property-store"></a>Integration in den Windows-Eigenschaften Speicher

Manchmal werden dieselben Metadateneigenschaften in verschiedenen Metadatenschemas verfügbar gemacht, häufig mit unterschiedlichen Eigenschaftsnamen. Wenn eine dieser Eigenschaften aktualisiert wird, die anderen aber nicht, können die Metadaten in der Datei nicht synchronisiert werden. Der Photo-Eigenschaften Handler stellt die Standard Implementierung von **IPropertyStore** für Images bereit und wird von Anwendungen sowie von der Windows-Fotogalerie und Windows-Explorer verwendet, um sicherzustellen, dass alle Metadaten in einem Image synchron bleiben und dass die von den Anwendungen angezeigten Eigenschaften mit den von der Windows-Fotogalerie und Windows-Explorer angezeigten Eigenschaften konsistent sind. Wenn der Photo-Eigenschaften Handler Metadaten aktualisiert, stellt er sicher, dass diese Eigenschaften konsistent über alle gängigen Metadatenformate hinweg aktualisiert werden, die in der Datei vorhanden sind.

Der Foto Eigenschaften Handler muss das Containerformat verstehen und die verschiedenen darin enthaltenen Eigenschaften finden. Im Allgemeinen ist es nicht möglich, dass der Foto-Eigenschaften Handler weiß, wie die verschiedenen Metadatenblöcke in einem proprietären Containerformat angeordnet werden. Wenn die Metadaten im Containerformat aber auf die gleiche Weise wie die Metadaten in einem TIFF-Container-oder JPEG-Containerformat angeordnet sind, kann der Foto Eigenschaften Handler dieses Wissen nutzen, um die Metadaten konsistent in Ihrem Containerformat zu aktualisieren.

Sie können diese Zuordnung registrieren, indem Sie den folgenden Registrierungs Eintrag erstellen. Dieser Eintrag benachrichtigt den Photo-Eigenschaften Handler, dass das von dieser GUID identifizierte Containerformat dieselben Metadatenabfrage-sprach Pfade wie das Containerformat mit der GUID 163bcc30e2e9-4s0b-961d-a3e9sdb788a3 versteht. (163bcc30e2e9-4f 0B-961d-a3e9f db788a3 ist die GUID für das TIFF-Containerformat.)

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

Im folgenden Eintrag wird die Standard Implementierung von " **IPropertyStore** " für den Photo-Eigenschaftenhandler mit Dateien mit der Erweiterung ". ext" verknüpft. Die erste GUID ist die IID der **IPropertyStore** -Schnittstelle, die zweite ist die GUID der Implementierung des Foto-Eigenschafts Handlers.

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

Codecs, die ein proprietäres Format verwenden, das nicht mit dem TIFF-oder JPEG-Containerformat kompatibel ist, müssen ihre eigene **IPropertyStore** -Implementierung schreiben.

## <a name="integration-with-the-windows-photo-gallery"></a>Integration in die Windows-Fotogalerie

Die Windows-Fotogalerie basiert auf WIC und kann jedes WIC-fähige Bildformat anzeigen, für das der Codec installiert ist. Um das System zu benachrichtigen, dass das Bildformat in der Windows-Fotogalerie geöffnet werden kann, müssen Sie eine Datei Zuordnung erstellen, indem Sie die folgenden Registrierungseinträge erstellen.

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

Die ProgID ist normalerweise die Dateinamenerweiterung, die mit dem Wort "file" angehängt wird. (Wenn die Dateinamenerweiterung beispielsweise ". txt" lautet, wäre die ProgID normalerweise "txtfile".)

Es gibt weitere Standard Registrierungseinträge, die Sie möglicherweise erstellen müssen, um Dateizuordnungen zu unterstützen. Da "y" nicht spezifisch für WIC ist, gehen Sie jedoch über den Rahmen dieses Themas hinaus.

## <a name="integration-with-the-windows-thumbnail-cache"></a>Integration in den Windows-Miniatur Ansichts Cache

Die folgenden beiden Einträge geben an, dass die Standard Implementierung des WIC-Miniatur Ansichts Anbieters verwendet werden kann, um Miniaturansichten für Dateien mit dieser Erweiterung abzurufen. Die erste GUID ist die IID der [IThumbnailProvider](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) -Schnittstelle, die zweite ist die GUID der Standardsystem Implementierung dieser Schnittstelle. (Alle Einträge unter HLCR \\ . ext \\ shellex \\ werden unter HKCR \\ systemfileassociations \\ . ext \\ shellex wiederholt \\ .)

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      {.ext}
         ShellEx
            {e357fccd-a995-4576-b01f-234630154e96}
               (Default) = {C7657C4A-9F68-40fa-A4DF-96BC08EB3551}
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Codierungs spezifische Registrierungseinträge](-wic-decoderregentries.md)
</dt> <dt>

[Codec-Installation und-Registrierung](-wic-codecinstallandreg.md)
</dt> <dt>

[Schreiben eines WIC-Enabled Codecs](-wic-howtowriteacodec.md)
</dt> <dt>

[Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
