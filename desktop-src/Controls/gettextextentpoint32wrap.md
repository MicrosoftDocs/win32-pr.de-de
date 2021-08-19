---
title: GetTextExtentPoint32Wrap-Funktion
description: Berechnet die Breite und Höhe der angegebenen Textzeichenfolge. Diese Funktion umschließt einen Aufruf von GetTextExtentPoint.
ms.assetid: 156f9344-6071-451c-94c7-63f369a5573a
keywords:
- GetTextExtentPoint32Wrap-Funktion Windows Controls
topic_type:
- apiref
api_name:
- GetTextExtentPoint32Wrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0217d1708764ec33dd76ea35ff330f0d411697b5e9be3a6bd148377002a1f127
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047210"
---
# <a name="gettextextentpoint32wrap-function"></a>GetTextExtentPoint32Wrap-Funktion

\[**GetTextExtentPoint32Wrap** ist über Windows XP mit Service Pack 2 (SP2) verfügbar. Sie kann in nachfolgenden Versionen geändert oder nicht verfügbar sein. Es wird empfohlen, [**GetTextExtentPoint stattdessen direkt**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa) zu verwenden.\]

Berechnet die Breite und Höhe der angegebenen Textzeichenfolge. Diese Funktion umschließt einen Aufruf von [**GetTextExtentPoint.**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa)

## <a name="syntax"></a>Syntax


```C++
BOOL GetTextExtentPoint32Wrap(
  _In_  HDC     hdc,
  _In_  LPCTSTR lpString,
  _In_  UINT    cbCount,
  _Out_ LPSIZE  lpSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hdc* \[ In\]
</dt> <dd>

Typ: **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**

Ein Handle für den Gerätekontext.

</dd> <dt>

*lpString* \[ In\]
</dt> <dd>

Typ: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Ein Zeiger auf einen Puffer, der den zu zeichneten Text enthält. Die Zeichenfolge muss nicht mit 0 (null) beendet werden, da *cbCount* die Länge der Zeichenfolge angibt.

</dd> <dt>

*cbCount* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Die Länge der Zeichenfolge in Bytes, auf die *lpString zeigt.*

</dd> <dt>

*lpSize* \[ out\]
</dt> <dd>

Typ: **LPSIZE**

Diese Methode gibt einen Zeiger auf eine [**SIZE-Struktur**](/previous-versions//dd145106(v=vs.85)) mit den Dimensionen der Zeichenfolge in logischen Einheiten zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück. andernfalls 0.

Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.

## <a name="remarks"></a>Bemerkungen

**GetTextExtentPoint32Wrap** wird nicht nach Namen exportiert oder in einer öffentlichen Headerdatei deklariert. Um sie zu verwenden, müssen Sie [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden und ordinal 420 von ComCtl32.dll abrufen, um einen Funktionszeiger zu erhalten.

Weitere Hinweise finden Sie unter [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                            |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (Version 5.81 oder höher)</dt> </dl> |



 

