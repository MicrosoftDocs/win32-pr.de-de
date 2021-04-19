---
title: Closedcaption. samistylecount
description: Die samistylecount-Eigenschaft ruft die Anzahl der Stile ab, die von der aktuellen Sami-Datei unterstützt werden.
ms.assetid: 57a85e5d-1598-4cb3-b47d-a6d8f22adfff
keywords:
- Closedcaption. samistylecount-Fenster Media Player
topic_type:
- apiref
api_name:
- ClosedCaption.SAMIStyleCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ab48fc6660065da1635b58b67784f2ab0ff91b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367548"
---
# <a name="closedcaptionsamistylecount"></a>Closedcaption. samistylecount

Die **samistylecount** -Eigenschaft ruft die Anzahl der Stile ab, die von der aktuellen Sami-Datei unterstützt werden.

``` syntax
player.closedCaption.SAMIStyleCount
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

[**Closedcaption. getsamistylename**](closedcaption-getsamistylename.md)
</dt> <dt>

[**Closedcaption. samistyle**](closedcaption-samistyle.md)
</dt> </dl>

 

 





