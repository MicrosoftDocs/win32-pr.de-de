---
description: IUserIdentity2 wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop.
ms.assetid: 85238574-f6bf-43d7-a41b-3ea086c45e07
title: IUserIdentity2-Schnittstelle (Msident. h)
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
ms.openlocfilehash: 88142e462566a6afaf299096744a0b8f9ea83dfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524443"
---
# <a name="iuseridentity2-interface"></a>IUserIdentity2-Schnittstelle

\[**IUserIdentity2** wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen [Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop](fastuserswitching.md).\]

Macht Methoden verfügbar, die die Benennung, das Kennwort und die ordinale Steuerung für eine bestimmte Benutzeridentität bereitstellen.

## <a name="members"></a>Member

Die **IUserIdentity2** -Schnittstelle erbt von [**iuseridentity**](iuseridentity.md). **IUserIdentity2** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IUserIdentity2** -Schnittstelle verfügt über diese Methoden.



| Methode                                                  | BESCHREIBUNG                                                       |
|:--------------------------------------------------------|:------------------------------------------------------------------|
| [**ChangePassword**](iuseridentity2-changepassword.md) | Veraltet. Legt ein neues Kennwort für die Identität fest.<br/>      |
| [**GetOrdinal**](iuseridentity2-getordinal.md)         | Veraltet. Ruft die Ordinalzahl für diese Identität ab.<br/> |
| [**SetName**](iuseridentity2-setname.md)               | Veraltet. Legt den anzeigen amen der Identität fest.<br/>     |



 

## <a name="remarks"></a>Bemerkungen

Diese Schnittstelle stellt auch die Methoden der [**iuseridentity**](iuseridentity.md) -Schnittstelle bereit, von der Sie erbt.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Ende des Supports (Client)<br/>    | Windows 2000 Professional<br/>                                                   |
| Ende des Supports (Server)<br/>    | Windows 2000 Server<br/>                                                         |
| Header<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Iuseridentity**](iuseridentity.md)
</dt> </dl>

 

 




