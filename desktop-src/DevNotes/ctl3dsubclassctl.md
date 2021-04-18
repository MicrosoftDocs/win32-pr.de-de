---
description: Unterklassen eines einzelnen Steuer Elements, wenn das Steuerelement nicht in einem Dialogfeld angezeigt wird.
ms.assetid: 07a2bce1-4c69-4f8d-bb24-b17351f5e771
title: Ctl3dSubclassCtl-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dSubclassCtl
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 0ff6c6744c4ddda203149981218b8143fb78bce7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371486"
---
# <a name="ctl3dsubclassctl-function"></a>Ctl3dSubclassCtl-Funktion

Unterklassen eines einzelnen Steuer Elements, wenn das Steuerelement nicht in einem Dialogfeld angezeigt wird.

## <a name="syntax"></a>Syntax


```C++
BOOL Ctl3dSubclassCtl(
   HWND hwnd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HWND* 
</dt> <dd>

Ein Handle für das Steuerelement Fenster.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn das Steuerelement erfolgreich untergeordnet ist. Andernfalls wird **false** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ctl3dUnsubclassCtl**](ctl3dunsubclassctl.md)
</dt> </dl>

 

 
