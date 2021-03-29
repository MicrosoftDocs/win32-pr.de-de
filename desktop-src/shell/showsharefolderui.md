---
description: Zeigt die Registerkarte Ordner Freigabe auf der Eigenschaften Seite für den angegebenen Ordner an.
ms.assetid: e622e4bb-eaf7-494f-b2a2-78ba1311a496
title: Showsharefolderui-Funktion
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
ms.openlocfilehash: e6270f72d1574a21b98ac9ee3151af1f34f08a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346428"
---
# <a name="showsharefolderui-function"></a>Showsharefolderui-Funktion

Zeigt die Registerkarte **Ordner Freigabe** auf der Eigenschaften Seite für den angegebenen Ordner an.

## <a name="syntax"></a>Syntax


```C++
HRESULT ShowShareFolderUI(
  _In_ HWND    hwndParent,
  _In_ LPCWSTR pszPath
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hwndParent* \[ in\]
</dt> <dd>

Typ: **HWND**

Ein Handle für das übergeordnete Fenster für das Eigenschaften Blatt.

</dd> <dt>

*pszpath* \[ in\]
</dt> <dd>

Typ: **LPCWSTR**

Ein Zeiger auf eine Zeichenfolge, die den Pfad zum Ordner angibt, in dem die Registerkarte für die **Ordner Freigabe** angezeigt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Diese Funktion gibt immer \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Diese Funktion verfügt über keine zugehörige lib-Datei. Sie müssen " [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) " und " [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) " verwenden, um Sie zu verwenden.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Ntshrui.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Showsharefolderuiw** (Unicode)<br/>                                            |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Cansharefolderw**](cansharefolderw.md)
</dt> </dl>

 

 
