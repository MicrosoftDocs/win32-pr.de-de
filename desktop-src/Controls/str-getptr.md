---
title: Str_GetPtr-Funktion
description: Kopiert eine Zeichenfolge von einem Puffer in einen anderen.
ms.assetid: a3dd55a0-3f8b-4d6c-9956-666bebc3ab8d
keywords:
- Windows-Steuerelemente Str_GetPtr-Funktion
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
ms.openlocfilehash: fec99bb4d91bde86d901c0e7ed4761bafd15f3a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740512"
---
# <a name="str_getptr-function"></a>Str \_ GetPtr-Funktion

\[Diese Funktion ist über Windows XP mit Service Pack 2 (SP2) und Windows Server 2003 verfügbar. Sie wird möglicherweise in nachfolgenden Versionen von Windows geändert oder ist nicht verfügbar.\]

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

*pszsource* \[ in\]
</dt> <dd>

Typ: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Ein Zeiger auf eine Quell Zeichenfolge.

</dd> <dt>

*pszdest* \[ in, out\]
</dt> <dd>

Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Ein Zeiger auf den Ziel Puffer. Dieser Wert kann **null** sein.

</dd> <dt>

*cchdest* \[ in\]
</dt> <dd>

Typ: **int**

Die Größe von *pszdest* in Zeichen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **int**

Wenn *pszdest* gleich NULL oder *cchdest* gleich NULL ist, wird die Größe des Puffers in Zeichen zurückgegeben, die eine mit NULL endenden Kopie der Zeichenfolge enthalten muss, auf die von *pszsource* **verwiesen wird.**

Wenn *pszdest* nicht **null** ist, wird die Anzahl der erfolgreich kopierten Zeichen zurückgegeben, einschließlich des abschließenden NULL-Zeichens.

Wenn *pszdest* nicht die gesamte Zeichenfolge enthalten kann, auf die *pszsource* zeigt, werden (*cchdest*-1) Zeichen kopiert, die Zeichenfolge mit NULL-terminiert und *cchdest* zurückgegeben.

## <a name="remarks"></a>Bemerkungen

**Str \_ GetPtr** ist als ANSI-(**Str \_ getptra**) und Unicode-Versionen (**Str \_ getptrw**) verfügbar. Diese Funktionen werden nicht nach Namen exportiert oder in einer öffentlichen Header Datei deklariert. Um Sie verwenden zu können, müssen Sie [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) und Request Ordnungszahl 233 (**Str \_ getptra**) oder 235 (**Str \_ getptrw**) aus ComCtl32.dll verwenden, um einen Funktionszeiger zu erhalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>ComCtl32.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Str \_ Getptrw** (Unicode) und **Str \_ getptra** (ANSI)<br/>                       |



 

