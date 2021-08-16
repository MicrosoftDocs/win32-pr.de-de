---
description: Gibt Java-Klassenlader frei, die möglicherweise beim Durchsuchen der Applets verwendet wurden.
ms.assetid: f6d5e8b9-4c0b-4533-8bf7-070b8c2e6681
title: NotifyBrowserShutdown-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NotifyBrowserShutdown
api_type:
- DllExport
api_location:
- Msjava.dll
ms.openlocfilehash: 60f361d8f9963081c4af2a840a01eb29f9946eb064cad2335f95b3622932add1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117826816"
---
# <a name="notifybrowsershutdown-function"></a>NotifyBrowserShutdown-Funktion

Gibt Java-Klassenlader frei, die möglicherweise beim Durchsuchen der Applets verwendet wurden.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI NotifyBrowserShutdown(
   LPVOID lpvReserved
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpvReserved* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert **S \_ OK.** Andernfalls ist der Rückgabewert ein Fehlercode.

## <a name="remarks"></a>Hinweise

Wenn die Anzahl der Browserfenster im integrierten Webmodus null erreicht, gibt diese Funktion die Java-Klassenlader frei. Wenn der Benutzer erneut mit dem Durchsuchen von Applets beginnt, werden von der Java-VM die neuesten Klassendateien heruntergeladen.

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjava.dll</dt> </dl> |



 

 
