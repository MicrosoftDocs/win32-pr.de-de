---
title: Controls. audiolanguagecount
description: Die audiolanguagecount-Eigenschaft ruft die Anzahl der unterstützten Audiosprachen ab.
ms.assetid: a6dda8bf-db8c-4e97-9277-5a23dfa93156
keywords:
- Steuerelemente. audiolanguagecount Windows Media Player
topic_type:
- apiref
api_name:
- Controls.audioLanguageCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09193eb19580d9456f25ea336fe68b8d21e06bae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370215"
---
# <a name="controlsaudiolanguagecount"></a>Controls. audiolanguagecount

Die **audiolanguagecount** -Eigenschaft ruft die Anzahl der unterstützten Audiosprachen ab.

``` syntax
player.controls.audioLanguageCount
      
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**).

## <a name="remarks"></a>Bemerkungen

Bei Windows Media-basierten Inhalten unterstützen Eigenschaften und Methoden im Zusammenhang mit der Sprachauswahl nur eine einzelne Ausgabe.

**Windows Media Player 10 Mobile:** Diese Eigenschaft gibt immer 1 zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9 oder höher.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Controls-Objekt**](controls-object.md)
</dt> <dt>

[**Controls. currentaudiolanguage**](controls-currentaudiolanguage.md)
</dt> <dt>

[**Controls. currentaudiolanguageindex**](controls-currentaudiolanguageindex.md)
</dt> <dt>

[**Controls. getaudiolanguagedescription**](controls-getaudiolanguagedescription.md)
</dt> <dt>

[**Controls. getaudiolanguageid**](controls-getaudiolanguageid.md)
</dt> <dt>

[**Controls. getlanguagename**](controls-getlanguagename.md)
</dt> </dl>

 

 





