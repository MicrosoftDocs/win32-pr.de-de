---
title: ErrorItem. errorcontext
description: Die errorcontext-Eigenschaft ruft einen Wert ab, der den Kontext des Fehlers angibt.
ms.assetid: 700d2bf0-dd3b-4211-99ea-58f952cf24b0
keywords:
- ErrorItem. errorcontext-Windows-Media Player
topic_type:
- apiref
api_name:
- ErrorItem.errorContext
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9b9ed91d34645f08e7d3d28860ced9ca51420dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360289"
---
# <a name="erroritemerrorcontext"></a>ErrorItem. errorcontext

Die **errorcontext** -Eigenschaft ruft einen Wert ab, der den Kontext des Fehlers angibt.

``` syntax
player.error.item(
        index
        ).errorContext
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zeichenfolge** , die den Fehler Kontext Code darstellt.

## <a name="remarks"></a>Bemerkungen

Der Fehler Kontext sind Informationen, die von Microsoft verwendet werden, um zusätzliche Informationen für den technischen Support zu erhalten.

**Windows Media Player 10 Mobile:** Diese Eigenschaft gibt immer eine leere Zeichenfolge zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/>                               |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ErrorItem-Objekt**](erroritem-object.md)
</dt> </dl>

 

 





