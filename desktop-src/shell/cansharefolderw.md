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
ms.openlocfilehash: 46df03208ecc468aac366fb0b4cfb33e1a68157e
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841681"
---
# <a name="cansharefolderw-function"></a>CanShareFolderW-Funktion

\[Diese Funktion ist über Windows XP mit Service Pack 2 (SP2) und Windows Server 2003 verfügbar. Sie kann in nachfolgenden Versionen von Windows geändert oder nicht verfügbar sein.\]

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



| Rückgabecode/-wert                                                                        | BESCHREIBUNG                                                                           |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>     | Der Pfad, auf den *pszPath zeigt,* gibt einen Ordner an, der freigegeben werden kann.<br/>    |
| <dl> <dt>**S \_ FALSE**</dt> </dl>  | Der Pfad, auf den *pszPath zeigt,* gibt einen Ordner an, der nicht freigegeben werden kann.<br/> |
| <dl> <dt>HRESULT-Fehler</dt> </dl> | Es ist ein Fehler aufgetreten.<br/>                                                     |



 

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine LIB-Datei zugeordnet. Sie müssen [**LoadLibrary und**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**GetProcAddress verwenden,**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) um sie zu verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ XP-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Ntshrui.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **CanShareFolderW** (Unicode)<br/>                                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ShowShareFolderUI**](./showsharefolderui.md)
</dt> </dl>

 

 
