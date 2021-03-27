---
description: 'Nimmt eine von IShellFolder:: GetDisplayNameOf zurückgegebene "strinret"-Struktur, konvertiert sie in eine Zeichenfolge und platziert das Ergebnis in einem Puffer.'
title: "\"Strauch\"-Funktion"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StrRetToStrN
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: a816fb5f-8320-4b63-a85d-dd4c59596ead
ms.openlocfilehash: 89a8d991e22e8615456bd8d4690c046ec0d325d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995174"
---
# <a name="strrettostrn-function"></a>"Strauch"-Funktion

Nimmt eine von [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof)zurückgegebene " [**strinret**](/windows/desktop/api/Shtypes/ns-shtypes-strret) "-Struktur, konvertiert sie in eine Zeichenfolge und platziert das Ergebnis in einem Puffer.

## <a name="syntax"></a>Syntax


```C++
BOOL StrRetToStrN(
  _Out_   LPTSTR        pszOut,
  _In_    UINT          cchOut,
  _Inout_ LPSTRRET      pStrRet,
  _In_    LPCITEMIDLIST pidl
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pszout* \[ vorgenommen\]
</dt> <dd>

Typ: **LPTSTR**

Puffer, der den anzeigen Amen enthalten soll. Sie wird als eine NULL-terminierte Zeichenfolge zurückgegeben. Wenn das *cchout* zu klein ist, wird der Name abgeschnitten, damit er passt.

</dd> <dt>

*cchout* \[ in\]
</dt> <dd>

Typ: **uint**

Größe von *pszout* in Zeichen. Wenn das *cchout* zu klein ist, wird die Zeichenfolge gekürzt, damit Sie passt.

</dd> <dt>

*pstrauret* \[ in, out\]
</dt> <dd>

Typ: **lpstrauret**

Zeiger auf eine " [**strinret**](/windows/desktop/api/Shtypes/ns-shtypes-strret) "-Struktur. Wenn die Funktion zurückgegeben wird, ist dieser Zeiger nicht mehr gültig.

</dd> <dt>

*PIDL* \[ in\]
</dt> <dd>

Typ: **lpcitemittellist**

Ein Zeiger auf die [**itemittellist**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) -Struktur des Elements.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **bool**

**True** für Erfolg, **false** für Fehler.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Ab Shell32.dll Version 5,0 entspricht das Aufrufen dieser Funktion dem Aufrufen von " [**straurettobuf**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa)".

 

 "" "" "" "" "" ". Um es zu verwenden, müssen Sie [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) und Request Ordnungszahl 96 aus Shell32.dll verwenden, um einen Funktionszeiger zu erhalten.

Wenn das **uType** -Element der Struktur, auf die von *pstrinret* verwiesen wird, auf " **chanret \_ WSTR**" festgelegt ist, wird der **polestr** -Member dieser Struktur bei der Rückgabe freigegeben.

Beachten Sie, dass diese Funktion aus Shell32.dll und nicht Shlwapi.dll exportiert wird. Es ist auch in "shlobj. h" und nicht in "shlwapi. h" enthalten.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4,71 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**"Strauch"**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra)
</dt> <dt>

[**"Stringebuf"**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa)
</dt> </dl>

 

 
