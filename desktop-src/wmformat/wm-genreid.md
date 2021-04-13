---
title: WM/GenreID
description: Das WM/GenreID-Attribut enthält einen Genre Bezeichner, der mit dem Inhalt des TCON-Tags in "ID3v2" kompatibel ist.
ms.assetid: 2f2a87f7-ba2d-465a-a36b-a8f58b5dd2d0
keywords:
- WM/GenreID-Windows Media-Format
topic_type:
- apiref
api_name:
- WM/GenreID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a3b25dffe69471f47eaf20124af48141835540f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389342"
---
# <a name="wmgenreid"></a>WM/GenreID

Das **WM/GenreID-** Attribut enthält einen Genre Bezeichner, der mit dem Inhalt des TCON-Tags in "ID3v2" kompatibel ist. Dies sollte die Genre-ID in Klammern enthalten, optional gefolgt von einer Optimierung, die das Genre beschreibt. Weitere Informationen finden Sie in der Spezifikation "ID3v2".

## <a name="global-constant"></a>Globale Konstante

g \_ wszwmgenreid

## <a name="data-type"></a>Datentyp

**WMT \_ - \_ Typzeichenfolge**

## <a name="remarks"></a>Bemerkungen

Das bevorzugte Attribut zum Angeben eines Genres ist [**WM/Genre**](wm-genre.md). Verwenden Sie diese Einstellung für dieses Attribut.

Wenn Sie in einer MP3-Datei entweder **WM/Genre** oder **WM/GenreID** ändern, wird das andere Attribut entsprechend geändert.

### <a name="example"></a>Beispiel



| Dateityp | Beispielwert   |
|-----------|-----------------|
| Audio     | "(4) Euro Disco" |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




