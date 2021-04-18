---
title: Iwmpcdromburn-Bezeichnung (Eigenschaft)
description: Die Label-Eigenschaft ruft die Zeichenfolge der CD-Volumebezeichnung ab
ms.assetid: 46e7741c-59c5-46d8-b9ca-09892d907cd7
keywords:
- Label-Eigenschaften Fenster Media Player
- Label-Eigenschaft, Windows Media Player, iwmpcdromburn-Schnittstelle
- Iwmpcdromburn Interface, Windows Media Player, Bezeichnung (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPCdromBurn.label
- IWMPCdromBurn.get_label
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05da344f1148de7e79cb605135964c6ab8225ac0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372128"
---
# <a name="iwmpcdromburnlabel-property"></a>Iwmpcdromburn:: Label-Eigenschaft

Die *Label* -Eigenschaft ruft die Zeichenfolge der CD-Volumebezeichnung ab

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```CSharp
public System.String label {get;}
```


```VB

Public ReadOnly Property label As System.String
```





## <a name="property-value"></a>Eigenschaftswert

Eine **System. String** , die die Zeichenfolge der Volumebezeichnung ist.

## <a name="remarks"></a>Bemerkungen

Aufgrund der Art und Weise, wie CD-Bezeichnungen gespeichert werden, ist die Bezeichnung der CD möglicherweise kürzer als die Länge der angegebenen volumezeichenfolge. Wenn die Zeichenfolge länger als die maximale Länge einer CD-Bezeichnung ist, wird der Text abgeschnitten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpcdromburn-Schnittstelle (VB und c#)**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





