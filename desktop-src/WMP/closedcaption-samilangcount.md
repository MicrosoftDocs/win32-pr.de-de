---
title: Closedcaption. samilangcount
description: Die samilangcount-Eigenschaft ruft die Anzahl der Sprachen ab, die von der aktuellen Sami-Datei unterstützt werden.
ms.assetid: ad2e776a-b430-46ee-9705-18d279e8715e
keywords:
- Closedcaption. samilangcount-Fenster Media Player
topic_type:
- apiref
api_name:
- ClosedCaption.SAMILangCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57d202ecc8bc18261ac4569f2251201e15911f91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359310"
---
# <a name="closedcaptionsamilangcount"></a>Closedcaption. samilangcount

Die **samilangcount** -Eigenschaft ruft die Anzahl der Sprachen ab, die von der aktuellen Sami-Datei unterstützt werden.

``` syntax
player.closedCaption.SAMILangCount
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**).

## <a name="remarks"></a>Bemerkungen

Diese Methode kann erst verwendet werden, wenn eine digitale Mediendatei (*Player*) geöffnet ist.**openstate** ist gleich 13).

**Windows Media Player 10 Mobile:** Diese Eigenschaft gibt immer 0 (null) zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9 oder höher.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Hinzufügen von Untertiteln zu digitalen Medien**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Closedcaption-Objekt**](closedcaption-object.md)
</dt> <dt>

[**Closedcaption. getsamilangname**](closedcaption-getsamilangname.md)
</dt> <dt>

[**Closedcaption. samilang**](closedcaption-samilang.md)
</dt> </dl>

 

 





