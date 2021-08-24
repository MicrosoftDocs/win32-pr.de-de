---
description: Verarbeitet Systemfarbänderungen für Anwendungen, die CTL3D verwenden.
ms.assetid: b1eadb7d-39a5-47e9-9ae5-62bd33557f6b
title: Ctl3dColorChange-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dColorChange
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: c9c3032bb7105a27b995c236e01ce5fc5c304de4108f6c996a5cbb5799be496d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654600"
---
# <a name="ctl3dcolorchange-function"></a>Ctl3dColorChange-Funktion

Verarbeitet Systemfarbänderungen für Anwendungen, die CTL3D verwenden.

## <a name="syntax"></a>Syntax


```C++
BOOL Ctl3dColorChange(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn die Funktion erfolgreich ist. andernfalls wird **FALSE zurückgegeben.**

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

Diese Funktion sollte in der Hauptfensterprozedur der Anwendung für die **WM \_ SYSCOLORCHANGE-Nachricht** aufgerufen werden, wie unten dargestellt.

## <a name="examples"></a>Beispiele

``` syntax
case WM_SYSCOLORCHANGE:
   Ctl3dColorChange();
   break;
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
