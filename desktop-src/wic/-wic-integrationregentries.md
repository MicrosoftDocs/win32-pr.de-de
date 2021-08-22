---
description: Dieses Thema gilt für Windows Vista und höher.
ms.assetid: 4d88806a-68a6-4394-a704-c7a47a0fdc70
title: Integration in Windows Fotogalerie und Windows Explorer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e20b690e2640fb40830721f1c6a3211641d81311724be2c70efae3781171e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119549440"
---
# <a name="integration-with-windows-photo-gallery-and-windows-explorer"></a>Integration in Windows Fotogalerie und Windows Explorer

Dieses Thema gilt für Windows Vista und höher. Sie enthält die folgenden Abschnitte:

-   [Introduction (Einführung)](#introduction)
-   [Integration in Windows Property Store](#integration-with-the-windows-property-store)
-   [Integration in die Windows Fotogalerie](#integration-with-the-windows-photo-gallery)
-   [Integration in den Windows Thumbnail Cache](#integration-with-the-windows-thumbnail-cache)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction"></a>Einführung

Damit Windows Fotogalerie und Windows Explorer Miniaturansichten anzeigen und Standardbildmetadaten suchen und aktualisieren können, muss einem Codec eine Implementierung der Schnittstellen [IThumbnailProvider](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) und [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) zugeordnet sein. Die IThumbnailProvider-Schnittstelle wird verwendet, um Miniaturansichten abzurufen und den Miniaturansichtscache aufzufüllen, und die IPropertyStore-Schnittstelle wird zum Suchen und Aktualisieren von Metadaten verwendet, die einer Datei zugeordnet sind. Ab Windows Vista verfügen alle Dateitypen über Miniaturansichten und Metadaten, aber unterschiedliche Dateitypen erfordern unterschiedliche Implementierungen dieser Schnittstellen, um die Miniaturansichten und Metadaten für sie abzurufen oder zu generieren. Das System stellt Standardimplementierungen dieser Schnittstellen bereit. Die Standardimplementierungen von IThumbnailProvider können für jedes WIC-fähige Bildformat (Windows Imaging Component) verwendet werden. Die Standardimplementierungen von IPropertyStore können mit jedem WIC-fähigen Bildformat verwendet werden, das auf einem Tagged Image File Format -Container (TIFF) oder JPEG-Container basiert. Um Ihr Imageformat den Standardimplementierungen beider Schnittstellen zuzuordnen, müssen Sie nur einige Registrierungseinträge hinzufügen.

Die folgenden Einträge geben dem Windows Fotogalerie und Windows Explorer an, dass eine Dateinamenerweiterung (.ext) und der zugehörige MIME-Typ einem Bildformat zugeordnet sind.

Der folgende Eintrag gibt Windows und Anwendungen, die den Inhaltstyp (auch als MIME-Typ bezeichnet) verwenden, an, dass eine Datei mit einer angegebenen Erweiterung (.ext) ein Bildformat ist. Der Dateitypbesitzer muss eine `<image sub type value>` auswählen, die das Dateiformat eindeutig identifiziert, und dieser Wert des Inhaltstyps muss bei IANA registriert werden.

```
HKEY_CLASSES_ROOT
   {.ext}
      ContentType = image/<image sub type>
```

Der folgende Eintrag gibt Windows, Windows Such- und Anwendungen, die [System.Kind](../properties/props-system-kind.md) verwenden, an, dass eine Dateinamenerweiterung (.ext) als Bild behandelt werden soll. Insbesondere wird angegeben, dass die System.Kind-Eigenschaft der Dateierweiterung auf Picture festgelegt werden soll.

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

## <a name="integration-with-the-windows-property-store"></a>Integration in die Windows Property Store

Manchmal werden die gleichen Metadateneigenschaften in unterschiedlichen Metadatenschemas verfügbar gemacht, häufig mit unterschiedlichen Eigenschaftennamen. Wenn eine dieser Eigenschaften aktualisiert wird, die anderen jedoch nicht, können die Metadaten in der Datei nicht mehr synchronisiert werden. Der Fotoeigenschaftenhandler stellt die **IPropertyStore-Standardimplementierungen** für Bilder bereit und wird von Anwendungen sowie vom Windows Fotogalerie und Windows-Explorer verwendet, um sicherzustellen, dass alle Metadaten in einem Bild synchron bleiben und dass die von Anwendungen angezeigten Eigenschaften mit denen übereinstimmen, die vom Windows Fotogalerie und Windows Explorer angezeigt werden. Wenn der Fotoeigenschaftshandler Metadaten aktualisiert, wird sichergestellt, dass diese Eigenschaften konsistent in allen gängigen Metadatenformaten aktualisiert werden, die in der Datei vorhanden sind.

Der Fotoeigenschaftenhandler muss das Containerformat verstehen und die verschiedenen Darin enthaltenen Eigenschaften finden. Im Allgemeinen kann der Fotoeigenschaftshandler nicht wissen, wie die verschiedenen Metadatenblöcke in einem proprietären Containerformat angeordnet sind. Wenn die Metadaten in Ihrem Containerformat jedoch auf die gleiche Weise wie die Metadaten in einem TIFF-Containerformat oder einem JPEG-Containerformat angeordnet sind, kann der Fotoeigenschaftshandler dieses Wissen nutzen, um Metadaten auch konsistent in Ihrem Containerformat zu aktualisieren.

Sie können diese Zuordnung registrieren, indem Sie den folgenden Registrierungseintrag erstellen. Dieser Eintrag benachrichtigt den Fotoeigenschaftenhandler, dass das von dieser GUID identifizierte Containerformat die gleichen Metadatenabfragesprachpfade wie das Containerformat mit der GUID 163bcc30-e2e9-4f0b-961d-a3e9fdb788a3 versteht. (163bcc30-e2e9-4f0b-961d-a3e9fdb788a3 ist die GUID für das TIFF-Containerformat.)

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

Der folgende Eintrag ordnet die Standardimplementierung von **IPropertyStore** des Fotoeigenschaftshandlers Dateien mit der Erweiterung ".ext" zu. Die erste GUID ist die IID der **IPropertyStore-Schnittstelle,** und die zweite ist die GUID der Implementierung des Fotoeigenschaftenhandlers.

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

Codecs, die ein proprietäres Format verwenden, das nicht mit dem TIFF- oder JPEG-Containerformat kompatibel ist, müssen ihre eigene **IPropertyStore-Implementierung** schreiben.

## <a name="integration-with-the-windows-photo-gallery"></a>Integration in die Windows Fotogalerie

Windows Fotogalerie basiert auf WIC und kann jedes WIC-fähige Bildformat anzeigen, für das der Codec installiert ist. Um das System zu benachrichtigen, dass Ihr Imageformat in Windows Fotogalerie geöffnet werden kann, müssen Sie eine Dateizuordnung erstellen, indem Sie die folgenden Registrierungseinträge erstellen.

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

Die ProgID ist in der Regel die Dateinamenerweiterung, die mit dem Wort "file" angefügt wird. (Wenn die Dateinamenerweiterung beispielsweise .txt ist, lautet die ProgID in der Regel "txtfile".)

Es gibt weitere Standardregistrierungseinträge, die Sie möglicherweise erstellen müssen, um Dateizuordnungen zu unterstützen. da die "y" jedoch nicht spezifisch für WIC sind, gehen sie über den Rahmen dieses Themas hinaus.

## <a name="integration-with-the-windows-thumbnail-cache"></a>Integration in den Windows Thumbnail Cache

Die folgenden beiden Einträge geben an, dass die Standardimplementierungen des WIC-Miniaturansichtsanbieters verwendet werden können, um Miniaturansichten für Dateien mit dieser Erweiterung abzurufen. Die erste GUID ist die IID der [IThumbnailProvider-Schnittstelle,](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) und die zweite ist die GUID der Standardsystemimplementierung dieser Schnittstelle. (Alle Einträge unter HLCR \\ .ext \\ ShellEx \\ werden unter HKCR \\ SystemFileAssociations \\ .ext \\ ShellEx \\ wiederholt.)

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

**Konzeptionellen**
</dt> <dt>

[Encoderspezifische Registrierungseinträge](-wic-decoderregentries.md)
</dt> <dt>

[CODEC-Installation und -Registrierung](-wic-codecinstallandreg.md)
</dt> <dt>

[Schreiben eines WIC-Enabled CODEC](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Übersicht über Bildverarbeitungskomponenten](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
