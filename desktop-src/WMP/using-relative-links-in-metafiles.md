---
title: Verwenden relativer Verknüpfungen in Metadateien
description: Verwenden relativer Verknüpfungen in Metadateien
ms.assetid: 8f6c40fc-e025-43d5-a43a-c162f28bbd71
keywords:
- Windows Media Metadatei-Wiedergabelisten, relative Links
- Wiedergabelisten, relative Links
- Metadatei-Wiedergabelisten, relative Links
- Metadatendateien, relative Links
- Windows Media-Metadateien, relative Links
- Relative Links
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9f9fe000ec071b0e54b9c6699a8a560ee4a26051
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855843"
---
# <a name="using-relative-links-in-metafiles"></a>Verwenden relativer Verknüpfungen in Metadateien

Relative Links sind eine vollständig unterstützte Funktion von Windows Media-Metadatendateien. Sie können relative Links in Metadateien verwenden, ähnlich wie Sie in HTML-Dokumenten verwendet werden. Durch die Verwendung relativer Verknüpfungen können Sie Metadateien erstellen, die portabel sind, d. h., Sie können eine gesamte Verzeichnisstruktur auf einen anderen Server kopieren oder verschieben, ohne die Pfade zu Grafikdateien zu aktualisieren, die als Banner oder die **href** -Attribute der **moreinfo** -Elemente verwendet werden (wenn Sie auf Dateien auf demselben Webserver wie die gespeicherte Metadatendatei verweisen). Relative Verknüpfungen funktionieren in jeder Anwendung, die Sie unterstützt, da die Teile der URL, die nicht im **href** -Attribut eines Elements enthalten sind, in der URL enthalten sind, die von der Anwendung an den Server gesendet wird, wenn diese URL angefordert wird. Dies bedeutet, dass das Protokoll (z. b. https://), der Servername und das virtuelle Verzeichnis, in dem sich die Datei befindet, die den relativen Link enthält, alle in der URL enthalten sind, die an den Server gesendet wird. Wenn sich die Mediendatei oder URL, die Sie mit einem relativen Link verknüpfen, nicht auf demselben Server wie die Metadatendatei befindet, ist der relative Link ungültig.

> [!Note]  
> Diese Informationen über relative Links sind nur dann korrekt, wenn Sie einen Link zu Metadateien verwenden, die im eigenständigen Windows-Media Player geöffnet sind. Wenn Sie das eingebettete Windows Media Player-Steuerelement verwenden, sind alle Verknüpfungen relativ zu der Seite, auf der das-Steuerelement gehostet wird, es sei denn, das untergeordnete **Basis** Element des **-Elements wird** verwendet, um den relativen Pfad umzuleiten.

 

Alle relativen Verknüpfungen in der Metadatei müssen für Streamingmedien vollständig relativ und nicht als Laufwerks bezogen sein. Wenn eine URL mit einem " \\ "-Zeichen beginnt, ist der Link "Drive-relative". Windows Media Player versucht, die Datei zu öffnen, mit der auf dem Laufwerk, auf dem die Metadatendatei geöffnet wurde, und in der Regel ein Webserver geöffnet wurde. Da Webserver virtuelle Verzeichnisse verwenden, versucht Windows Media Player, den angegebenen Stream oder die angegebene Mediendatei in einem Unterverzeichnis eines virtuellen Verzeichnisses auf dem Webserver zu finden, von dem aus die Metadatendatei geöffnet wurde. Ein Benutzer hat keinen Zugriff auf ein Serververzeichnis. Das Beispiel in diesem Abschnitt veranschaulicht die Verwendung eines vollständig relativen Links.

Sie können auf einem einzelnen Computer, auf dem sich alle Mediendateien, mit denen in der Metadatei-Wiedergabeliste verknüpft ist, auf einem Speichergerät auf dem Computer verwenden. Medien können jedoch nicht auf diese Weise gestreamt werden.

Wenn Sie einen Link zu einer anderen Metadatei verwenden, um relative Verknüpfungen zuzulassen, ist der Name, der als Titel von Windows Media Player angezeigt wird, der Titel in der ursprünglichen Metadatendatei.

Relative Links können nicht für URLs zu einem Streaming Media-Server verwendet werden, da für den Zugriff auf Streamingmedieninhalte unterschiedliche Protokolle verwendet werden.

In der folgenden Beispiel Wiedergabeliste enthält der erste **ENTRYREF** eine URL für eine andere Wiedergabeliste (relative. Wax).


```XML
<ASX>
    <ENTRYREF HREF="https://example.microsoft.com/metafiles/relative.wax"/>
</ASX>

```



Das folgende Beispiel zeigt die Datei relative. Wax, die relative Links enthält.


```XML
<ASX version = "3.0">
    <BANNER HREF = "graphics/logo1.jpg">
        <MOREINFO HREF = "category1/category1.htm" />
    </BANNER>
    <ENTRY>
        <REF HREF = "mms://samples.microsoft.com/myfile.wma" />
    </ENTRY>
</ASX>

```



Die URL, die den Verweis auf die Wiedergabeliste (relative. Wax) enthält, kann in einer Metadatei-Wiedergabeliste vorhanden sein, auf die der Benutzer zugreifen kann. Damit die URL erfolgreich verarbeitet werden kann, muss ein Webserver mit dem Namen "example.Microsoft.com" vorhanden sein. Dieser Webserver muss über ein virtuelles Verzeichnis verfügen, das als "Metafiles" definiert ist. Die referenzierte Wiedergabeliste (relative. Wax) muss auf dem Webserver mit dem Namen "example.Microsoft.com" im virtuellen Verzeichnis "Metafiles" vorhanden sein.

Damit auf die Mediendateien, auf die verwiesen wird, in der Wiedergabeliste relative. Wax erfolgreich zugreifen und wiedergegeben wird, muss ein Verzeichnis mit dem Namen "graphics" vorhanden sein, bei dem es sich um ein Unterverzeichnis des virtuellen Verzeichnisses "Metafiles" des Servers handelt. Die Grafikdatei Logo1.jpg, auf die im **Banner** Element verwiesen wird, muss das Unterverzeichnis mit dem Namen Grafiken sein.

Ähnlich muss sich ein Dokument mit dem Namen Category1.htm in einem Unterverzeichnis mit dem Namen Category1 befinden. Das Verzeichnis mit dem Namen Category1 muss als Unterverzeichnis des virtuellen Verzeichnisses "Metafiles" auf dem Webserver example.Microsoft.com vorhanden sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen von Metafile-Wiedergabelisten**](creating-metafile-playlists.md)
</dt> <dt>

[**Metafile-Wiedergabelisten**](metafile-playlists.md)
</dt> <dt>

[**Verweis auf Windows Media-Metadateielemente**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Leitfaden für Windows Media-Metadateien**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




