---
title: Albuminfo-Element
description: Das Element "Albuminfo" gibt die URL für die Webseite an, die von Windows Media Player angezeigt wird, wenn der Benutzer weitere Informationen zu einem bestimmten Medien Element anzeigen möchte.
ms.assetid: c872e95a-3723-4ce8-8d61-e2bc9e12c785
keywords:
- Fenster Media Player des Albuminfo-Elements
topic_type:
- apiref
api_name:
- AlbumInfo Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3805ae2d5fca687ce024efca74e0254db7c8ae3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361526"
---
# <a name="albuminfo-element"></a>Albuminfo-Element

> [!Note]  
> In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Das Element " **Albuminfo** " gibt die URL für die Webseite an, die von Windows Media Player angezeigt wird, wenn der Benutzer weitere Informationen zu einem bestimmten Medien Element anzeigen möchte.

``` syntax
<AlbumInfo
   URL = "URL"
/>
      
```

## <a name="attributes"></a>Attribute

<dl> <dt>

<span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (erforderlich)
</dt> <dd>

Die URL für die Webseite, die von Windows Media Player angezeigt wird.

</dd> </dl>

## <a name="parentchild-elements"></a>Über-/unterordnungselemente



| Hierarchy       | Element         |
|-----------------|-----------------|
| Übergeordnete Elemente | **ServiceInfo** |
| Untergeordnete Elemente  | Keine            |



 

## <a name="remarks"></a>Bemerkungen

Wenn der Benutzer auf eine Schaltfläche in Windows Media Player klickt, um zusätzliche Informationen zu einem bestimmten Medien Element anzuzeigen, sendet der Player die URL-Anforderung mit Parametern, die mithilfe eines Fragezeichens (?) Abfrage Zeichenfolgen-Trennzeichen angehängt werden. In der folgenden Tabelle werden die mit der URL-Anforderung gesendeten Parameter ausführlich erläutert. Andere können für Legacy Kompatibilitätszwecke vorhanden sein.



| Name         | Wert                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Aufzunehmen*      | Der Wert des **WM/albumtitle-** Attributs für das Medien Element.                                                                                                        |
| *Interpret*     | Der Wert des **WM/Album-** Attributs, sofern vorhanden, oder andernfalls der Wert des **Author** -Attributs für das Medien Element.                                         |
| *Geoid*      | ID des geografischen Standorts für Windows. Die Speicherort-ID wird vom Benutzer im Bereich **Speicherort** der Einstellungen für Regions-und Sprachoptionen in der Systemsteuerung angegeben. |
| *locale*     | Windows Media Player-Gebiets Schema-ID.                                                                                                                                     |
| *Titel*      | Der Wert des **Title** -Attributs für das Medien Element.                                                                                                                |
| *UFID*       | Der Wert des **WM/UniqueFileIdentifier-** Attributs für das Medien Element.                                                                                              |
| *UserLocale* | Windows-Gebiets Schema-ID. Das Gebiets Schema wird vom Benutzer im Bereich " **Standards und Formate** " der Einstellungen für Regions-und Sprachoptionen in der Systemsteuerung angegeben.        |
| *version*    | Windows Media Player-Versionsnummer im folgenden Format: 10.0. x. xxxx oder 11.0. x. xxxx.                                                                         |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------|
| Version<br/> | Windows Media Player 10 oder höher.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Beispiel eines serviceInfo-Dokuments für einen Online Store vom Typ 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Beispiel eines serviceInfo-Dokuments für einen Typ 2-Online Store**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Servicinfo-Dokument**](serviceinfo-document.md)
</dt> </dl>

 

 





