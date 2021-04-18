---
title: Iwmpclosedcaption samistyle (Eigenschaft)
description: Die samistyle-Eigenschaft ruft den Untertitel Stil ab oder legt ihn fest.
ms.assetid: 0b1f92c6-b659-4ade-90c8-62a06e475f5c
keywords:
- Samistyle-Eigenschaften Fenster Media Player
- Samistyle-Eigenschaft, Windows Media Player, iwmpclosedcaption-Schnittstelle
- Iwmpclosedcaption-Schnittstelle, Windows Media Player, samistyle (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPClosedCaption.SAMIStyle
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bd0b48fc1807d6ca1854651c7f222183a845be3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365650"
---
# <a name="iwmpclosedcaptionsamistyle-property"></a>Iwmpclosedcaption:: samistyle (Eigenschaft)

Die **samistyle** -Eigenschaft ruft den Untertitel Stil ab oder legt ihn fest.

## <a name="syntax"></a>Syntax


```CSharp
public System.String SAMIStyle {get; set;}
```


```VB

Public Property SAMIStyle As System.String
```





## <a name="property-value"></a>Eigenschaftswert

Der **System. String** -Wert, der dem Namen entspricht, der im Stil Bezeichner einer Sami-Datei angegeben ist.

## <a name="remarks"></a>Bemerkungen

Eine Sami-Datei kann mehrere Format Definitionen enthalten. Sami-Stile werden zwischen den Tags und in der Sami <STYLE> - </STYLE> Datei definiert. Ein Stil wird mit einer Text Zeichenfolge mit vorangestelltem \# Zeichen definiert. Beispiel:


```
#Emphasis1 {Name: Big Bold Italic; font-size: 14pt; text-align: center;
            color: blue; font-family: sans-serif; font-weight: bold;
            font-style: italic;}
```



Gibt einen Stil an, der eine bestimmte Schriftart erzeugt.

Wenn kein Sami-Format angegeben ist, wird standardmäßig das erste Format verwendet, das in der Sami-Datei definiert ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Hinzufügen von Untertiteln zu digitalen Medien**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Iwmpclosedcaption-Schnittstelle (VB und c#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption2-Schnittstelle (VB und c#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





