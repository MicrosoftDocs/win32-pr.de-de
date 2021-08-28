---
title: IWMPClosedCaption-SAMIStyle-Eigenschaft
description: Die SAMIStyle-Eigenschaft ruft den Untertitelstil ab oder legt diese fest.
ms.assetid: 0b1f92c6-b659-4ade-90c8-62a06e475f5c
keywords:
- SAMIStyle-Windows Media Player
- SAMIStyle-Eigenschaft Windows Media Player , IWMPClosedCaption-Schnittstelle
- IWMPClosedCaption-Schnittstelle Windows Media Player , SAMIStyle-Eigenschaft
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
ms.openlocfilehash: e147b48ffb80e1114133b59018cef514eefd2ae7
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885868"
---
# <a name="iwmpclosedcaptionsamistyle-property"></a>IWMPClosedCaption::SAMIStyle -Eigenschaft

Die **SAMIStyle-Eigenschaft** ruft den Untertitelstil ab oder legt diese fest.

## <a name="syntax"></a>Syntax


```CSharp
public System.String SAMIStyle {get; set;}
```


```VB

Public Property SAMIStyle As System.String
```





## <a name="property-value"></a>Eigenschaftswert

Die **System.String-Datei,** bei der es sich um den im Stilbezeichner einer SAMI-Datei angegebenen Namen handelt.

## <a name="remarks"></a>Hinweise

Eine SAMI-Datei kann mehrere Formatformatdefinitionen enthalten. SAMI-Stile werden zwischen &lt; style und tags in der &gt; </STYLE> SAMI-Datei definiert. Ein Stil wird mit einer Textzeichenfolge definiert, der ein Zeichen \# voran steht. Beispiel:


```
#Emphasis1 {Name: Big Bold Italic; font-size: 14pt; text-align: center;
            color: blue; font-family: sans-serif; font-weight: bold;
            font-style: italic;}
```



Dies gibt einen Stil an, der eine bestimmte Schriftart erzeugt.

Wenn kein SAMI-Stil angegeben ist, wird standardmäßig der erste in der SAMI-Datei definierte Stil verwendet.

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

 

 





