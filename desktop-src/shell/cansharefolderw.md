---
description: Wird verwendet, um zu bestimmen, ob die Option diesen Ordner freigeben in der Webansicht angezeigt werden soll.
title: Cansharefolderw-Funktion
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
ms.openlocfilehash: cf7d0feb31666f3a918c0307a0b0983bff246fea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525403"
---
# <a name="cansharefolderw-function"></a>Cansharefolderw-Funktion

\[Diese Funktion ist über Windows XP mit Service Pack 2 (SP2) und Windows Server 2003 verfügbar. Sie wird möglicherweise in nachfolgenden Versionen von Windows geändert oder ist nicht verfügbar.\]

Wird verwendet, um zu bestimmen, ob die Option **diesen Ordner freigeben** in der Webansicht angezeigt werden soll.

## <a name="syntax"></a>Syntax


```C++
STDAPI CanShareFolderW(
  _In_ LPCWSTR pszPath
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pszpath* \[ in\]
</dt> <dd>

Typ: **LPCWSTR**

Ein Zeiger auf eine Zeichenfolge, die den Pfad des Ordners angibt, der getestet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **STDAPI**

Die Rückgabewerte umfassen Folgendes:



| Rückgabecode/-wert                                                                        | BESCHREIBUNG                                                                           |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>     | Der Pfad, auf den von *pszpath* verwiesen wird, gibt einen Ordner an, der freigegeben werden kann.<br/>    |
| <dl> <dt>**S \_ false**</dt> </dl>  | Der Pfad, auf den *pszpath* zeigt, gibt einen Ordner an, der nicht freigegeben werden kann.<br/> |
| <dl> <dt>HRESULT-Fehler</dt> </dl> | Es ist ein Fehler aufgetreten.<br/>                                                     |



 

## <a name="remarks"></a>Bemerkungen

Diese Funktion verfügt über keine zugehörige lib-Datei. Sie müssen " [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) " und " [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) " verwenden, um Sie zu verwenden.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Ntshrui.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Cansharefolderw** (Unicode)<br/>                                               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Showsharefolderui**](./showsharefolderui.md)
</dt> </dl>

 

 
