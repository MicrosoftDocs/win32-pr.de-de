---
description: IUserIdentity2 wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schnellem Benutzerwechsel und Remotedesktop.
ms.assetid: 85238574-f6bf-43d7-a41b-3ea086c45e07
title: IUserIdentity2-Schnittstelle (Msident.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: a1a23ea6e0d5832ee6d78453f3a246b9db749c0d7b24b90a2199a7e8cfd225b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118720586"
---
# <a name="iuseridentity2-interface"></a>IUserIdentity2-Schnittstelle

\[**IUserIdentity2** wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein. Verwenden Sie stattdessen [Benutzerkonten mit schnellem Benutzerwechsel und Remotedesktop](fastuserswitching.md).\]

Macht Methoden verfügbar, die Benennungs-, Kennwort- und Ordnungssteuerung für eine bestimmte Benutzeridentität bereitstellen.

## <a name="members"></a>Member

Die **IUserIdentity2-Schnittstelle** erbt von [**IUserIdentity**](iuseridentity.md). **IUserIdentity2** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IUserIdentity2-Schnittstelle** verfügt über diese Methoden.



| Methode                                                  | Beschreibung                                                       |
|:--------------------------------------------------------|:------------------------------------------------------------------|
| [**ChangePassword**](iuseridentity2-changepassword.md) | Veraltet. Legt ein neues Kennwort für die Identität fest.<br/>      |
| [**GetOrdinal**](iuseridentity2-getordinal.md)         | Veraltet. Ruft die Ordnungszahl für diese Identität ab.<br/> |
| [**SetName**](iuseridentity2-setname.md)               | Veraltet. Legt den Anzeigenamen der Identität fest.<br/>     |



 

## <a name="remarks"></a>Hinweise

Diese Schnittstelle stellt auch die Methoden der [**IUserIdentity-Schnittstelle**](iuseridentity.md) bereit, von der sie erbt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Ende des Supports (Client)<br/>    | Windows 2000 Professional<br/>                                                   |
| Ende des Supports (Server)<br/>    | Windows 2000 Server<br/>                                                         |
| Header<br/>                   | <dl> <dt>Msident.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msident.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IUserIdentity**](iuseridentity.md)
</dt> </dl>

 

 




