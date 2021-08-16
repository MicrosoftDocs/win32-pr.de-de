---
title: Str_GetPtr-Funktion
description: Kopiert eine Zeichenfolge von einem Puffer in einen anderen.
ms.assetid: a3dd55a0-3f8b-4d6c-9956-666bebc3ab8d
keywords:
- Str_GetPtr-Windows Steuerelemente
topic_type:
- apiref
api_name:
- Str_GetPtr
- Str_GetPtrA
- Str_GetPtrW
api_location:
- ComCtl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77c76ad276f6cb6dfc12bc272fbbc86c83617a0d00d36d77cf2ab0ca113811d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919450"
---
# <a name="str_getptr-function"></a>Str \_ GetPtr-Funktion

\[Diese Funktion ist über Windows XP mit Service Pack 2 (SP2) und Windows Server 2003 verfügbar. Sie kann in nachfolgenden Versionen von geändert oder nicht verfügbar Windows.\]

Kopiert eine Zeichenfolge von einem Puffer in einen anderen.

## <a name="syntax"></a>Syntax


```C++
int WINAPI Str_GetPtr(
  _In_    LPCTSTR pszSource,
  _Inout_ LPCSTR  pszDest,
  _In_    int     cchDest
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pszSource* \[ In\]
</dt> <dd>

Typ: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Ein Zeiger auf eine Quellzeichenfolge.

</dd> <dt>

*pszDest* \[ in, out\]
</dt> <dd>

Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Ein Zeiger auf den Zielpuffer. Dieser Wert kann NULL **sein.**

</dd> <dt>

*cchDest* \[ In\]
</dt> <dd>

Typ: **int**

Die Größe von *pszDest* in Zeichen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **int**

Wenn *pszDest* NULL oder *cchDest* 0 (null) ist, gibt die Größe des Puffers in Zeichen zurück, die eine auf **NULL** terminierte Kopie der Zeichenfolge enthalten muss, auf die *pszSource zeigt.*

Wenn *pszDest* nicht NULL **ist,** gibt die Anzahl der erfolgreich kopierten Zeichen zurück, einschließlich des beendenden NULL-Zeichens.

Wenn *pszDest* nicht die gesamte Zeichenfolge enthalten kann, auf die *pszSource* zeigt, werden (*cchDest*-1) Zeichen kopiert, die Zeichenfolge mit NULL-Terminierung und *cchDest* zurückgegeben.

## <a name="remarks"></a>Hinweise

**Str \_ GetPtr ist** als ANSI- (**Str \_ GetPtrA**) und Unicode-Versionen (**Str \_ GetPtrW**) verfügbar. Diese Funktionen werden nicht nach Namen exportiert oder in einer öffentlichen Headerdatei deklariert. Um sie zu verwenden, müssen Sie [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden und die Ordnungszahl 233 (**Str \_ GetPtrA**) oder 235 (**Str \_ GetPtrW**) von ComCtl32.dll anfordern, um einen Funktionszeiger zu erhalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>ComCtl32.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Str \_ GetPtrW** (Unicode) und **Str \_ GetPtrA** (ANSI)<br/>                       |



 

