---
title: MOREINFO-Element
description: Das MOREINFO-Element gibt eine URL zu einer Website, einer E-Mail-Adresse oder einem Skriptbefehl an, der einem Show-, Clip- oder Banner zugeordnet ist.
ms.assetid: b817ef1d-4ca0-45f4-942b-695eaf537110
keywords:
- MOREINFO-Element Windows Media Player
topic_type:
- apiref
api_name:
- MOREINFO Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 925783b6bd48fbc8b944d7b8fd2a2b94a9954c7036114145b99b015b90cbb6d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134953"
---
# <a name="moreinfo-element"></a>MOREINFO-Element

Das **MOREINFO-Element** gibt eine URL zu einer Website, einer E-Mail-Adresse oder einem Skriptbefehl an, der einem Show-, Clip- oder Banner zugeordnet ist.

``` syntax
<MOREINFO
   HREF = "URL"
   TARGET = "Frame"
/>
```

## <a name="attributes"></a>Attribute

**HREF** (erforderlich)

URL zu einer Website, einer E-Mail-Adresse oder einem Skriptbefehl.

**Ziel**

Wert, der den Frame oder das Fenster definiert, in dem der Browser die durch das **HREF-Attribut** definierte Seite öffnet.

Dies kann eine Zeichenfolge sein, die einen Fensternamen oder einen der folgenden Werte enthält.



| Wert    | Beschreibung                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| \_leer  | Das Dokument wird in einem neuen Browserfenster geladen.                                                                              |
| \_self   | Das Dokument wird im selben Frame wie das aktuelle Dokument geladen, das das Windows Media Player-Steuerelement enthält.                |
| \_Elternteil | Das Dokument wird in den unmittelbar übergeordneten Frame des aktuellen Frames geladen, oder der aktuelle Frame, wenn kein übergeordneter Frame vorhanden ist. |
| \_top    | Das Dokument wird im vollständigen Browserfenster geladen und ersetzt alle anderen Frames oder Dokumente.                                  |



 

## <a name="parentchild-elements"></a>Übergeordnete/untergeordnete Elemente



| Hierarchy       | Elemente                       |
|-----------------|--------------------------------|
| Übergeordnete Elemente | **ASX,** **EINTRAG,** **BANNER** |
| Untergeordnete Elemente  | Keine                           |



 

## <a name="remarks"></a>Bemerkungen

Dieses Element gibt eine URL zu einer Website, einer E-Mail-Adresse oder einem **Skriptbefehl an. Der Benutzer kann auf das Ziel der URL zugreifen, indem er auf die Grafik oder den Text klickt, die bzw. der dem MOREINFO-Element zugeordnet ist.** Die Details hängen vom übergeordneten Element des **MOREINFO-Elements** ab:

-   Wenn das **MOREINFO-Element** das untergeordnete Element eines **ASX-Elements** ist, kann der Benutzer auf die URL zugreifen, indem er auf den Titel anzeigen klickt.
-   Wenn das **MOREINFO-Element** das untergeordnete Element eines **ENTRY-Elements** ist, kann der Benutzer auf die URL zugreifen, indem er auf den Titel des Clips klickt.
-   Wenn das **MOREINFO-Element** das untergeordnete Element eines **BANNER-Elements** ist, kann der Benutzer auf die URL zugreifen, indem er auf die Bannergrafik klickt.

Wenn das **HREF-Attribut** eine URL zu einer Website angibt, wird der Browser geöffnet und navigiert zur URL. Wenn das **HREF-Attribut** eine E-Mail-Adresse angibt, wird die E-Mail-Anwendung des Benutzers gestartet. Wenn das **HREF-Attribut** einen Skriptbefehl angibt, wird der Skriptbefehl im Browser ausgeführt.

**Hinweis**

Wenn das **MOREINFO-Element** in einem **ASX-** oder **ENTRY-Element** angezeigt wird und der Mauszeiger über dem Titel der Show (für ein **ASX-Element)** oder clip (für ein **ENTRY-Element)** gehalten wird, kann die im **HREF-Attribut** definierte URL ausgewählt werden und von Windows Media Player darauf zugegriffen werden.

Das **TARGET-Attribut** definiert den Frame oder das Fenster, in dem der Browser die durch das **HREF-Attribut** definierte Seite öffnet. Die Werte für dieses Attribut folgen standardmäßiger HTML-Syntax und -Definitionen. Wenn bei einem in eine Webseite eingebetteten Steuerelement kein **TARGET-Attribut** definiert ist, lädt die URL das aktuelle Browserfenster und ersetzt die vorhandene Seite, was bedeutet, dass der Inhalt nicht mehr wiedergegeben wird. Daher wird empfohlen, immer ein **TARGET-Attribut** anzugeben, wenn Sie das Windows Media Player-Steuerelement in eine Webseite einbetten.

Wenn die Metadatei im eigenständigen Windows Media Player geöffnet wird, wird das **TARGET-Attribut** ignoriert, und die URL wird in einem vorhandenen Browserfenster geladen. Wenn derzeit kein Browserfenster geöffnet ist, wird die URL in ein neues Browserfenster geladen.

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
| Version<br/> | Windows Media Player Version 70 oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Windows Referenz zu Medienmetadateielementen**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Referenz zu Medienmetadateien**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





