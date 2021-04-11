---
title: Abrufen von Metadaten
description: Abrufen von Metadaten
ms.assetid: f634118a-0a62-4407-8be1-a907347de55b
keywords:
- Windows Media Metadatei-Wiedergabelisten, Abrufen von Metadaten
- Wiedergabelisten, Abrufen von Metadaten
- Metadatei-Wiedergabelisten, Abrufen von Metadaten
- Windows Media Metadatei-Wiedergabelisten, Abrufen von Metadaten
- Wiedergabelisten, Abrufen von Metadaten
- Metadatei-Wiedergabelisten, Abrufen von Metadaten
- Metadaten, Abrufen
- Abrufen von Metadaten
- Windows Media Player, Abrufen von Metadaten
- Windows Media Player, Abrufen von Metadaten
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3c9855ec1dc95a52429561e91aa82abdac088523
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947856"
---
# <a name="retrieving-metadata"></a>Abrufen von Metadaten

Während ein Show-oder Clip-Vorgang abgespielt wird, kann das Skript Metadaten wie Titel und Autor mithilfe der **getiteminfo** -Methoden der Windows-Media Player **Medien** -und **Wiedergabe** Listen Objekte abrufen. Sie können Metadaten aus dem Bereich "ASX" mithilfe von **Wiedergabe** Listen-Objektmethoden und aus dem Eintrags Bereich mithilfe von **Medien** Objektmethoden abrufen.

Wenn Sie z. b. die Werte für "Author", "abstract" und "param" in der folgenden Datei abrufen möchten, verwenden Sie die **getiteminfo** -Methode des **Wiedergabe** Listen Objekts. Der Attribut Name ist für diese Methode erforderlich. Attributnamen können abgerufen werden, indem die Indexnummer der **attributeName** -Eigenschaft bereitgestellt wird. Die verfügbaren Indizes für ein **Wiedergabe** Listen Objekt können mithilfe der **AttributeCount** -Eigenschaft abgerufen werden.

## <a name="example-code"></a>Beispielcode


```XML

    <ASX version="3.0">
        <AUTHOR>My Talking File</AUTHOR>
        <ABSTRACT>Talking File Album</ABSTRACT>
        <PARAM name="one" value="111"/>
        <ENTRY>
            <REF href="Artists_Only.wma"/>
            <TITLE>Artists Only</TITLE>
            <COPYRIGHT>2000</COPYRIGHT>
            <PARAM name="three" value="333"/>
        </ENTRY>
        <PARAM name="two" value="222"/>
    </ASX>
    

```



Um die Werte des aktuellen **Medien** Objekts im Einstiegsbereich für Ref, Title, Copyright und param ("Three") abzurufen, verwenden Sie die **currentMedia** -Eigenschaft des **Player** -Objekts. Verwenden Sie die **AttributeCount** -Eigenschaft des **Media** -Objekts, um die Anzahl der für das angegebene **Medien** Objekt verfügbaren Attribute zu ermitteln. Verwenden Sie Indexnummern mit der **getiteminfobyatom** -Methode, um Attributwerte abzurufen. Verwenden Sie Indexnummern mit der **GetAttributeName** -Methode des **Media** -Objekts, um die Namen der verfügbaren Attribute zu bestimmen, und verwenden Sie dann die Ergebnisse mit der **getiteminfo** -Methode.

Ein Beispiel für die Verwendung von Windows Media Player-Objektmethoden zum Abrufen von Metadaten finden Sie unter [Wiedergabeliste. AttributeCount](playlist-attributecount.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen von Metafile-Wiedergabelisten**](creating-metafile-playlists.md)
</dt> <dt>

[**Metafile-Wiedergabelisten**](metafile-playlists.md)
</dt> <dt>

[**Leitfaden für Windows Media-Metadateien**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




