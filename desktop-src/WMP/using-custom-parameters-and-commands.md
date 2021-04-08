---
title: Verwenden von benutzerdefinierten Parametern und Befehlen
description: Verwenden von benutzerdefinierten Parametern und Befehlen
ms.assetid: 6b0bfd19-1672-41e3-9b7f-c8d541168c0e
keywords:
- Windows Media Metadatei-Wiedergabelisten, benutzerdefinierte Parameter
- Wiedergabelisten, benutzerdefinierte Parameter
- Metadatei-Wiedergabelisten, benutzerdefinierte Parameter
- Windows Media Metadatei-Wiedergabelisten, benutzerdefinierte Befehle
- Wiedergabelisten, benutzerdefinierte Befehle
- Metadatei-Wiedergabelisten, benutzerdefinierte Befehle
- Windows Media Metadatei-Wiedergabelisten, Parameter
- Wiedergabelisten, Parameter
- Metadatei-Wiedergabelisten, Parameter
- benutzerdefinierte Parameter
- Benutzerdefinierte Befehle
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 59f577fa4f3af71799b163389f85987d8723e045
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856327"
---
# <a name="using-custom-parameters-and-commands"></a>Verwenden von benutzerdefinierten Parametern und Befehlen

Mithilfe des **param** -Elements können Sie benutzerdefinierte Parameter erstellen, um zusätzliche Metadaten in einer Metadatei-Wiedergabeliste zu übergeben. Verwenden Sie das **Name** -Attribut des **param** -Elements, um den Namen des benutzerdefinierten Parameters zu definieren. Verwenden Sie das **value** -Attribut, um den Wert für den benannten benutzerdefinierten Parameter zu definieren.

Rufen Sie **param** -Metadaten mithilfe der **getiteminfo** -Methoden der **Medien** -und **Wiedergabe** Listen Objekte ab. Ein Beispiel für die Verwendung dieser Methoden zum Abrufen von Metadaten finden Sie unter der [AttributeCount](playlist-attributecount.md) -Methode des **Wiedergabe** Listen Objekts.

Die folgende Beispiel-Metadatei-Wiedergabeliste zeigt die Verwendung des **param** -Elements, um benutzerdefinierte Parameter zu definieren.


```XML
<ASX version="3.0" BANNERBAR="auto" >
    <TITLE>Example Media Player Show</TITLE>
    <PARAM NAME="Director" VALUE="Jane D." />

    <ENTRY>
        <TITLE>Example Clip</TITLE>
        <REF HREF="https://www.proseware.com/media.wma" />
        <PARAM NAME="Title" VALUE="Example Clip" />
        <PARAM NAME="Location" VALUE="North America" />
        <PARAM NAME="Release Date" VALUE="March 1998" />
    </ENTRY>

    <ENTRY>
        <TITLE>Another Clip</TITLE>
        <REF HREF="https://www.proseware.com/more_media.wma" />
        <PARAM NAME="Title" VALUE="Another Clip" />
        <PARAM NAME="Location" VALUE="Japan" />
        <PARAM NAME="Release Date" VALUE="December 2000" />
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden von Metafile-Wiedergabelisten**](using-metafile-playlists.md)
</dt> </dl>

 

 




