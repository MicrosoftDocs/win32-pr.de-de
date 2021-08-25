---
title: WM/GenreID
description: Das WM/GenreID-Attribut enthält einen Genrebezeichner, der mit dem Inhalt des TCON-Tags in ID3v2 kompatibel ist.
ms.assetid: 2f2a87f7-ba2d-465a-a36b-a8f58b5dd2d0
keywords:
- WM/GenreID windows Media Format
topic_type:
- apiref
api_name:
- WM/GenreID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9355a16196d386d4ec3f2a98588eced2981f8e62a3df96a9c0d094551a10a733
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930440"
---
# <a name="wmgenreid"></a>WM/GenreID

Das **WM/GenreID-Attribut** enthält einen Genrebezeichner, der mit dem Inhalt des TCON-Tags in ID3v2 kompatibel ist. Diese sollte die Genre-ID in Klammern enthalten, optional gefolgt von einer Verfeinerung, die das Genre weiter beschreibt. Weitere Informationen finden Sie in der ID3v2-Spezifikation.

## <a name="global-constant"></a>Globale Konstante

g \_ wszWMGenreID

## <a name="data-type"></a>Datentyp

**\_WMT-TYPZEICHENFOLGE \_**

## <a name="remarks"></a>Hinweise

Das bevorzugte Attribut zum Angeben eines Genre ist [**WM/Genre**](wm-genre.md). Verwenden Sie es vor diesem Attribut.

Wenn Sie entweder **WM/Genre oder** **WM/GenreID** in einer MP3-Datei ändern, wird das andere Attribut geändert, um eine Übereinstimmung zu finden.

### <a name="example"></a>Beispiel



| Dateityp | Beispielwert   |
|-----------|-----------------|
| Audio     | "(4) Eurodisco" |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




