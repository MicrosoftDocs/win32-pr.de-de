---
title: Ref-Element
description: Das ref-Element gibt eine URL für den Inhalt digitaler Medien an.
ms.assetid: 0ba11a1e-3802-4156-83ca-f1bae1eb366c
keywords:
- Windows Media Player Ref-Element
topic_type:
- apiref
api_name:
- REF Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 739ac61007e619055c28732c5c5aa763e84054fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368397"
---
# <a name="ref-element"></a>Ref-Element

Das **ref** -Element gibt eine URL für den Inhalt digitaler Medien an.

``` syntax
<REF
   HREF = "URL"
>
</REF>
```

## <a name="attributes"></a>Attribute

**Href** (erforderlich)

URL zu beliebigen Medieninhalten, die von Windows Media Player unterstützt werden.

## <a name="parentchild-elements"></a>Über-/unterordnungselemente



| Hierarchy       | Elemente                                                                         |
|-----------------|----------------------------------------------------------------------------------|
| Übergeordnete Elemente | **Ein**                                                                        |
| Untergeordnete Elemente  | **Duration**, **Endmarker**, **previewduration**, **Startmarker**, **StartTime** |



 

## <a name="remarks"></a>Bemerkungen

Dieses Element gibt eine URL für ein Medien Inhalts Element an. Die URL kann auf jeden unterstützten Medientyp verweisen, wobei jedes Protokoll verwendet wird, das von Windows Media Player unterstützt wird.

Zu den unterstützten Medientypen zählen weiterhin Bilder wie GIF-und JPG-Images sowie Flash-Dateien mit der Dateinamenerweiterung ". swf". Diese Medientypen sind nützlich, um Werbeinhalte in eine Wiedergabeliste einzubeziehen. Mit Bilddateien und Flash Dateien, die in einer Schleife wiedergegeben werden, müssen Sie auch den Zeitraum angeben, in dem das Medien Element angezeigt werden soll, indem Sie ein **Duration** -Element innerhalb des **ref** -Elements einschließen. Wenn Sie möchten, dass ein Bild weiterhin angezeigt wird, während der nächste Eintrag in der Wiedergabeliste gepuffert wird, schließen Sie ein **param** -Element in das **Entry** -Element ein, legen Sie das **Name** -Attribut auf showwhilebuffereing fest, und legen Sie das Attribut **value** auf true fest.

Zum Verweisen auf Inhalte auf einer CD oder DVD, die dies zulässt, werden die Protokolle wmpcd und wmpdvd bereitgestellt. Wenn Sie z. b. das **href** -Attribut auf "wmpdvd://f/5/3" festlegen, wird Kapitel 3 von Titel 5 auf einer DVD wiedergegeben, aber nur, wenn die DVD erstellt wurde, um Sie zuzulassen.

Anwendungen, die digitale Medien aus einer Firewall öffnen, haben beim Öffnen der Medienelemente eine bessere Leistung, wenn die Adresse mit dem DNS-Namen (Domain Nameserver) anstelle der IP-Adresse angegeben wird.

Dieses Element wird am häufigsten für den URL-Rollover verwendet. Wenn Windows Media Player ein in einem **ref** -Element definiertes Medien Medium nicht öffnen kann, wird die URL im nächsten **ref** -Element ausprobiert. Sobald Windows Media Player Medieninhalte über eine URL öffnet, die im Bereich eines **Eintrags** Elements definiert ist, ignoriert Sie nachfolgende **ref** -Tags innerhalb dieses **Eintrags** Elements. Wenn die Wiedergabe des Inhalts abgeschlossen ist, wechselt Windows Media Player zum nächsten **Eintrags** Element, sofern vorhanden.

-   **Wichtig** Sobald Windows Media Player eine Verbindung mit einem Inhalt herstellt, auf den verwiesen wird, werden alle **anderen Verweis** Elemente in diesem **Eintrag** ignoriert, unabhängig davon, ob die Verbindung normal oder nicht ordnungsgemäß beendet wird.

Wenn das Medien Element, auf das verwiesen wird, eine Bilddatei ist, muss das **Duration** -Element verwendet werden, um die Anzeigezeit für das Bild anzugeben.

**Hinweis**

Der Versuch, Flash Medien wiederzugeben, die Sound mit dem ersten Frame enthalten, kann zu unerwarteten Ergebnissen führen. Sie sollten Flash Inhalte erstellen, um Sound ab dem zweiten Frame wiederzugeben.

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
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Unterstützte Protokolle und Dateitypen**](supported-protocols-and-file-types.md)
</dt> <dt>

[**Verweis auf Windows Media-Metadateielemente**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Referenz zu Windows Media-Metadateien**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





