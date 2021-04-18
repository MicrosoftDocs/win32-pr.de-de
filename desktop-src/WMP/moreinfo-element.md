---
title: Moreingefo-Element
description: Das moreinfo-Element gibt eine URL zu einer Website, einer e-Mail-Adresse oder einem Skript Befehl an, die einer Show, einem Clip oder einem Banner zugeordnet ist.
ms.assetid: b817ef1d-4ca0-45f4-942b-695eaf537110
keywords:
- Moreingefo-Element Fenster Media Player
topic_type:
- apiref
api_name:
- MOREINFO Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: efc54fe9745566ec7eaa87b7f0f4645b07a055f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358260"
---
# <a name="moreinfo-element"></a>Moreingefo-Element

Das **moreinfo** -Element gibt eine URL zu einer Website, einer e-Mail-Adresse oder einem Skript Befehl an, die einer Show, einem Clip oder einem Banner zugeordnet ist.

``` syntax
<MOREINFO
   HREF = "URL"
   TARGET = "Frame"
/>
```

## <a name="attributes"></a>Attribute

**Href** (erforderlich)

URL zu einer Website, einer e-Mail-Adresse oder einem Skript Befehl.

**Spar**

Ein Wert, der den Frame oder das Fenster definiert, in dem der Browser die durch das **href** -Attribut definierte Seite öffnet.

Dabei kann es sich um eine Zeichenfolge handeln, die einen Fensternamen oder einen der folgenden Werte enthält.



| Wert    | BESCHREIBUNG                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| \_Blitz  | Das Dokument wird in einem neuen Browserfenster geladen.                                                                              |
| \_self   | Das Dokument wird im gleichen Frame geladen wie das aktuelle Dokument, das das Windows Media Player-Steuerelement enthält.                |
| \_übergeordneten | Das Dokument wird in den unmittelbar übergeordneten Frame des aktuellen Frames oder den aktuellen Frame geladen, wenn kein übergeordneter Frame vorhanden ist. |
| \_top    | Das Dokument wird im vollständigen Browserfenster geladen und ersetzt alle anderen Frames oder Dokumente.                                  |



 

## <a name="parentchild-elements"></a>Über-/unterordnungselemente



| Hierarchy       | Elemente                       |
|-----------------|--------------------------------|
| Übergeordnete Elemente | **ASX**, **Eintrag**, **Banner** |
| Untergeordnete Elemente  | Keine                           |



 

## <a name="remarks"></a>Bemerkungen

Dieses Element gibt eine URL zu einer Website, einer e-Mail-Adresse **oder einem Skript Befehl an. Der Benutzer kann auf das Ziel der URL zugreifen, indem er auf die Grafik oder den Text klickt, der dem Morein FO-Element zugeordnet ist** . Die Details hängen von dem übergeordneten Element des **moreingefo** -Elements ab:

-   Wenn das **moreinfo** -Element das untergeordnete Element eines **ASX** -Elements ist, kann der Benutzer auf die URL zugreifen, indem er auf den Titel anzeigen klickt.
-   Wenn das **moreinfo** -Element das untergeordnete Element eines **Entry** -Elements ist, kann der Benutzer auf die URL zugreifen, indem er auf den Clip-Titel klickt.
-   Wenn das **Moran FO** -Element das untergeordnete Element eines **Banner** Elements ist, kann der Benutzer auf die URL zugreifen, indem er auf die Banner Grafik klickt.

Wenn das **href** -Attribut eine URL zu einer Website angibt, wird der Browser geöffnet und navigiert zur URL. Wenn das **href** -Attribut eine e-Mail-Adresse angibt, wird die e-Mail des Benutzers gestartet. Wenn das **href** -Attribut einen Skript Befehl angibt, wird der Skript Befehl im Browser ausgeführt.

**Hinweis**

Wenn das **moreinfo** -Element in einem **ASX** -oder **Entry** -Element angezeigt wird, wenn der Mauszeiger über dem Titel der Anzeige (für **ein-** Element des-Elements) oder von Clip (bei einem **Entry** -Element) gehalten wird, kann die im **href** -Attribut definierte URL ausgewählt und von Windows Media Player aufgerufen werden.

Das **Ziel** Attribut definiert den Frame oder das Fenster, in dem der Browser die durch das **href** -Attribut definierte Seite öffnet. Die Werte für dieses Attribut entsprechen standardmäßigen HTML-Syntax und-Definitionen. Wenn ein in einer Webseite eingebettetes Steuerelement kein **Ziel** Attribut definiert ist, lädt die URL das aktuelle Browserfenster und ersetzt die vorhandene Seite, was bedeutet, dass die Inhalte nicht mehr abgespielt werden. Daher wird empfohlen, beim Einbetten des Windows Media Player-Steuer Elements auf einer Webseite immer ein **Ziel** Attribut anzugeben.

Wenn die Metadatendatei im eigenständigen Windows-Media Player geöffnet ist, wird das **Ziel** Attribut ignoriert, und die URL wird in ein vorhandenes Browserfenster geladen. Wenn derzeit kein Browserfenster geöffnet ist, wird die URL in einem neuen Browserfenster geladen.

## <a name="examples"></a>Beispiele


```XML
<ASX VERSION="3.0">

   <TITLE>Example Media Player Show</TITLE>
   <MOREINFO HREF="https://example.microsoft.com/info/show_info.htm" />
   
   <ENTRY>
      <TITLE>Example Clip</TITLE>
      <MOREINFO HREF="https://example.microsoft.com/info/clip1_info.htm" />
      <REF HREF="mms://example.microsoft.com/media.asf" />
   </ENTRY>
   
</ASX>

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------|
| Version<br/> | Windows Media Player, Version 70 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Verweis auf Windows Media-Metadateielemente**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Referenz zu Windows Media-Metadateien**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





