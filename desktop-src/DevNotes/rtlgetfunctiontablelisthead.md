---
description: Ermöglicht einem Debugger das Untersuchen dynamischer Funktionstabelleninformationen.
ms.assetid: 32fd0dfd-ca7c-45e4-9d59-2b3318d7e13d
title: RtlGetFunctionTableListHead-Funktion
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
ms.openlocfilehash: ff41aca0d268083132fd1a45371b0bb1ca026e5e6d693619ba1e2c2f9f2dd8f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118666730"
---
# <a name="rtlgetfunctiontablelisthead-function"></a>RtlGetFunctionTableListHead-Funktion

\[Diese Funktion kann ohne weitere Ankündigung geändert oder aus Windows entfernt werden.\]

Ermöglicht einem Debugger das Untersuchen dynamischer Funktionstabelleninformationen.

## <a name="syntax"></a>Syntax


```C++
PLIST_ENTRY RtlGetFunctionTableListHead(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf den Kopf der Funktionstabellenliste zurück.

## <a name="remarks"></a>Hinweise

Beachten Sie, dass für einige Definitionen die WDK-Headerdatei (Windows Driver Kit) Ntdef.h erforderlich ist. Die zugeordnete Importbibliothek Ntdll.lib ist im WDK verfügbar. Sie können auch die Funktionen [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um dynamisch mit Ntdll.dll zu verknüpfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
