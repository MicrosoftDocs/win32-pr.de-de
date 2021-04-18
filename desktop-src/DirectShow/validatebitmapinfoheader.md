---
description: Die validatebitmapinfoheader-Funktion überprüft eine BITMAPINFOHEADER-Struktur auf bestimmte häufige Fehler, die Pufferüberläufe oder ganzzahlige über Läufe verursachen können.
ms.assetid: a797c286-ed77-437f-9ec1-1ef3a189bf62
title: Validatebitmapinfoheader-Funktion (checkbmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateBitmapInfoHeader
api_type:
- HeaderDef
api_location:
- checkbmi.h
ms.openlocfilehash: c7242778a2ff16414b07f887dc1e71a1547a88e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364480"
---
# <a name="validatebitmapinfoheader-function"></a>Validatebitmapinfoheader-Funktion

Die- `ValidateBitmapInfoHeader` Funktion überprüft eine [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur auf bestimmte häufige Fehler, die Pufferüberläufe oder ganzzahlige über Läufe verursachen können.

> [!Note]  
> Diese Funktion garantiert nicht, dass die [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur gültig ist oder dass der Code, der die Struktur verwendet, sicher ist.

 

## <a name="syntax"></a>Syntax


```C++
BOOL ValidateBitmapInfoHeader(
   const BITMAPINFOHEADER *pbmi,
         DWORD            cbSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbmi* 
</dt> <dd>

Zeiger auf die zu validierende [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur.

</dd> <dt>

*CBSIZE* 
</dt> <dd>

Größe des Speicherblocks, der die Struktur enthält (in Bytes).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen booleschen Wert zurück. Wenn der Wert **false** ist, ist die [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur ungültig.

## <a name="remarks"></a>Bemerkungen

Diese Funktion schützt vor den folgenden Fehlern:

-   Arithmetischer Überlauf in der Struktur Größe oder einer ungültigen Struktur Größe.
-   Ungültiger Wert für den **biclrused** -Member.
-   Arithmetischer Überlauf in der Bildgröße (**bisizeimage**).
-   Ungültige Werte für die Bildgröße (**bisizeimage**) für RGB-Formate.

Die-Funktion prüft nicht, ob die Struktur ein gültiges Videoformat beschreibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Checkbmi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Video-und Bildfunktionen](video-and-image-functions.md)
</dt> </dl>

 

 




