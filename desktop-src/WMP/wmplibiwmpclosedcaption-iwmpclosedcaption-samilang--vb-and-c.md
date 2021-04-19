---
title: Iwmpclosedcaption samilang-Eigenschaft
description: Die samilang-Eigenschaft ruft die für Untertitel angezeigte Sprache ab oder legt diese fest.
ms.assetid: dcdd6bcd-b869-439f-b500-df26d3873b04
keywords:
- Samilang-Eigenschaften Fenster Media Player
- Samilang-Eigenschaft, Windows Media Player, iwmpclosedcaption-Schnittstelle
- Iwmpclosedcaption-Schnittstelle, Windows Media Player, samilang (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPClosedCaption.SAMILang
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe29defa3736795c88613ee7ab2ef11a914a3f80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369249"
---
# <a name="iwmpclosedcaptionsamilang-property"></a>Iwmpclosedcaption:: samilang-Eigenschaft

Die **samilang** -Eigenschaft ruft die für Untertitel angezeigte Sprache ab oder legt diese fest.

## <a name="syntax"></a>Syntax


```CSharp
public System.String SAMILang {get; set;}
```


```VB

Public Property SAMILang As System.String
```





## <a name="property-value"></a>Eigenschaftswert

Der **System. String** -Wert, der dem Namen entspricht, der in der Sprach-ID einer Sami-Datei angegeben ist.

## <a name="remarks"></a>Bemerkungen

Eine Sami-Datei kann Text für eine oder mehrere Sprachen enthalten. Die Sprachen, die für Untertitel verfügbar sind, werden zwischen den Tags und in der Sami <STYLE> - </STYLE> Datei definiert. Eine Sprach-ID wird mit einer eindeutigen alphanumerischen Zeichenfolge angegeben, der ein Zeitraum (.) vorangestellt ist. Der für eine Sprache angegebene Name kann eine beliebige Zeichenfolge sein. Beispielsweise könnte Folgendes zum Definieren von US-Englisch verwendet werden:


```
.ENUSCC {Name:'English Captions' lang: en-US; SAMIType:CC;}
```



Wenn keine Sami-Sprache angegeben ist, wird standardmäßig die erste in der Sami-Datei definierte Sprache verwendet.

Die Zeichenfolge, die Sie mit **samilang** festlegen, muss mit dem **Name** -Attribut im sprachspezifizierer identisch sein.

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

 

 





