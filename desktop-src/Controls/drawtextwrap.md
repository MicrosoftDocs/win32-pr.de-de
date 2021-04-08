---
title: Drawtextwrap-Funktion
description: Zeichnet formatierten Text im angegebenen Rechteck. Er formatiert den Text gemäß der angegebenen Methode (erweitert Registerkarten, rechtfertigt Zeichen, Zeilenumbruch usw.). Diese Funktion umschließt einen aufzurufenden DrawText-Befehl.
ms.assetid: 28ab4c5e-3b8f-49e8-b072-500ba1916caf
keywords:
- Windows-Steuerelemente der drawtextwrap-Funktion
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
ms.openlocfilehash: cfc5eb707b4016a592ad339223e0f32ab21d4a29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949469"
---
# <a name="drawtextwrap-function"></a>Drawtextwrap-Funktion

\[**Drawtextwrap** ist über Windows XP mit Service Pack 2 (SP2) verfügbar. Sie wird möglicherweise in nachfolgenden Versionen geändert oder ist nicht verfügbar. Es wird empfohlen, stattdessen [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) direkt zu verwenden.\]

Zeichnet formatierten Text im angegebenen Rechteck. Er formatiert den Text gemäß der angegebenen Methode (erweitert Registerkarten, rechtfertigt Zeichen, Zeilenumbruch usw.). Diese Funktion umschließt einen aufzurufenden [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext)-Befehl.

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

*hdc* \[ in\]
</dt> <dd>

Typ: **[ **hdc**](/windows/desktop/WinProg/windows-data-types)**

Ein Handle für den Gerätekontext.

</dd> <dt>

*lpString* \[ in, out\]
</dt> <dd>

Typ: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Ein Zeiger auf einen Puffer, der den zu zeichnenden Text enthält. Wenn der *nCount* -Parameter-1 ist, muss die Zeichenfolge mit Null beendet werden.

Wenn " *Uformat* " dt \_ modifystring enthält, kann die Funktion dieser Zeichenfolge bis zu vier zusätzliche Zeichen hinzufügen. Der Puffer, der die Zeichenfolge enthält, sollte groß genug sein, um diese zusätzlichen Zeichen aufnehmen zu können.

</dd> <dt>

*nCount* \[ in\]
</dt> <dd>

Typ: **int**

Die Länge der Zeichenfolge, auf die von *lpString* verwiesen wird. Wenn *nCount* den Wert-1 hat, wird angenommen, dass der *lpString* -Parameter ein Zeiger auf eine auf NULL endende Zeichenfolge ist, und [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) berechnet automatisch die Zeichen Anzahl.

</dd> <dt>

*lprect* \[ in, out\]
</dt> <dd>

Typ: **lprect**

Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die das Rechteck in logischen Koordinaten enthält, in dem der Text formatiert werden soll.

</dd> <dt>

*Uformat* \[ in\]
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Die Formatierungsoptionen. Eine vollständige Liste der Optionen finden Sie in der Dokumentation zu [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) .

</dd> <dt>

*lpdtparametriams* \[ in\]
</dt> <dd>

Typ: **lpdrawtextparametriams**

Ein Zeiger auf eine [**drawtextparameams**](/windows/win32/api/winuser/ns-winuser-drawtextparams) -Struktur, die zusätzliche Formatierungsoptionen angibt. Dieser Parameter kann **NULL** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **int**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert die Texthöhe in logischen Einheiten. Wenn **dt \_ vCenter** oder **dt \_ Bottom** angegeben ist, ist der Rückgabewert der Offset vom **obersten** Member von *LPRC* bis zum unteren Rand des gezeichneten Texts, wenn die Funktion fehlschlägt, der Rückgabewert 0 (null) ist.

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.

## <a name="remarks"></a>Bemerkungen

**Drawtextwrap** wird nicht nach Name exportiert oder in einem öffentlichen Header deklariert. Um es zu verwenden, müssen Sie [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) und Request Ordnungszahl 415 aus ComCtl32.dll verwenden, um einen Funktionszeiger zu erhalten.

Weitere Hinweise finden Sie unter [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (Version 6,0 oder höher)</dt> </dl> |



 

