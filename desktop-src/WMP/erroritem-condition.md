---
title: ErrorItem. Condition
description: Die Condition-Eigenschaft ruft einen Wert ab, der die Bedingung für den Fehler angibt.
ms.assetid: efb54b48-cfaa-479f-9ee6-ce6724dca24c
keywords:
- ErrorItem. Condition-Windows-Media Player
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
ms.openlocfilehash: c498e7479a7a3e067dea2d8a562800351effd672
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373938"
---
# <a name="erroritemcondition"></a>ErrorItem. Condition

Die **Condition** -Eigenschaft ruft einen Wert ab, der die Bedingung für den Fehler angibt.

``` syntax
player.error.item(
        index
        ).condition
      
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**), die den Bedingungs Code darstellt.

## <a name="remarks"></a>Bemerkungen

Der Bedingungs Code ist ein Wert, der von Microsoft verwendet wird, um zusätzliche Informationen für die Mitarbeiter des technischen Supports bereitzustellen.

**Windows Media Player 10 Mobile:** Diese Eigenschaft gibt immer 0 (null) zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9 oder höher.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ErrorItem-Objekt**](erroritem-object.md)
</dt> </dl>

 

 





