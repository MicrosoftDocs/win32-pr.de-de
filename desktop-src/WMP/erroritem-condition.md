---
title: ErrorItem.condition
description: Die Condition-Eigenschaft ruft einen Wert ab, der die Bedingung für den Fehler angibt.
ms.assetid: efb54b48-cfaa-479f-9ee6-ce6724dca24c
keywords:
- ErrorItem.condition Windows Media Player
topic_type:
- apiref
api_name:
- ErrorItem.condition
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5f4bfe2c4b2b517b0fd300a0c6465ae9f10147518937822212b621d808f0ded
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996640"
---
# <a name="erroritemcondition"></a>ErrorItem.condition

Die **Condition-Eigenschaft** ruft einen Wert ab, der die Bedingung für den Fehler angibt.

``` syntax
player.error.item(
        index
        ).condition
      
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**long**), die den Bedingungscode darstellt.

## <a name="remarks"></a>Hinweise

Der Bedingungscode ist ein Wert, der von Microsoft verwendet wird, um zusätzliche Informationen für technische Supportmitarbeiter bereitzustellen.

**Windows Media Player 10 Mobile:** Diese Eigenschaft gibt immer 0 zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player serie 9 oder höher.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ErrorItem-Objekt**](erroritem-object.md)
</dt> </dl>

 

 





