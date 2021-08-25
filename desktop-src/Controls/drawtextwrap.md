---
title: DrawTextWrap-Funktion
description: Zeichnet formatierten Text im angegebenen Rechteck. Der Text wird gemäß der angegebenen Methode formatiert (Erweitern von Registerkarten, Rechtfertigen von Zeichen, Zeilenbruch usw.). Diese Funktion umschließt einen Aufruf von DrawText.
ms.assetid: 28ab4c5e-3b8f-49e8-b072-500ba1916caf
keywords:
- DrawTextWrap-Funktion Windows-Steuerelemente
topic_type:
- apiref
api_name:
- DrawTextWrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcbd504955b6ae772ffb3db7bc4cc0223215d6d9ecf880fe7d7e3aa359c992ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878290"
---
# <a name="drawtextwrap-function"></a>DrawTextWrap-Funktion

\[**DrawTextWrap** ist über Windows XP mit Service Pack 2 (SP2) verfügbar. Er kann in nachfolgenden Versionen geändert oder nicht verfügbar sein. Stattdessen wird empfohlen, [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) direkt zu verwenden.\]

Zeichnet formatierten Text im angegebenen Rechteck. Der Text wird gemäß der angegebenen Methode formatiert (Erweitern von Registerkarten, Rechtfertigen von Zeichen, Zeilenbruch usw.). Diese Funktion umschließt einen Aufruf von [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext).

## <a name="syntax"></a>Syntax


```C++
int WINAPI DrawTextWrap(
  _In_    HDC              hdc,
  _Inout_ LPCTSTR          lpString,
  _In_    int              nCount,
  _Inout_ LPRECT           lpRect,
  _In_    UINT             uFormat,
  _In_    LPDRAWTEXTPARAMS lpDTParams
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hdc* \[ In\]
</dt> <dd>

Typ: **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**

Ein Handle für den Gerätekontext.

</dd> <dt>

*lpString* \[ in, out\]
</dt> <dd>

Typ: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Ein Zeiger auf einen Puffer, der den zu zeichnende Text enthält. Wenn der *nCount-Parameter* -1 ist, muss die Zeichenfolge NULL-terminiert sein.

Wenn *uFormat* DT \_ MODIFYSTRING enthält, kann die Funktion dieser Zeichenfolge bis zu vier zusätzliche Zeichen hinzufügen. Der Puffer, der die Zeichenfolge enthält, sollte groß genug sein, um diese zusätzlichen Zeichen aufzunehmen.

</dd> <dt>

*nCount* \[ In\]
</dt> <dd>

Typ: **int**

Die Länge der Zeichenfolge, auf die *lpString* zeigt. Wenn *nCount* -1 ist, wird davon ausgegangen, dass der *lpString-Parameter* ein Zeiger auf eine auf NULL endende Zeichenfolge ist, und [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) berechnet die Zeichenanzahl automatisch.

</dd> <dt>

*lpRect* \[ in, out\]
</dt> <dd>

Typ: **LPRECT**

Ein Zeiger auf eine [**RECT-Struktur,**](/previous-versions//dd162897(v=vs.85)) die das Rechteck in logischen Koordinaten enthält, in dem der Text formatiert werden soll.

</dd> <dt>

*uFormat* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Die Formatierungsoptionen. Eine vollständige Liste der Optionen finden Sie in der Dokumentation zu [**DrawText.**](/windows/desktop/api/winuser/nf-winuser-drawtext)

</dd> <dt>

*lpDTParams* \[ In\]
</dt> <dd>

Typ: **LPDRAWTEXTPARAMS**

Ein Zeiger auf eine [**DRAWTEXTPARAMS-Struktur,**](/windows/win32/api/winuser/ns-winuser-drawtextparams) die zusätzliche Formatierungsoptionen angibt. Dieser Parameter kann **NULL** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **int**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert die Texthöhe in logischen Einheiten. Wenn **DT \_ VCENTER** oder **DT \_ BOTTOM** angegeben wird, ist der Rückgabewert der Offset vom **obersten** Member von *lprc* bis zum unteren Rand des gezeichneten Texts. Wenn die Funktion fehlschlägt, ist der Rückgabewert 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.

## <a name="remarks"></a>Bemerkungen

**DrawTextWrap** wird nicht anhand des Namens exportiert oder in einem öffentlichen Header deklariert. Um es zu verwenden, müssen Sie [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden und Ordnungszahl 415 von ComCtl32.dll anfordern, um einen Funktionszeiger abzurufen.

Weitere Hinweise finden Sie unter [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (Version 6.0 oder höher)</dt> </dl> |



 

