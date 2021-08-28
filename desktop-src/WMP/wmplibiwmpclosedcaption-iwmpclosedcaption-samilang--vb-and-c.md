---
title: IWMPClosedCaption-SAMILang-Eigenschaft
description: Die SAMILang-Eigenschaft ruft die sprache ab, die für Untertitel angezeigt wird, oder legt sie fest.
ms.assetid: dcdd6bcd-b869-439f-b500-df26d3873b04
keywords:
- SAMILang-Eigenschaft Windows Media Player
- SAMILang-Eigenschaft Windows Media Player , IWMPClosedCaption-Schnittstelle
- IWMPClosedCaption-Schnittstelle Windows Media Player , SAMILang-Eigenschaft
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
ms.openlocfilehash: a9577f7d9030a12a12596fe2cdc2a999922658ce
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887178"
---
# <a name="iwmpclosedcaptionsamilang-property"></a>IWMPClosedCaption::SAMILang-Eigenschaft

Die **SAMILang-Eigenschaft** ruft die sprache ab, die für Untertitel angezeigt wird, oder legt sie fest.

## <a name="syntax"></a>Syntax


```CSharp
public System.String SAMILang {get; set;}
```


```VB

Public Property SAMILang As System.String
```





## <a name="property-value"></a>Eigenschaftswert

Die **System.String,** die dem namen entspricht, der im Sprachbezeichner einer SAMI-Datei angegeben ist.

## <a name="remarks"></a>Hinweise

Eine SAMI-Datei kann Text für eine oder mehrere Sprachen enthalten. Die sprachen, die für Untertitel verfügbar sind, werden zwischen STYLE &lt; und Tags in der &gt; </STYLE> SAMI-Datei definiert. Ein Sprachbezeichner wird mit einer eindeutigen alphanumerischen Zeichenfolge angegeben, der ein Punkt (.) vorangestellt ist. Der für eine Sprache angegebene Name kann eine beliebige Zeichenfolge sein. Beispielsweise kann Folgendes verwendet werden, um englisch (USA) zu definieren:


```
.ENUSCC {Name:'English Captions' lang: en-US; SAMIType:CC;}
```



Wenn keine SAMI-Sprache angegeben ist, wird standardmäßig die erste in der SAMI-Datei definierte Sprache verwendet.

Die Zeichenfolge, die Sie mit **SAMILang** festlegen, muss mit dem **Name-Attribut** im Sprachspezifizierer übereinstimmen.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Hinzufügen von Untertiteln zu digitalen Medien**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**IWMPClosedCaption-Schnittstelle (VB und C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption2-Schnittstelle (VB und C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





