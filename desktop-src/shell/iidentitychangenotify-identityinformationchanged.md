---
description: Identityinformationchanged wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop.
ms.assetid: 3aca8a98-3d12-482d-9991-d6b53adde522
title: 'Iidentitychangenotify:: identityinformationchanged-Methode (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify.IdentityInformationChanged
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: c33f67a4def3312564ed943e2a3a917fe2843980
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864903"
---
# <a name="iidentitychangenotifyidentityinformationchanged-method"></a>Iidentitychangenotify:: identityinformationchanged-Methode

\[**Identityinformationchanged** wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen [Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop](fastuserswitching.md).\]

Wird aufgerufen, wenn sich die Informationen zu einer Benutzeridentität geändert haben oder wenn eine Benutzeridentität hinzugefügt oder gelöscht wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT IdentityInformationChanged(
   DWORD dwType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwType* 
</dt> <dd>

Typ: **DWORD**

Ein-Wert, der den Typ der geänderten Informationen oder den für eine Identität ausgeführten Vorgang angibt. Kann eine Kombination der folgenden Werte sein.

<dt>



 (IIC \_ aktuelle \_ Identität \_ geändert)


</dt> <dd>

Die aktuelle Identität wurde geändert.

</dd> <dt>



 (IIC \_ Identität \_ geändert)


</dt> <dd>

Eine Identität wurde geändert.

</dd> <dt>



 (IIC \_ Identität \_ gelöscht)


</dt> <dd>

Eine Identität wurde gelöscht.

</dd> <dt>



 (IIC \_ Identität \_ hinzugefügt)


</dt> <dd>

Es wurde eine neue Identität hinzugefügt.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Sie können diese Methode implementieren, um benutzerdefiniertes Verhalten für Ihre Anwendung bereitzustellen, wenn die Liste der Benutzer Identitäten im System geändert wurde.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Ende des Supports (Client)<br/>    | Windows 2000 Professional<br/>                                                   |
| Ende des Supports (Server)<br/>    | Windows 2000 Server<br/>                                                         |
| Header<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msoe.dll</dt> </dl>    |



 

 




