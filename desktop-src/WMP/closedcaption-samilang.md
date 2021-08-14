---
title: ClosedCaption.SAMILang
description: Die SAMILang-Eigenschaft gibt die Sprache an, die für Untertitel angezeigt wird, oder ruft sie ab.
ms.assetid: 990fb180-cb37-4022-b236-03f5acfd3ad3
keywords:
- ClosedCaption.SAMILang-Windows Media Player
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
ms.openlocfilehash: 4c423b041601a38e81b1c4e83c34c010edb3365a4eb7e05596038fa887818ba1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342285"
---
# <a name="closedcaptionsamilang"></a>ClosedCaption.SAMILang

Die **SAMILang-Eigenschaft** gibt die Sprache an, die für Untertitel angezeigt wird, oder ruft sie ab.

``` syntax
player.closedCaption.SAMILang
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine Zeichenfolge mit **Lese-/Schreibzugriff.**

## <a name="remarks"></a>Hinweise

Eine SAMI-Datei kann Text für eine oder mehrere Sprachen enthalten. Die für Untertitel verfügbaren Sprachen werden zwischen den Tags <STYLE> und </STYLE> in der SAMI-Datei definiert. Ein Sprachbezeichner wird mit einer eindeutigen alphanumerischen Zeichenfolge angegeben, der ein Zeitraum (.) voran steht. Der für eine Sprache angegebene Name kann eine beliebige Zeichenfolge sein. Beispielsweise kann folgendes verwendet werden, um englisch (USA) zu definieren:


```
.ENUSCC {Name:'English Captions' lang: en-US; SAMIType:CC;}

```



Wenn keine SAMI-Sprache angegeben ist, wird standardmäßig die erste sprache verwendet, die in der SAMI-Datei definiert ist.

Der Wert, den Sie mit *ClosedCaption übergeben.* **SAMILang muss** mit dem **Name-Attribut** im Sprachspezifizierer übereinstimmen.

**Windows Media Player 10 Mobile:** Diese Eigenschaft ist schreibgeschützt und gibt immer eine leere Zeichenfolge zurück.

## <a name="examples"></a>Beispiele

Im folgenden beispiel JScript *ClosedCaption verwendet.* **SAMILang** in einem HTML SELECT-Element, um die Sprache für Untertitel anzugeben. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Hinzufügen von Untertiteln zu digitalen Medien**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**ClosedCaption-Objekt**](closedcaption-object.md)
</dt> </dl>

 

 





