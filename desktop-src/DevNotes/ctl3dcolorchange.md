---
description: Behandelt System Farbänderungen für Anwendungen, die ctl3d verwenden.
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
ms.openlocfilehash: 7e7b0d4480fde480ea24a6c2c0dd8a7a849fbc75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361952"
---
# <a name="ctl3dcolorchange-function"></a>Ctl3dColorChange-Funktion

Behandelt System Farbänderungen für Anwendungen, die ctl3d verwenden.

## <a name="syntax"></a>Syntax


```C++
BOOL Ctl3dColorChange(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn die Funktion erfolgreich ausgeführt wurde. Andernfalls wird **false** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

Diese Funktion sollte in der Hauptfenster Prozedur der Anwendung für die WM- **\_ syscolorchange** -Meldung aufgerufen werden, wie unten gezeigt.

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



 

 
