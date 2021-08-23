---
description: Verarbeitet die \_ WM-CTLCOLOR-Nachricht für Anwendungen, die CTL3D verwenden.
ms.assetid: 8626a559-4856-4e7d-bf9c-edc48613b8f4
title: Ctl3dCtlColorEx-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dCtlColorEx
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 46fe35fd507f20e41e0a9b563ded5c9cf46e9c557893bc9287d65cbdf651b24f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691640"
---
# <a name="ctl3dctlcolorex-function"></a>Ctl3dCtlColorEx-Funktion

Verarbeitet die **\_ WM-CTLCOLOR-Nachricht** für Anwendungen, die CTL3D verwenden.

## <a name="syntax"></a>Syntax


```C++
HBRUSH Ctl3dCtlColorEx(
   UINT   wm,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wm* 
</dt> <dd>

Die **WM \_ CTLCOLOR-Nachricht** für die Anwendung.

</dd> <dt>

*wParam* 
</dt> <dd>

Ein Handle für den Anzeigekontext (DC).

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle für ein untergeordnetes Fenster (Steuerelement).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ein Handle für den entsprechenden Pinsel zurück, wenn die Funktion erfolgreich ausgeführt wird. Andernfalls wird zurückgegeben, `(HBRUSH)(0)` was angibt, dass ein Fehler aufgetreten ist.

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
