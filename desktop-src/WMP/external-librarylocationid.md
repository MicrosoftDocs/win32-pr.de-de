---
title: Extern. librarylocationid
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | Extern. librarylocationid
ms.assetid: 9a9bea89-c05c-4759-be22-86588bbeca2c
keywords:
- Externe. librarylocationid-Windows-Media Player
topic_type:
- apiref
api_name:
- External.libraryLocationID
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89f411ad8575bc7419cf9300d1aab46073ee869c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355888"
---
# <a name="externallibrarylocationid"></a>Extern. librarylocationid

> [!Note]  
> In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Die **librarylocationid** -Eigenschaft ruft den Bezeichner des bestimmten Medien Elements ab, das momentan in der Ansicht des Players angezeigt wird.

``` syntax
window.external.libraryLocationID
      
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zeichenfolge**.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft funktioniert in Kombination mit der Eigenschaft " [extern. librarylocationtype](external-librarylocationtype.md) ". Nehmen wir beispielsweise an, dass **librarylocationtype** gleich cpalbumid und **librarylocationid** gleich 3 ist. Dies bedeutet, dass die aktuelle Ansicht in Windows Media Player das Album mit der ID 3 anzeigt. Weitere Informationen zur kennzeichnen von Ansichten von Online Store-Inhalten durch Windows Media Player finden Sie unter [Standort und ausgewähltes Element](location-and-selected-item.md).

Bestimmte Sichten in Windows-Media Player sind einem bestimmten Medien Element zugeordnet. Wenn die aktuelle Ansicht z. b. ein einzelnes Album darstellt, ist **librarylocationtype** gleich cpalbumid, und **librarylocationid** ist die ID des Albums. Andere Sichten sind keinem bestimmten Medien Element zugeordnet. Wenn die aktuelle Ansicht z. b. Alle Alben darstellt, ist **librarylocationtype** gleich allcpalbumids, aber es gibt keinen sinnvollen Wert, der **librarylocationid** zugewiesen werden kann. In Fällen, in denen die **librarylocationid** -Eigenschaft keinen sinnvollen Wert hat, entspricht Sie der leeren Zeichenfolge.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Externes Objekt für den Typ 1-Online Speicher**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**Extern. librarylocationtype**](external-librarylocationtype.md)
</dt> <dt>

[**Speicherort und ausgewähltes Element**](location-and-selected-item.md)
</dt> </dl>

 

 





