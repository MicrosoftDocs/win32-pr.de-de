---
title: Closedcaption. samilang
description: Die samilang-Eigenschaft gibt die für Untertitel angezeigte Sprache an oder ruft Sie ab.
ms.assetid: 990fb180-cb37-4022-b236-03f5acfd3ad3
keywords:
- Closedcaption. samilang-Fenster Media Player
topic_type:
- apiref
api_name:
- ClosedCaption.SAMILang
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae99b9a164e29b4adeb2fd7b23a1b79945dcb26e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370635"
---
# <a name="closedcaptionsamilang"></a>Closedcaption. samilang

Die **samilang** -Eigenschaft gibt die für Untertitel angezeigte Sprache an oder ruft Sie ab.

``` syntax
player.closedCaption.SAMILang
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine Lese- **/schreibzeichenfolge**.

## <a name="remarks"></a>Bemerkungen

Eine Sami-Datei kann Text für eine oder mehrere Sprachen enthalten. Die Sprachen, die für Untertitel verfügbar sind, werden zwischen den Tags und in der Sami <STYLE> - </STYLE> Datei definiert. Eine Sprach-ID wird mit einer eindeutigen alphanumerischen Zeichenfolge angegeben, der ein Zeitraum (.) vorangestellt ist. Der für eine Sprache angegebene Name kann eine beliebige Zeichenfolge sein. Beispielsweise könnte Folgendes zum Definieren von US-Englisch verwendet werden:


```
.ENUSCC {Name:'English Captions' lang: en-US; SAMIType:CC;}

```



Wenn keine Sami-Sprache angegeben ist, wird standardmäßig die erste in der Sami-Datei definierte Sprache verwendet.

Der Wert, den Sie mithilfe von *closedcaption* übergeben. **Samilang** muss mit dem **Name** -Attribut im sprachspezifizierer identisch sein.

**Windows Media Player 10 Mobile:** Diese Eigenschaft ist schreibgeschützt und gibt immer eine leere Zeichenfolge zurück.

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird *closedcaption* verwendet. **Samilang** in einem HTML-SELECT-Element, um die Closed Caption-Sprache anzugeben. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
<!-- Create the SELECT element. -->
<SELECT ID = CCLANG  NAME = "CCLANG"  LANGUAGE = "JScript"

     /* Set the closed caption language when the SELECT element changes. */
        onChange = "Player.closedCaption.SAMILang = CCLANG.value;
        ">

        /* Fill in the SELECT element options. */
           <OPTION VALUE = "'Spanish Captions'">Spanish
           <OPTION VALUE = "'Japanese Captions'">Japanese
           <OPTION VALUE = "'English Captions'">English
           <OPTION VALUE = "'French Captions'">French
           <OPTION VALUE = "'German Captions'" SELECTED>German
</SELECT>

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Hinzufügen von Untertiteln zu digitalen Medien**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Closedcaption-Objekt**](closedcaption-object.md)
</dt> </dl>

 

 





