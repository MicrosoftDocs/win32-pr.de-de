---
description: Öffnet das Dialogfeld "Schlüssel-Manager" in der Benutzeroberfläche.
ms.assetid: 65c2763f-42d5-4534-94f7-e753f6486014
title: KRShowKeyMgr-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KRShowKeyMgr
api_type:
- DllExport
api_location:
- Keymgr.dll
ms.openlocfilehash: 59b6b38cf7e78755c7d5c481a22a0a8b3854c8a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364794"
---
# <a name="krshowkeymgr-function"></a>KRShowKeyMgr-Funktion

\[Diese Funktion ist nur in Windows XP enthalten. Es ist zurzeit nicht in einer anderen Version von Windows enthalten, und es wird davon ausgegangen, dass es in zukünftigen Versionen von Windows nicht mehr enthalten ist.\]

Öffnet das Dialogfeld "Schlüssel-Manager" in der Benutzeroberfläche.

## <a name="syntax"></a>Syntax


```C++
void KRShowKeyMgr(
   HWND      hwParent,
   HINSTANCE hInstance,
   LPWSTR    pszCmdLine,
   int       CmdShow
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hwparent* 
</dt> <dd>

Ein Handle für das übergeordnete Fenster des Dialog Felds. Dieser Parameter kann **NULL** sein.

</dd> <dt>

*hInstance* 
</dt> <dd>

Dieser Parameter wird nicht verwendet und sollte auf **null** festgelegt werden.

</dd> <dt>

*pszcmdline* 
</dt> <dd>

Dieser Parameter wird nicht verwendet und sollte auf **null** festgelegt werden.

</dd> <dt>

*Cmdshow* 
</dt> <dd>

Dieser Parameter wird nicht verwendet und sollte auf **null** festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Keymgr.dll</dt> </dl> |



 

 
