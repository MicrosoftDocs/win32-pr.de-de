---
description: Die IScanProfileMgr-Schnittstelle stellt Methoden zum Erstellen, Öffnen, Löschen und Verwalten von Scanprofilen bereit.
ms.assetid: f57a71b7-750c-42a8-be73-229f0145d9d5
title: IScanProfileMgr-Schnittstelle (Scanprofilemgr.h)
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
ms.openlocfilehash: d2d517143a55c2bd732bb8f9c642697a7d50151ddb72fcffd13d978caef597b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593090"
---
# <a name="iscanprofilemgr-interface"></a>IScanProfileMgr-Schnittstelle

Die **IScanProfileMgr-Schnittstelle** stellt Methoden zum Erstellen, Öffnen, Löschen und Verwalten von Scanprofilen bereit.

## <a name="members"></a>Member

Die **IScanProfileMgr-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IScanProfileMgr** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IScanProfileMgr-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                              | BESCHREIBUNG                                                                                                            |
|:------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [**CreateProfile**](-wia-iscanprofilemgr-createprofile.md)                         | Erstellt ein leeres Scanprofil und ordnet es einem Scanner oder einem anderen WIA 2.0-Element zu.<br/>                       |
| [**DeleteAllProfiles**](-wia-iscanprofilemgr-deleteallprofiles.md)                 | Löscht alle Scanprofile, die dem angegebenen Gerät zugeordnet sind.<br/>                                         |
| [**DeleteAllProfilesForUser**](-wia-iscanprofilemgr-deleteallprofilesforuser.md)   | Löscht alle Scanprofile, die für den Benutzer in dem System verfügbar sind, unter dem Ihre Anwendung ausgeführt wird. <br/> |
| [**DeleteProfile**](-wia-iscanprofilemgr-deleteprofile.md)                         | Löscht das angegebene Scanprofil.<br/>                                                                         |
| [**GetDefaultProfile**](-wia-iscanprofilemgr-getdefaultprofile.md)                 | Ruft das Standardscanprofil ab.<br/>                                                                              |
| [**GetNumProfiles**](-wia-iscanprofilemgr-getnumprofiles.md)                       | Ruft die Anzahl der Scanprofile ab, die für den Benutzer im System erstellt wurden, unter dem ihre Anwendung ausgeführt wird.<br/> |
| [**GetNumProfilesforDeviceID**](-wia-iscanprofilemgr-getnumprofilesfordeviceid.md) | Ruft die Anzahl der Scanprofile für das Gerät ab.<br/>                                                            |
| [**GetProfiles**](-wia-iscanprofilemgr-getprofiles.md)                             | Ruft alle Überprüfungsprofile ab, die für den Benutzer in dem System verfügbar sind, unter dem Ihre Anwendung ausgeführt wird.<br/>     |
| [**GetProfilesforDeviceID**](-wia-iscanprofilemgr-getprofilesfordeviceid.md)       | Ruft alle einem Gerät zugeordneten Scanprofile ab.<br/>                                                        |
| [**OpenProfile**](-wia-iscanprofilemgr-openprofile.md)                             | Öffnet ein Scanprofil, das als XML-Datei auf dem Datenträger gespeichert wurde.<br/>                                            |
| [**Aktualisieren**](-wia-iscanprofilemgr-refresh.md)                                     | Listet alle Scanprofile im System erneut auf.<br/>                                                          |
| [**SetDefault**](-wia-iscanprofilemgr-setdefault.md)                               | Legt das angegebene Scanprofil als Standardprofil fest.<br/>                                                     |



 

## <a name="remarks"></a>Hinweise

Verwenden Sie zum Erstellen eines **IScanProfileMgr-Objekts** die [CoCreateInstance-Methode](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) mit den folgenden Parametern:

``` syntax
CoCreateInstance(CLSID_ScanProfileMgr, NULL, CLSCTX_LOCAL_SERVER, IID_IScanProfileMgr, ppv)
```

Wenn ein Scanprofil mit der [**IScanProfile::Save-Methode**](-wia-iscanprofile-save.md) gespeichert wird, wird es als XML-Datei unter %USERPROFILE% \\ Anwendungsdaten \\ Microsoft Document Center \\ \\ UserScanProfiles gespeichert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Scanprofilemgr.h</dt> </dl> |
| Idl<br/>                      | <dl> <dt>Scanprofiles.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Scanprofilschema](-wia-scan-profile-schema.md)
</dt> </dl>

 

 
