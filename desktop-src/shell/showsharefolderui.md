---
description: Zeigt die Registerkarte Ordnerfreigabe auf dem Eigenschaftenblatt für den angegebenen Ordner an.
ms.assetid: e622e4bb-eaf7-494f-b2a2-78ba1311a496
title: ShowShareFolderUI-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShowShareFolderUI
- ShowShareFolderUIW
api_type:
- DllExport
api_location:
- Ntshrui.dll
ms.openlocfilehash: 9683d7faee4bd44bd8f21e14250503f351e1a134119f978f872d7a0fe3ad6c4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968259"
---
# <a name="showsharefolderui-function"></a>ShowShareFolderUI-Funktion

Zeigt die **Registerkarte Ordnerfreigabe** auf dem Eigenschaftenblatt für den angegebenen Ordner an.

## <a name="syntax"></a>Syntax


```C++
HRESULT ShowShareFolderUI(
  _In_ HWND    hwndParent,
  _In_ LPCWSTR pszPath
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hwndParent* \[ In\]
</dt> <dd>

Typ: **HWND**

Ein Handle für das übergeordnete Fenster für das Eigenschaftenblatt.

</dd> <dt>

*pszPath* \[ In\]
</dt> <dd>

Typ: **LPCWSTR**

Ein Zeiger auf eine Zeichenfolge, die den Pfad zu dem Ordner angibt, in dem die Registerkarte **Ordnerfreigabe angezeigt** wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Diese Funktion gibt immer S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine LIB-Datei zugeordnet. Sie müssen [**LoadLibrary und**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**GetProcAddress verwenden,**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) um sie zu verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Ntshrui.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **ShowShareFolderUIW** (Unicode)<br/>                                            |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CanShareFolderW**](cansharefolderw.md)
</dt> </dl>

 

 
