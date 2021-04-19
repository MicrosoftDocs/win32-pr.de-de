---
title: InfoCenter-Element
description: In diesem Abschnitt werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | InfoCenter-Element
ms.assetid: 1a9cc513-5dd1-46d8-9409-16413695b4c8
keywords:
- InfoCenter-Element Fenster Media Player
topic_type:
- apiref
api_name:
- InfoCenter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ef62e0f6b41090642400a7f0a8b88af72818da4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359257"
---
# <a name="infocenter-element"></a>InfoCenter-Element

> [!Note]  
> In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Das **Infocenter** -Element gibt die URL der **Webseite an, die von Windows** Media Player in der Info Center-Ansichts Funktion von angezeigt wird, wenn der Online Store aktiv ist.

``` syntax
<InfoCenter
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

Der Benutzer steuert, wann die Info Center Ansicht aktiv ist.

Zum Abrufen von Informationen über das aktuell wiedergegebene Medien Element müssen Sie eine Instanz von Windows Media Player-Steuerelement in Ihre Webseite einbetten und das Player-Objektmodell verwenden.

In der folgenden Tabelle werden die mit der URL-Anforderung gesendeten Parameter ausführlich erläutert. Andere können für Legacy Kompatibilitätszwecke vorhanden sein.



| Name         | Wert                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Geoid*      | ID des geografischen Standorts für Windows. Die Speicherort-ID wird vom Benutzer im Bereich **Speicherort** der Einstellungen für Regions-und Sprachoptionen in der Systemsteuerung angegeben. |
| *locale*     | Windows Media Player-Gebiets Schema-ID.                                                                                                                                     |
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

 

 





