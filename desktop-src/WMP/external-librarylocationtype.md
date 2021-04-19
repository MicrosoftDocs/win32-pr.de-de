---
title: Extern. librarylocationtype
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | Extern. librarylocationtype
ms.assetid: aaf20147-8331-40bd-a5cd-5ee9b8e2d022
keywords:
- Externe. librarylocationtype-Windows-Media Player
topic_type:
- apiref
api_name:
- External.libraryLocationType
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2c2f14940a2ad41bed24493396e2bacfba2f0a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360280"
---
# <a name="externallibrarylocationtype"></a>Extern. librarylocationtype

> [!Note]  
> In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Die **librarylocationtype** -Eigenschaft ruft eine [Bibliotheks Speicherort Konstante](library-location-constants.md) ab, die den Typ der aktuellen Ansicht in Windows Media Player angibt.

``` syntax
window.external.libraryLocationType
      
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zeichenfolge** , die eine der Bibliotheks Speicherort Konstanten enthält.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft funktioniert in Kombination mit der [externen. librarylocationid](external-librarylocationid.md) -Eigenschaft. Nehmen wir beispielsweise an, dass **librarylocationtype** gleich cpalbumid und **librarylocationid** gleich 3 ist. Dies bedeutet, dass die aktuelle Ansicht in Windows Media Player das Album mit der ID 3 anzeigt. Weitere Informationen zur kennzeichnen von Ansichten von Online Store-Inhalten durch Windows Media Player finden Sie unter [Standort und ausgewähltes Element](location-and-selected-item.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Externes Objekt für den Typ 1-Online Speicher**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**Extern. librarylocationid**](external-librarylocationid.md)
</dt> <dt>

[**Speicherort und ausgewähltes Element**](location-and-selected-item.md)
</dt> </dl>

 

 





