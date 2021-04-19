---
description: Behandelt die WM \_ CtlColor-Meldung für Anwendungen, die ctl3d verwenden.
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
ms.openlocfilehash: 57df7ed5e439d75b2edbf71e743cac069f0ed75b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373935"
---
# <a name="ctl3dctlcolorex-function"></a>Ctl3dCtlColorEx-Funktion

Behandelt die **WM \_ CtlColor** -Meldung für Anwendungen, die ctl3d verwenden.

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

Die **WM- \_ CtlColor** -Meldung für die Anwendung.

</dd> <dt>

*wParam* 
</dt> <dd>

Ein Handle für den Anzeige Kontext (DC).

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle für ein untergeordnetes Fenster (-Steuerelement).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ein Handle für den passenden Pinsel zurück, wenn die Funktion erfolgreich ausgeführt wird. Andernfalls wird zurück `(HBRUSH)(0)` gegeben, dass ein Fehler aufgetreten ist.

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
