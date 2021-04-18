---
title: Buycd-Element
description: In diesem Abschnitt werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | Buycd-Element
ms.assetid: 01aaf20a-49ee-420b-a612-f09155390d4a
keywords:
- Fenster "buycd-Element" Media Player
topic_type:
- apiref
api_name:
- BuyCD Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ca1ebe4bd85015ca9ce1c0bece24e7dc47ff9fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368511"
---
# <a name="buycd-element"></a>Buycd-Element

> [!Note]  
> In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Das Element " **buycd** " gibt die URLs für Webseiten an, die von Windows Media Player angezeigt werden, wenn der Benutzer sich für einen Kauf entscheidet.

``` syntax
<BuyCD
    MediaPlayerURL = "URL"
    MediaCenterURL = "URL"
    BrowserURL = "URL"
/>
```

## <a name="attributes"></a>Attribute

<dl> <dt>

<span id="MediaPlayerURL__required_"></span><span id="mediaplayerurl__required_"></span><span id="MEDIAPLAYERURL__REQUIRED_"></span>**Mediaplayerurl** (erforderlich)
</dt> <dd>

Die URL für die Webseite, die im Online Store angezeigt wird, um eine CD oder DVD für den Kauf in Windows Media Player bereitzustellen.

</dd> <dt>

<span id="MediaCenterURL"></span><span id="mediacenterurl"></span><span id="MEDIACENTERURL"></span>**Mediacenterurl**
</dt> <dd>

Die URL für die Webseite, die im Online Store angezeigt wird, um eine CD oder DVD für den Kauf in Windows XP Media Center Edition 2004 Update anzubieten.

</dd> <dt>

<span id="BrowserURL"></span><span id="browserurl"></span><span id="BROWSERURL"></span>**Browserurl**
</dt> <dd>

Die URL für die Webseite, die im Online Store angezeigt wird, um eine CD oder DVD für den Einkauf in einem separaten Browserfenster anzubieten. Diese URL wird auch von Windows XP Service Pack 2 oder höher für das Feature **für Musik Online** verwendet.

</dd> </dl>

## <a name="parentchild-elements"></a>Über-/unterordnungselemente



| Hierarchy       | Element         |
|-----------------|-----------------|
| Übergeordnete Elemente | **ServiceInfo** |
| Untergeordnete Elemente  | Keine            |



 

## <a name="remarks"></a>Bemerkungen

Wenn der Benutzer auf eine Schaltfläche oder einen Link in Windows Media Player klickt, um eine CD oder DVD zu erwerben, sendet der Player die URL-Anforderung an ServiceTask1 mit Parametern, die mithilfe eines Fragezeichens (?) Abfrage Zeichenfolgen-Trennzeichen angehängt In der folgenden Tabelle werden die mit der URL-Anforderung gesendeten Parameter ausführlich erläutert. Andere können für Legacy Kompatibilitätszwecke vorhanden sein.



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



 

Windows XP Media Center Edition 2004 stellt Benutzern eine Benutzeroberfläche zur Verfügung, die in einer Entfernung angezeigt werden soll. Sie sollten Webseiten erstellen, damit der *mediacenterurl* -Parameter auf großen anzeigen angezeigt wird.

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

 

 





