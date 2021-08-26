---
title: LABEL-Eigenschaft "IWMPC wie die Bezeichnung"
description: Die Label-Eigenschaft ruft die CD-Volumebezeichnungszeichenfolge ab.
ms.assetid: 46e7741c-59c5-46d8-b9ca-09892d907cd7
keywords:
- Bezeichnungseigenschafts-Windows Media Player
- label-eigenschaft Windows Media Player , IWMPC wie Die Schnittstelle
- IWMPCwiederSchnittstellenschnittstelle Windows Media Player , Bezeichnungseigenschaft
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
ms.openlocfilehash: d8b8917706e20b5d1361054ac5f6fd209c0026837c428ecba715727e3d828a4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000549"
---
# <a name="iwmpcdromburnlabel-property"></a>IWMPC wie die Eigenschaft "::label"

Die *Label-Eigenschaft* ruft die CD-Volumebezeichnungszeichenfolge ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```CSharp
public System.String label {get;}
```


```VB

Public ReadOnly Property label As System.String
```





## <a name="property-value"></a>Eigenschaftswert

Eine **System.String,** die die Volumebezeichnungszeichenfolge ist.

## <a name="remarks"></a>Hinweise

Aufgrund der Art und Weise, wie CD-Bezeichnungen gespeichert werden, ist die Bezeichnung der CD möglicherweise kürzer als die Länge der angegebenen Volumebezeichnungszeichenfolge. Wenn die Zeichenfolge länger als die maximale Länge einer CD-Bezeichnung ist, wird der Text abgeschnitten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPCführungsschnittstelle (VB und C#)**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





