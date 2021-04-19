---
title: Param-Element (WMP-SDK)
description: Das param-Element definiert einen benutzerdefinierten Parameter, der einer Wiedergabeliste oder einem Element einer Wiedergabeliste zugeordnet ist.
ms.assetid: d905a42a-ac89-4c99-94ca-b3b7060ebbdc
keywords:
- Param-Element, Windows Media Player
topic_type:
- apiref
api_name:
- PARAM Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7879f9dc9a8cf31afee5a3f1684af5cba33a9e0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373975"
---
# <a name="param-element"></a>Param-Element

Das **param** -Element definiert einen benutzerdefinierten Parameter, der einer Wiedergabeliste oder einem Element einer Wiedergabeliste zugeordnet ist.

``` syntax
<PARAM
   NAME = "parameter name"
   VALUE = "parameter value"
/>
```

## <a name="parameters"></a>Parameter

Ein Parameter kann auch mit der Anzeige anstelle eines einzelnen Clips verknüpft werden, indem dieses Element direkt nach dem **ASX** -Tag platziert wird. Diese Elemente werden durch ihre Namen und einen Indexwert, der mit Null beginnt, referenziert.

> [!Note]  
> Dieses **ASX** -Element ist nur für Windows Media Player Version 6,01 und höher verfügbar. Die Standardinstallation von Microsoft Internet Explorer 5 umfasst eine kompatible Version von Windows Media Player.

 

## <a name="attributes"></a>Attribute

**NAME**

Der Name, mit dem auf den Parameterwert zugegriffen wird. Der Name kann eine beliebige gültige Zeichenfolge sein. Die folgenden Zeichen folgen wurden bereits definiert.



| Zeichenfolge                          | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AllowShuffle                    | Das **value** -Attribut gibt an, ob die Metadatendatei-Wiedergabeliste der Windows Media Player Shuffle-Funktion das Abspielen der Einträge in zufälliger Reihenfolge ermöglicht. Das **value** -Attribut kann auf "yes" oder "No" festgelegt werden. Der Standardwert ist "No".                                                                                                                                                                                                                                                                                                                                                                  |
| CanPause                        | Das **value** -Attribut gibt an, ob der Benutzer die Wiedergabe anhalten kann. Das **value** -Attribut kann auf "yes" oder "No" festgelegt werden. Der Standardwert ist "yes".                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| CanSeek                         | Das **value** -Attribut gibt an, ob der Benutzer die aktuelle Wiedergabe Position mithilfe der Suchleiste, der schnellen Vorwärtsbewegung oder der schnellen Umkehrung ändern kann. Das **value** -Attribut kann auf "yes" oder "No" festgelegt werden. Der Standardwert ist "yes".                                                                                                                                                                                                                                                                                                                                                                    |
| Canskipback                     | Das **value** -Attribut gibt an, ob der Benutzer **durch Klicken auf** zurück zum vorherigen Wiedergabelisten Element springen kann. Das **value** -Attribut kann auf "yes" oder "No" festgelegt werden. Der Standardwert ist "yes".                                                                                                                                                                                                                                                                                                                                                                                         |
| Canskipforward                  | Das **value** -Attribut gibt an, ob der Benutzer durch Klicken auf **weiter** auf das nächste Wiedergabelisten Element springen kann. Das **value** -Attribut kann auf "yes" oder "No" festgelegt werden. Der Standardwert ist "yes".                                                                                                                                                                                                                                                                                                                                                                                                  |
| Cpradioid                       | Das **value** -Attribut gibt die ID eines Radio Feeds an, der von einem Online Store vom Typ 1 bereitgestellt wird. Das heißt, das **value** -Attribut muss mit dem Radio ID-Feld eines der Radio Feeds im Katalog des Online Stores identisch sein. Das übergeordnete Element ist das **ASX** -Element.                                                                                                                                                                                                                                                                                                                                   |
| Codierung                        | Das **value** -Attribut wird auf "UTF-8" festgelegt, um anzugeben, dass es sich bei der Metadatei um eine Unicode-codierte Datei (UTF-8) handelt.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Htmlllink                       | Das **value** -Attribut ist eine Zeichenfolge, die von einem Onlinespeicher vom Typ 1 bereitgestellt wird Windows Media Player übergibt die Zeichenfolge an die [iwmpcontentpartner:: getiteminfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) -Methode, die vom Plug-in des Online Stores implementiert wird. Die **getiteminfo** -Methode gibt die URL der Webseite zurück, die im Fenster " **jetzt Wiedergabe** " des Players angezeigt werden soll. Die Webseite hat Zugriff auf alle Methoden, die das **externe** Objekt für den Typ 1 speichert. Eine Liste dieser Methoden finden Sie unter [externes Objekt für den Typ 1 Online Stores](external-object-for-type-1-online-stores.md). |
| HtmlView                        | Das **value** -Attribut gibt eine URL an, die im Bereich für die wieder **Gabe** des vollmodusplayers für die Dauer der Wiedergabeliste oder den aktuellen Eintrag angezeigt wird, je nachdem, ob es sich beim übergeordneten Element um das **ASX** -Element oder ein **Entry** -Element handelt. HtmlView wird für das Windows Media Player-Steuerelement nicht unterstützt.                                                                                                                                                                                                                                                                               |
| Log:*FieldName* \[ :*Namespace*\] | Das **value** -Attribut gibt den Wert an, auf den das angegeben Protokollfeld festgelegt wird. Der:*Namespace* -Teil des **Name** -Attributs ist optional.                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Vorab Puffer                       | Das **value** -Attribut gibt an, ob der nächste Wiedergabelisten Eintrag mit der Pufferung vor dem Ende des aktuellen Eintrags beginnt, was einen nahtlosen Übergang ermöglicht. Das **value** -Attribut kann auf "true" oder "false" festgelegt werden.                                                                                                                                                                                                                                                                                                                                                                                 |
| Showwhilebuffereing              | Das **value** -Attribut gibt an, ob eine Bilddatei, auf die vom aktuellen **Eintrags** Element verwiesen wird, weiterhin nach der angegebenen Dauer angezeigt wird, während der nächste Wiedergabelisten Eintrag gepuffert wird. Das **value** -Attribut kann auf "true" oder "false" festgelegt werden.                                                                                                                                                                                                                                                                                                                                         |



 

