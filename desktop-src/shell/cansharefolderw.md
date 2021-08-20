---
description: Wird verwendet, um zu bestimmen, ob die Option Diesen Ordner freigeben in der Webansicht angezeigt werden soll.
title: CanShareFolderW-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CanShareFolderW
- CanShareFolderW
api_type:
- DllExport
api_location:
- Ntshrui.dll
ms.assetid: 5fd28a14-53e7-4016-9c49-9bb14ce7808b
ms.openlocfilehash: 7013c6ae825c34ae7d2dd7b9d507eac1e52c8d4e3a27182e5297e72ef13b4d9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032868"
---
# <a name="cansharefolderw-function"></a>CanShareFolderW-Funktion

\[Diese Funktion ist über Windows XP mit Service Pack 2 (SP2) und Windows Server 2003 verfügbar. Sie kann in nachfolgenden Versionen von geändert oder nicht verfügbar Windows.\]

Wird verwendet, um zu bestimmen, ob die Option **Diesen Ordner freigeben** in der Webansicht angezeigt werden soll.

## <a name="syntax"></a>Syntax


```C++
STDAPI CanShareFolderW(
  _In_ LPCWSTR pszPath
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pszPath* \[ In\]
</dt> <dd>

Typ: **LPCWSTR**

Ein Zeiger auf eine Zeichenfolge, die den Pfad des zu testden Ordners angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **STDAPI**

Die Rückgabewerte umfassen Folgendes.



| Rückgabecode/-wert                                                                        | Beschreibung                                                                           |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>     | Der Pfad, auf den *pszPath zeigt,* gibt einen Ordner an, der freigegeben werden kann.<br/>    |
| <dl> <dt>**S \_ FALSE**</dt> </dl>  | Der Pfad, auf den *pszPath zeigt,* gibt einen Ordner an, der nicht freigegeben werden kann.<br/> |
| <dl> <dt>HRESULT-Fehler</dt> </dl> | Es ist ein Fehler aufgetreten.<br/>                                                     |



 

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine LIB-Datei zugeordnet. Sie müssen [**LoadLibrary und**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**GetProcAddress verwenden,**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) um sie zu verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Ntshrui.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **CanShareFolderW** (Unicode)<br/>                                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ShowShareFolderUI**](./showsharefolderui.md)
</dt> </dl>

 

 
