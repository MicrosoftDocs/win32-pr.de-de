---
description: IUserIdentity wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schnellem Benutzerwechsel und Remotedesktop.
ms.assetid: c2f11f8b-f944-445b-b4fc-ac57b0fe3a74
title: IUserIdentity-Schnittstelle (Msident.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: f7e721f60198791e530300d5181abaa84e96c1a04f285972314ab866dd86215f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713780"
---
# <a name="iuseridentity-interface"></a>IUserIdentity-Schnittstelle

\[**IUserIdentity** wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein. Verwenden Sie stattdessen [Benutzerkonten mit schnellem Benutzerwechsel und Remotedesktop](fastuserswitching.md).\]

Macht Methoden verfügbar, die Identifikations-, Registrierungs- und Ordnerdaten für eine bestimmte Benutzeridentität bereitstellen.

## <a name="members"></a>Member

Die **IUserIdentity-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IUserIdentity** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IUserIdentity-Schnittstelle** verfügt über diese Methoden.



| Methode                                                         | Beschreibung                                                                                      |
|:---------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**GetCookie**](iuseridentity-getcookie.md)                   | Veraltet. Ruft das Cookie ab, das verwendet wird, um diese Benutzeridentität eindeutig zu identifizieren.<br/>             |
| [**GetIdentityFolder**](iuseridentity-getidentityfolder.md)   | Veraltet. Ruft den Dateiordner ab, der dieser Identität zugeordnet ist.<br/>                       |
| [**GetName**](iuseridentity-getname.md)                       | Veraltet. Ruft den Namen ab, der dieser Benutzeridentität zugeordnet ist.<br/>                         |
| [**OpenIdentityRegKey**](iuseridentity-openidentityregkey.md) | Veraltet. Ruft den Schlüssel in der Registrierung ab, der dieser Benutzeridentität entspricht.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Schnittstelle stellt Informationen bereit, die einer bestimmten Benutzeridentität im System entsprechen. Sie können auf den Identitätsordner, den Registrierungsschlüssel und das Identifikationscookie dieser Benutzeridentität zugreifen und den der Benutzeridentität zugeordneten Namen abrufen.

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

[**IUserIdentity2**](iuseridentity2.md)
</dt> <dt>

[**IUserIdentityManager**](iuseridentitymanager.md)
</dt> <dt>

[**IEnumUserIdentity**](ienumuseridentity.md)
</dt> </dl>

 

 