**VALUE**

Wert, der diesem Parameter zugeordnet ist. Dabei kann es sich entweder um einen numerischen oder einen Zeichen folgen Wert handeln.

## <a name="parentchild-elements"></a>Über-/unterordnungselemente



| Hierarchy       | Elemente           |
|-----------------|--------------------|
| Übergeordnete Elemente | **ASX**, **Eintrag** |
| Untergeordnete Elemente  | Keine               |



 

## <a name="remarks"></a>Bemerkungen

Dieses Element ermöglicht es Benutzern, zusätzliche Informationen zu den einzelnen Clips im **Eintrags** Element zu platzieren, in dem Sie enthalten ist. Verwenden Sie zum Abrufen der im Wiedergabelisten **Eintrag** angegebenen Metadateninformationen das *Medium*. **getiteminfo** -Methode. Das *Medium*. die **getiteminfo** -Methode ruft den Wert des **value** -Attributs ab, wenn der Name des Parameters angegeben ist. In früheren Versionen von Windows Media Player die im Wiedergabelisten **Eintrag** angegebenen Metadateninformationen mithilfe der **getmediaparameter** -Methode abgerufen werden, wobei der Name des Parameters und eine Indexnummer für den Eintrag angegeben wird.

Ein Parameter kann auch mit der Anzeige anstelle eines einzelnen Clips verknüpft werden, indem dieses Element direkt nach dem **ASX** -Tag platziert wird. Diese Elemente werden durch ihre Namen und einen Indexwert, der mit Null beginnt, referenziert.

**Hinweis**

Dieses **ASX** -Element ist nur für Windows Media Player Version 6,01 und höher verfügbar. Die Standardinstallation von Microsoft Internet Explorer 5 umfasst eine kompatible Version von Windows Media Player.

## <a name="examples"></a>Beispiele


```XML
<ASX VERSION="3.0">
   <TITLE>Example Media Player Show</TITLE>
   <PARAM NAME="Director" VALUE="Jane D." />
   
   <ENTRY>
      <TITLE>Example Clip</TITLE>
      <REF HREF="https://sample.microsoft.com/media.asf" />
      <PARAM NAME="Location" VALUE="North America" />
      <PARAM NAME="Release Date" VALUE="March 1998" />
   </ENTRY>
   
   <ENTRY>
      <TITLE>Another Clip</TITLE>
      <REF HREF="https://sample.microsoft.com/more_media.asf" />
      <PARAM NAME="Location" VALUE="Japan">
      <PARAM NAME="Release Date" VALUE="December 1996" />
   </ENTRY>
</ASX>

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher, Windows Media Player 9 oder höher ist für die vordefinierten namens Attribute erforderlich, Windows Media Player 10 oder höher ist für die vordefinierten Namen "CanPause", "CanSeek", "canskipback" und "canskipforward" erforderlich.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Anzeigen von Webseiten in Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Protokollieren von Streamdaten**](logging-stream-data.md)
</dt> <dt>

[**Verweis auf Windows Media-Metadateielemente**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Referenz zu Windows Media-Metadateien**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





