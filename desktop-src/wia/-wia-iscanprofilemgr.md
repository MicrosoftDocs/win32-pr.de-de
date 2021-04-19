---
description: Die iscanprofilemgr-Schnittstelle stellt Methoden zum Erstellen, öffnen, löschen und Verwalten von Scan Profilen bereit.
ms.assetid: f57a71b7-750c-42a8-be73-229f0145d9d5
title: Iscanprofilemgr-Schnittstelle (scanprofilemgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 9f0762befdda272b91451dcca67c3f9560ad354e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348226"
---
# <a name="iscanprofilemgr-interface"></a>Iscanprofilemgr-Schnittstelle

Die **iscanprofilemgr** -Schnittstelle stellt Methoden zum Erstellen, öffnen, löschen und Verwalten von Scan Profilen bereit.

## <a name="members"></a>Member

Die **iscanprofilemgr** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Iscanprofilemgr** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iscanprofilemgr** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                              | BESCHREIBUNG                                                                                                            |
|:------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [**"Kreateprofile"**](-wia-iscanprofilemgr-createprofile.md)                         | Erstellt ein leeres Überprüfungs Profil und ordnet es einem Scanner oder einem anderen WIA-2,0-Element zu.<br/>                       |
| [**Deleteallprofiles**](-wia-iscanprofilemgr-deleteallprofiles.md)                 | Löscht alle Überprüfungs Profile, die dem angegebenen Gerät zugeordnet sind.<br/>                                         |
| [**Deleteallprofilesforuser**](-wia-iscanprofilemgr-deleteallprofilesforuser.md)   | Löscht alle Überprüfungs Profile, die für den Benutzer in dem System verfügbar sind, unter dem Ihre Anwendung ausgeführt wird. <br/> |
| [**DeleteProfile**](-wia-iscanprofilemgr-deleteprofile.md)                         | Löscht das angegebene Überprüfungs Profil.<br/>                                                                         |
| [**Getdefaultprofile**](-wia-iscanprofilemgr-getdefaultprofile.md)                 | Ruft das Standard Überprüfungs Profil ab.<br/>                                                                              |
| [**Getnumprofiles**](-wia-iscanprofilemgr-getnumprofiles.md)                       | Ruft die Anzahl der Überprüfungs Profile ab, die für den Benutzer im System erstellt wurden, unter dem Ihre Anwendung ausgeführt wird.<br/> |
| [**Getnumprofilesforde viceid**](-wia-iscanprofilemgr-getnumprofilesfordeviceid.md) | Ruft die Anzahl der Scan Profile für das Gerät ab.<br/>                                                            |
| [**Getprofiles**](-wia-iscanprofilemgr-getprofiles.md)                             | Ruft alle Überprüfungs Profile ab, die für den Benutzer im System verfügbar sind, unter dem Ihre Anwendung ausgeführt wird.<br/>     |
| [**Getprofilesforde viceid**](-wia-iscanprofilemgr-getprofilesfordeviceid.md)       | Ruft alle einem Gerät zugeordneten Scan Profile ab.<br/>                                                        |
| [**Openprofile**](-wia-iscanprofilemgr-openprofile.md)                             | Öffnet ein Überprüfungs Profil, das als XML-Datei auf einem Datenträger gespeichert wurde.<br/>                                            |
| [**Aktualisieren**](-wia-iscanprofilemgr-refresh.md)                                     | Listet alle Scan Profile im System erneut auf.<br/>                                                          |
| [**SetDefault**](-wia-iscanprofilemgr-setdefault.md)                               | Legt das angegebene Überprüfungs Profil als Standardprofil fest.<br/>                                                     |



 

## <a name="remarks"></a>Bemerkungen

Verwenden Sie zum Erstellen eines **iscanprofilemgr** -Objekts die [cokreateinstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Methode mit den folgenden Parametern:

``` syntax
CoCreateInstance(CLSID_ScanProfileMgr, NULL, CLSCTX_LOCAL_SERVER, IID_IScanProfileMgr, ppv)
```

Wenn ein Überprüfungs Profil mithilfe der [**iscanprofile:: Save**](-wia-iscanprofile-save.md) -Methode gespeichert wird, wird es als XML-Datei unter% User Profile% \\ Application Data \\ Microsoft \\ Document Center \\ userscanprofiles gespeichert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Scanprofilemgr. h</dt> </dl> |
| IDL<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Profil Schema überprüfen](-wia-scan-profile-schema.md)
</dt> </dl>

 

 
