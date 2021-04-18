---
description: Ermöglicht einem Debugger, Informationen zu dynamischen Funktionstabellen zu überprüfen.
ms.assetid: 32fd0dfd-ca7c-45e4-9d59-2b3318d7e13d
title: Rtlgetfunctiontablelisderad-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetFunctionTableListHead
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 3dde476ee9958952d85c66816a113b92529aa13e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368667"
---
# <a name="rtlgetfunctiontablelisthead-function"></a>Rtlgetfunctiontablelisderad-Funktion

\[Diese Funktion kann ohne vorherige Ankündigung geändert oder aus Windows entfernt werden.\]

Ermöglicht einem Debugger, Informationen zu dynamischen Funktionstabellen zu überprüfen.

## <a name="syntax"></a>Syntax


```C++
PLIST_ENTRY RtlGetFunctionTableListHead(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf den Anfang der Funktionstabellen Liste zurück.

## <a name="remarks"></a>Bemerkungen

Beachten Sie, dass die Windows Driver Kit (WDK)-Header Datei ntdef. h für einige Definitionen erforderlich ist. Die zugehörige Import Bibliothek ntdll. lib ist im WDK verfügbar. Sie können auch die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Ntdll.dll zu verknüpfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
