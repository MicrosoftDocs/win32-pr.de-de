---
description: Verwendet eine von IShellFolder::GetDisplayNameOf zurückgegebene STRRET-Struktur, konvertiert sie in eine Zeichenfolge und platziert das Ergebnis in einen Puffer.
title: StrRetToStrN-Funktion
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
ms.openlocfilehash: 50295d712e539c94f10a708674cea595a47ae4e0
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841031"
---
# <a name="strrettostrn-function"></a>StrRetToStrN-Funktion

Verwendet eine [**strret-Struktur,**](/windows/desktop/api/Shtypes/ns-shtypes-strret) die von [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof)zurückgegeben wird, konvertiert sie in eine Zeichenfolge und platziert das Ergebnis in einen Puffer.

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

*pszOut* \[ out\]
</dt> <dd>

Typ: **LPTSTR**

Puffer zum Halten des Anzeigenamens. Sie wird als auf NULL beendete Zeichenfolge zurückgegeben. Wenn *cchOut* zu klein ist, wird der Name abgeschnitten, damit er passt.

</dd> <dt>

*cchOut* \[ In\]
</dt> <dd>

Typ: **UINT**

Größe von *pszOut* in Zeichen. Wenn *cchOut* zu klein ist, wird die Zeichenfolge abgeschnitten, damit sie passt.

</dd> <dt>

*pStrRet* \[ in, out\]
</dt> <dd>

Typ: **LPSTRRET**

Zeiger auf eine [**STRRET-Struktur.**](/windows/desktop/api/Shtypes/ns-shtypes-strret) Wenn die Funktion zurückgegeben wird, ist dieser Zeiger nicht mehr gültig.

</dd> <dt>

*pidl* \[ In\]
</dt> <dd>

Typ: **LPJSMIDLIST**

Zeiger auf die [**ITEMIDLIST-Struktur des**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) Elements.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **BOOL**

**TRUE** für Erfolg, **FALSE** für Fehler.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Ab Shell32.dll Version 5.0 entspricht das Aufrufen dieser Funktion dem Aufruf von [**StrRetToBuf.**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa)

 

**StrRetToStrN** wird nicht anhand des Namens exportiert. Um es zu verwenden, müssen Sie [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden und Ordnungszahl 96 von Shell32.dll anfordern, um einen Funktionszeiger abzurufen.

Wenn der **uType-Member** der -Struktur, auf die *pStrRet* zeigt, auf **STRRET \_ WSTR** festgelegt ist, wird der **pOleStr-Member** dieser Struktur bei der Rückgabe freigegeben.

Beachten Sie, dass diese Funktion nicht aus Shlwapi.dll, sondern aus Shell32.dll exportiert wird. Sie ist auch in "Shlobj.h" und nicht in "Shlwapi.h" enthalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4.71 oder höher)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**StrRetToStr**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra)
</dt> <dt>

[**StrRetToBuf**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa)
</dt> </dl>

 

 
