---
title: GetTextExtentPoint32Wrap-Funktion
description: Berechnet die Breite und Höhe der angegebenen Text Zeichenfolge. Diese Funktion umschließt einen Aufrufen von GetTextExtentPoint.
ms.assetid: 156f9344-6071-451c-94c7-63f369a5573a
keywords:
- GetTextExtentPoint32Wrap-Funktion Windows-Steuerelemente
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
ms.openlocfilehash: b6a0db92ad019950cf8be0a72260da75acc06779
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740112"
---
# <a name="gettextextentpoint32wrap-function"></a>GetTextExtentPoint32Wrap-Funktion

\[**GetTextExtentPoint32Wrap** ist über Windows XP mit Service Pack 2 (SP2) verfügbar. Sie wird möglicherweise in nachfolgenden Versionen geändert oder ist nicht verfügbar. Es wird empfohlen, stattdessen [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa) direkt zu verwenden.\]

Berechnet die Breite und Höhe der angegebenen Text Zeichenfolge. Diese Funktion umschließt einen Aufrufen von [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa).

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

*hdc* \[ in\]
</dt> <dd>

Typ: **[ **hdc**](/windows/desktop/WinProg/windows-data-types)**

Ein Handle für den Gerätekontext.

</dd> <dt>

*lpString* \[ in\]
</dt> <dd>

Typ: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Ein Zeiger auf einen Puffer, der den Text enthält, der gezeichnet werden soll. Die Zeichenfolge muss nicht mit 0 (null) beendet werden, da *cbcount* die Länge der Zeichenfolge angibt.

</dd> <dt>

*cbcount* \[ in\]
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Die Länge der Zeichenfolge in Bytes, auf die von *lpString* verwiesen wird.

</dd> <dt>

*lpsize* \[ vorgenommen\]
</dt> <dd>

Typ: **lpsize**

Wenn diese Methode zurückgegeben wird, enthält Sie einen Zeiger auf eine [**Größen**](/previous-versions//dd145106(v=vs.85)) Struktur, die die Dimensionen der Zeichenfolge in logischen Einheiten enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück. andernfalls 0.

Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.

## <a name="remarks"></a>Bemerkungen

**GetTextExtentPoint32Wrap** wird nicht nach Name exportiert oder in einer öffentlichen Header Datei deklariert. Um es zu verwenden, müssen Sie [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) und Request Ordnungszahl 420 aus ComCtl32.dll verwenden, um einen Funktionszeiger zu erhalten.

Weitere Hinweise finden Sie unter [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                            |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (Version 5,81 oder höher)</dt> </dl> |



 

