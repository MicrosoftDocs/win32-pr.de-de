---
description: Gibt Java-Klassen Lade Programme frei, die möglicherweise beim Durchsuchen der Applets genutzt wurden.
ms.assetid: f6d5e8b9-4c0b-4533-8bf7-070b8c2e6681
title: Notifybrowsershutdown-Funktion
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
ms.openlocfilehash: 77fa2e5a0d387fcc0c90417b5f57d49178bc0626
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351313"
---
# <a name="notifybrowsershutdown-function"></a>Notifybrowsershutdown-Funktion

Gibt Java-Klassen Lade Programme frei, die möglicherweise beim Durchsuchen der Applets genutzt wurden.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI NotifyBrowserShutdown(
   LPVOID lpvReserved
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpvreserved* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert **S \_ OK**. Andernfalls ist der Rückgabewert ein Fehlercode.

## <a name="remarks"></a>Bemerkungen

Wenn die Anzahl der Browserfenster im integrierten Webmodus Null erreicht, gibt diese Funktion die Java-Klassen Lade Programme frei. Wenn der Benutzer das Durchsuchen von Applets erneut startet, lädt die Java-VM die neuesten Klassendateien herunter.

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjava.dll</dt> </dl> |



 

 
