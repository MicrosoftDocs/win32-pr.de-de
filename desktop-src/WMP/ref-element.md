---
title: REF-Element
description: Das REF-Element gibt eine URL für digitale Medieninhalte an.
ms.assetid: 0ba11a1e-3802-4156-83ca-f1bae1eb366c
keywords:
- REF-Element Windows Media Player
topic_type:
- apiref
api_name:
- REF Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9195eb1fc3ca1f13e64376c0200cbb2e6ec4589e6740a74b1ff7670c0951df25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118333277"
---
# <a name="ref-element"></a>REF-Element

Das **REF-Element** gibt eine URL für digitale Medieninhalte an.

``` syntax
<REF
   HREF = "URL"
>
</REF>
```

## <a name="attributes"></a>Attribute

**HREF** (erforderlich)

URL zu allen Medieninhalten, die von Windows Media Player unterstützt werden.

## <a name="parentchild-elements"></a>Übergeordnete/untergeordnete Elemente



| Hierarchy       | Elemente                                                                         |
|-----------------|----------------------------------------------------------------------------------|
| Übergeordnete Elemente | **Eintrag**                                                                        |
| Untergeordnete Elemente  | **DURATION,** **ENDMARKER,** **PREVIEWDURATION,** **STARTMARKER,** **STARTTIME** |



 

## <a name="remarks"></a>Hinweise

Dieses Element gibt eine URL für einen Medieninhalt an. Die URL kann auf einen beliebigen unterstützten Medientyp verweisen, indem sie ein beliebiges Protokoll verwendet, das von Windows Media Player unterstützt wird.

Zu den unterstützten Medientypen gehören Standbilder wie .gif und .jpg Bilder und Flashdateien mit der Dateinamenerweiterung .swf. Diese Medientypen eignen sich zum Einschließen von Werbeinhalten in eine Wiedergabeliste. Bei Bilddateien und Flashdateien, die in einer Schleife wiedergegeben werden, müssen Sie auch die Zeitspanne zum Anzeigen des Medienelements angeben, indem Sie ein **DURATION-Element** in das **REF-Element** einschließen. Wenn ein Bild weiterhin angezeigt werden soll, während der nächste Eintrag in der Wiedergabeliste gepuffert wird, fügen Sie ein **PARAM-Element** in das **ENTRY-Element** ein, legen Sie das **Name-Attribut** auf ShowWhileBuffering fest, und legen Sie dessen **Wertattribut** auf TRUE fest.

Um auf Inhalte auf einer CD oder dvd zu verweisen, die dies zulässt, werden die Protokolle wmpcd und wmpdvd bereitgestellt. Wenn Sie z. B. das **HREF-Attribut** auf "wmpdvd://f/5/3" festlegen, wird Kapitel 3 von Titel 5 auf einer DVD wiedergegeben, aber nur, wenn die DVD erstellt wurde, um sie zuzulassen.

Anwendungen, die digitale Medien hinter einer Firewall öffnen, erzielen eine bessere Leistung beim Öffnen der Medienelemente, wenn die Adresse mit dem DNS-Namen (Domain Name Server) anstelle der IP-Adresse angegeben wird.

Dieses Element wird am häufigsten für URL-Rollover verwendet. Wenn Windows Media Player ein mediendefiniertes Element in einem **REF-Element** nicht öffnen kann, wird die URL im nächsten **REF-Element** versucht. Sobald Windows Media Player Medieninhalte aus einer URL öffnet, die innerhalb des Bereichs eines **ENTRY-Elements** definiert ist, werden nachfolgende **REF-Tags** in diesem **ENTRY-Element** ignoriert. Nachdem die Wiedergabe des Inhalts abgeschlossen ist, wird Windows Media Player ggf. mit dem nächsten **ENTRY-Element** fortgeschaltet.

-   **Wichtig** Sobald Windows Media Player eine Verbindung mit einem Referenzinhalt herstellt, ignoriert er alle anderen **REF-Elemente** in **diesem ENTRY,** unabhängig davon, ob die Verbindung normal oder ungewöhnlich beendet wird.

Wenn es sich bei dem Medienelement, auf das verwiesen wird, um eine Bilddatei handelt, muss das **DURATION-Element** verwendet werden, um die Anzeigezeit für das Bild anzugeben.

**Hinweis**

Der Versuch, Flashmedien wiederzugeben, die Sound mit dem ersten Frame enthalten, kann zu unerwarteten Ergebnissen führen. Sie sollten Flash-Inhalte erstellen, um Sound ab dem zweiten Frame wiederzuspielen.

## <a name="examples"></a>Beispiele


```XML
<ASX VERSION="3.0">
   <ENTRY>
   <TITLE>Example Clip</TITLE>
      <REF HREF="mms://example.microsoft.com/selection1.asf" />
      <REF HREF="mms://sample.microsoft.com/mirror/selection1.asf" />
   </ENTRY>
</ASX>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Unterstützte Protokolle und Dateitypen**](supported-protocols-and-file-types.md)
</dt> <dt>

[**Windows Referenz zu Medienmetadateielementen**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Referenz zu Medienmetadateien**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





