---
title: ExtTextOutWrap-Funktion
description: Zeichnet Text mit der aktuell ausgewählten Schriftart, Hintergrundfarbe und Textfarbe. Sie können optional Dimensionen angeben, die für Clipping, Deckkraft oder beides verwendet werden sollen. Diese Funktion umschließt einen Aufruf von ExtTextOut.
ms.assetid: 0804c231-53f9-4de6-b703-0077cdcebcb5
keywords:
- ExtTextOutWrap-Funktion Windows Controls
topic_type:
- apiref
api_name:
- ExtTextOutWrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 934a8d203cf232a339db46e97783e87c075e5bb949ec5d23e20a7b1874ea6ef2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047270"
---
# <a name="exttextoutwrap-function"></a>ExtTextOutWrap-Funktion

\[**ExtTextOutWrap** ist über Windows XP mit Service Pack 2 (SP2) verfügbar. Sie kann in nachfolgenden Versionen geändert oder nicht verfügbar sein. Stattdessen wird empfohlen, [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) direkt zu verwenden.\]

Zeichnet Text mit der aktuell ausgewählten Schriftart, Hintergrundfarbe und Textfarbe. Sie können optional Dimensionen angeben, die für Clipping, Deckkraft oder beides verwendet werden sollen. Diese Funktion umschließt einen Aufruf von [**ExtTextOut.**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta)

## <a name="syntax"></a>Syntax


```C++
BOOL ExtTextOutWrap(
  _In_       HDC     hdc,
  _In_       int     X,
  _In_       int     Y,
  _In_       UINT    uOptions,
  _In_ const RECT    *lprc,
  _In_       LPCTSTR lpString,
  _In_       UINT    cbCount,
  _In_ const INT     *lpDx
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hdc* \[ In\]
</dt> <dd>

Typ: **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**

Ein Handle für den Gerätekontext.

</dd> <dt>

*X* \[ in\]
</dt> <dd>

Typ: **int**

Die x-Koordinate in logischen Koordinaten des Referenzpunkts, der zum Positionieren der Zeichenfolge verwendet wird.

</dd> <dt>

*Y* \[ in\]
</dt> <dd>

Typ: **int**

Die y-Koordinate in logischen Koordinaten des Referenzpunkts, der zum Positionieren der Zeichenfolge verwendet wird.

</dd> <dt>

*uOptions* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Werte, die angeben, wie das anwendungsdefinierte Rechteck verwendet werden soll. Eine vollständige Liste der Optionen finden Sie unter [**ExtTextOut.**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta)

</dd> <dt>

*lprc* \[ In\]
</dt> <dd>

Typ: **const [**RECT**](/previous-versions//dd162897(v=vs.85)) \***

Ein Zeiger auf eine optionale [**RECT-Struktur,**](/previous-versions//dd162897(v=vs.85)) die die Dimensionen in logischen Koordinaten eines Rechtecks angibt, das für Clipping, Deckkraft oder beides verwendet wird.

</dd> <dt>

*lpString* \[ In\]
</dt> <dd>

Typ: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Ein Zeiger auf einen Puffer, der den zu zeichnenden Text enthält. Die Zeichenfolge muss nicht auf null enden, da *cbCount* die Länge der Zeichenfolge angibt.

</dd> <dt>

*cbCount* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Die Länge der Zeichenfolge in Bytes, auf die *lpString* zeigt.

</dd> <dt>

*lpDx* \[ In\]
</dt> <dd>

Typ: **const [**INT**](/windows/desktop/WinProg/windows-data-types) \***

Ein Zeiger auf ein optionales Array von Werten, das den Abstand zwischen den Ursprüngen benachbarter Zeichenzellen angibt. Beispielsweise trennen *die logischen Einheiten lpDx* \[ x die Ursprünge der \] Zeichenzelle x und der Zeichenzelle (x + 1).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**

Gibt einen Wert ungleich 0 (null) zurück, wenn die Zeichenfolge erfolgreich gezeichnet wurde. Wenn jedoch die ANSI-Version von [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) mit ETO \_ GLYPH INDEX aufgerufen \_ wird, gibt die Funktion **TRUE** zurück, obwohl die Funktion nichts tut.

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.

## <a name="remarks"></a>Bemerkungen

**ExtTextOutWrap** wird nicht anhand des Namens exportiert oder in einer öffentlichen Headerdatei deklariert. Um es zu verwenden, müssen Sie [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden und Ordnungszahl 417 von ComCtl32.dll anfordern, um einen Funktionszeiger abzurufen.

Weitere Hinweise finden Sie unter [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (Version 6.0 oder höher)</dt> </dl> |



 

