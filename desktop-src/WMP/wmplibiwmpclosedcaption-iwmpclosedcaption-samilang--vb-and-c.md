---
title: IWMPClosedCaption-SAMILang-Eigenschaft
description: Die SAMILang-Eigenschaft ruft die Sprache ab, die für Untertitel angezeigt wird, oder legt sie fest.
ms.assetid: dcdd6bcd-b869-439f-b500-df26d3873b04
keywords:
- SAMILang-Windows Media Player
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
ms.openlocfilehash: 98354d5e1e4f796442dd0347a4ed2796cafdf7297d3829af9b8839d48df00c3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117930313"
---
# <a name="iwmpclosedcaptionsamilang-property"></a>IWMPClosedCaption::SAMILang -Eigenschaft

Die **SAMILang-Eigenschaft** ruft die Sprache ab, die für Untertitel angezeigt wird, oder legt sie fest.

## <a name="syntax"></a>Syntax


```CSharp
public System.String SAMILang {get; set;}
```


```VB

Public Property SAMILang As System.String
```





## <a name="property-value"></a>Eigenschaftswert

Die **System.String,die** den im Sprachbezeichner einer SAMI-Datei angegebenen Namen angibt.

## <a name="remarks"></a>Hinweise

Eine SAMI-Datei kann Text für eine oder mehrere Sprachen enthalten. Die für Untertitel verfügbaren Sprachen werden zwischen den Tags <STYLE> und </STYLE> in der SAMI-Datei definiert. Ein Sprachbezeichner wird mit einer eindeutigen alphanumerischen Zeichenfolge angegeben, der ein -Zeitraum (.) voran steht. Der für eine Sprache angegebene Name kann eine beliebige Zeichenfolge sein. Beispielsweise kann folgendes verwendet werden, um Englisch (USA) zu definieren:


```
.ENUSCC {Name:'English Captions' lang: en-US; SAMIType:CC;}
```



Wenn keine SAMI-Sprache angegeben ist, wird standardmäßig die erste sprache verwendet, die in der SAMI-Datei definiert ist.

Die Zeichenfolge, die Sie mit **SAMILang** festlegen, muss mit dem **Name-Attribut** im Sprachspezifizierer übereinstimmen.

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

[**IWMPClosedCaption-Schnittstelle (VB und C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption2-Schnittstelle (VB und C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





