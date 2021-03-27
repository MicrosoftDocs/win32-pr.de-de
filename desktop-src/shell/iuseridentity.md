---
description: Iuseridentity wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop.
ms.assetid: c2f11f8b-f944-445b-b4fc-ac57b0fe3a74
title: Iuseridentity-Schnittstelle (Msident. h)
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
ms.openlocfilehash: 068d806086aff44db172a4a7b09f55b600204478
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979481"
---
# <a name="iuseridentity-interface"></a>Iuseridentity-Schnittstelle

\[**Iuseridentity** wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen [Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop](fastuserswitching.md).\]

Macht Methoden verfügbar, die Identifikations-, Registrierungs-und Ordner Daten für eine bestimmte Benutzeridentität bereitstellen.

## <a name="members"></a>Member

Die **iuseridentity** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iuseridentity** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iuseridentity** -Schnittstelle verfügt über diese Methoden.



| Methode                                                         | BESCHREIBUNG                                                                                      |
|:---------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**GetCookie**](iuseridentity-getcookie.md)                   | Veraltet. Ruft das Cookie ab, mit dem diese Benutzeridentität eindeutig identifiziert wird.<br/>             |
| [**Getidentityfolder**](iuseridentity-getidentityfolder.md)   | Veraltet. Ruft den Datei Ordner ab, der dieser Identität zugeordnet ist.<br/>                       |
| [**GetName**](iuseridentity-getname.md)                       | Veraltet. Ruft den Namen ab, der dieser Benutzeridentität zugeordnet ist.<br/>                         |
| [**Openidentityregkey**](iuseridentity-openidentityregkey.md) | Veraltet. Ruft den Schlüssel in der Registrierung ab, der dieser Benutzeridentität entspricht.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Schnittstelle stellt Informationen bereit, die einer bestimmten Benutzeridentität entsprechen, die auf dem System vorhanden ist. Sie können auf den Identitäts Ordner dieser Benutzeridentität, den zugehörigen Registrierungsschlüssel und das zugehörige Identifikations Cookie zugreifen und den Namen abrufen, der der Benutzeridentität zugeordnet ist.

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

[**IUserIdentity2**](iuseridentity2.md)
</dt> <dt>

[**Iuseridentitymanager**](iuseridentitymanager.md)
</dt> <dt>

[**Iumumuseridentity**](ienumuseridentity.md)
</dt> </dl>

 

 
