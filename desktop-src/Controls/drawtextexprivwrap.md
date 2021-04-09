---
title: Drawtextexprivwrap-Funktion
description: Zeichnet formatierten Text im angegebenen Rechteck. Diese Funktion umschließt einen aufzurufenden drawtextex-Befehl.
ms.assetid: 3212282c-1adb-4f7e-b4d7-7d833b26ac60
keywords:
- Windows-Steuerelemente der drawtextexprivwrap-Funktion
topic_type:
- apiref
api_name:
- DrawTextExPrivWrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eba496a121af3ba88ed24ab6c9c7834c90153ec0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957189"
---
# <a name="drawtextexprivwrap-function"></a>Drawtextexprivwrap-Funktion

\[**Drawtextexprivwrap** ist über Windows XP mit Service Pack 2 (SP2) verfügbar. Sie wird möglicherweise in nachfolgenden Versionen geändert oder ist nicht verfügbar. Es wird empfohlen, stattdessen [**drawtextex**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) direkt zu verwenden.\]

Zeichnet formatierten Text im angegebenen Rechteck. Diese Funktion umschließt einen aufzurufenden [**drawtextex**](/windows/desktop/api/winuser/nf-winuser-drawtextexa)-Befehl.

## <a name="syntax"></a>Syntax


```C++
int WINAPI DrawTextExPrivWrap(
  _In_    HDC              hdc,
  _Inout_ LPTSTR           lpchText,
  _In_    int              cchText,
  _Inout_ LPRECT           lprc,
  _In_    UINT             dwDTFormat,
  _In_    LPDRAWTEXTPARAMS lpDTParams
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hdc* \[ in\]
</dt> <dd>

Typ: **[ **hdc**](/windows/desktop/WinProg/windows-data-types)**

Ein Handle für den Gerätekontext, in dem gezeichnet werden soll.

</dd> <dt>

*lpchtext* \[ in, out\]
</dt> <dd>

Typ: **[ **LPTSTR**](/windows/desktop/WinProg/windows-data-types)**

Ein Zeiger auf einen Puffer, der den zu zeichnenden Text enthält. Wenn der *cchtext* -Parameter-1 ist, muss die Zeichenfolge mit Null beendet werden.

Wenn *dwdtformat* dt \_ modifystring enthält, kann die Funktion dieser Zeichenfolge bis zu vier zusätzliche Zeichen hinzufügen. Der Puffer, der die Zeichenfolge enthält, sollte groß genug sein, um diese zusätzlichen Zeichen aufnehmen zu können.

</dd> <dt>

*cchtext* \[ in\]
</dt> <dd>

Typ: **int**

Die Länge der Zeichenfolge, auf die von *lpchtext* verwiesen wird. Wenn *cchtext* -1 ist, wird angenommen, dass der *lpchtext* -Parameter ein Zeiger auf eine mit NULL endende Zeichenfolge ist, und [**drawtextex**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) berechnet automatisch die Zeichen Anzahl.

</dd> <dt>

*LPRC* \[ in, out\]
</dt> <dd>

Typ: **lprect**

Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die das Rechteck in logischen Koordinaten enthält, in dem der Text formatiert werden soll.

</dd> <dt>

*dwdtformat* \[ in\]
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Die Formatierungsoptionen. Eine umfassende Liste der Optionen finden Sie in der Dokumentation zu [**drawtextex**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) .

</dd> <dt>

*lpdtparametriams* \[ in\]
</dt> <dd>

Typ: **lpdrawtextparametriams**

Ein Zeiger auf eine [**drawtextparameams**](/windows/win32/api/winuser/ns-winuser-drawtextparams) -Struktur, die zusätzliche Formatierungsoptionen angibt. Dieser Parameter kann **NULL** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **int**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert die Texthöhe in logischen Einheiten. Wenn **dt \_ vCenter** oder **dt \_ Bottom** angegeben ist, ist der Rückgabewert der Offset vom **obersten** Member von *LPRC* bis zum unteren Rand des gezeichneten Texts.

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.

## <a name="remarks"></a>Bemerkungen

**Drawtextexprivwrap** wird nicht nach Name exportiert oder in einer öffentlichen Header Datei deklariert. Um es zu verwenden, müssen Sie [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) und Request Ordnungszahl 416 aus ComCtl32.dll verwenden, um einen Funktionszeiger zu erhalten.

Weitere Hinweise finden Sie unter [**drawtextex**](/windows/desktop/api/winuser/nf-winuser-drawtextexa).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (Version 6,0 oder höher)</dt> </dl> |



 

