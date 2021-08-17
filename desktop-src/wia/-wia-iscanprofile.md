---
description: Die IScanProfile-Schnittstelle stellt ein einzelnes Scanprofil dar und ermöglicht Anwendungen das Festlegen und Abrufen der Eigenschaften des Profils.
ms.assetid: 5cd76256-d64e-4934-8cc2-0a467c7e34a9
title: IScanProfile-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile
api_type:
- COM
api_location:
- Scanprofiles.idl
ms.openlocfilehash: 1de80ac23ffa3e2687e2e6d0449f7a273067d5899204c479f9b62e8571190d61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450830"
---
# <a name="iscanprofile-interface"></a>IScanProfile-Schnittstelle

Die **IScanProfile-Schnittstelle** stellt ein einzelnes Scanprofil dar und ermöglicht Anwendungen das Festlegen und Abrufen der Eigenschaften des Profils.

## <a name="members"></a>Member

Die **IScanProfile-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IScanProfile** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IScanProfile-Schnittstelle** verfügt über diese Methoden.



| Methode                                                     | BESCHREIBUNG                                                                                                                                         |
|:-----------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAllPropIDs**](-wia-iscanprofile-getallpropids.md)   | Ruft alle verfügbaren Eigenschaften-IDs in einem Profil ab.<br/>                                                                                            |
| [**GetDeviceID**](-wia-iscanprofile-getdeviceid.md)       | Gibt die ID des Geräts zurück.<br/>                                                                                                            |
| [**GetGUID**](-wia-iscanprofile-getguid.md)               | Gibt die GUID des Profils zurück.<br/>                                                                                                         |
| [**GetItem**](-wia-iscanprofile-getitem.md)               | Ruft die GUID der Kategorie des WIA 2.0-Elements ab, dem das Profil zugeordnet ist.<br/>                                                   |
| [**GetName**](-wia-iscanprofile-getname.md)               | Ruft den Anzeigenamen des Profils ab.<br/>                                                                                                   |
| [**GetNumPropIDS**](-wia-iscanprofile-getnumpropids.md)   | Ruft die Anzahl der Eigenschaften-IDs in einem Profil ab.<br/>                                                                                            |
| [**GetProperty**](-wia-iscanprofile-getproperty.md)       | Ruft den Wert der angegebenen untergeordneten Eigenschaften im `<Properties>` -Element eines Scanprofils ab.<br/>                                            |
| [**IsDefault**](-wia-iscanprofile-isdefault.md)           | Ruft einen Wert ab, der angibt, ob das Profil das Standardscanprofil eines zugeordneten [**IWiaItem2-Geräts**](-wia-iwiaitem2.md) ist.<br/> |
| [**RemoveProperty**](-wia-iscanprofile-removeproperty.md) | Entfernt eine angegebene Liste untergeordneter Eigenschaften im `<Properties>` -Element eines Scanprofils.<br/>                                            |
| [**Speichern**](-wia-iscanprofile-save.md)                     | Speichert Änderungen an einem Profil auf dem Datenträger.<br/>                                                                                                      |
| [**SetItem**](-wia-iscanprofile-setitem.md)               | Legt die GUID der Kategorie des WIA 2.0-Elements fest, dem das Profil zugeordnet ist.<br/>                                                       |
| [**SetName**](-wia-iscanprofile-setname.md)               | Legt den Anzeigenamen des Profils fest.<br/>                                                                                                   |
| [**Setproperty**](-wia-iscanprofile-setproperty.md)       | Legt den Wert der angegebenen untergeordneten Eigenschaften im `<Properties>` -Element eines Scanprofils fest.<br/>                                            |



 

## <a name="remarks"></a>Hinweise

Jedes [**IWiaItem2-Gerät**](-wia-iwiaitem2.md) kann über ein Überprüfungsprofil verfügen. **IWiaItem2-Elemente** der Typen WIA \_ CATEGORY \_ FINISHED FILE und WIA CATEGORY ROOT können jedoch \_ keine Profile \_ \_ aufweisen.

Wenn ein Scanprofil mit der [**IScanProfile::Save-Methode**](-wia-iscanprofile-save.md) gespeichert wird, wird es als XML-Datei unter %USERPROFILE% \\ Anwendungsdaten \\ Microsoft Document Center \\ \\ UserScanProfiles gespeichert.

Um eine Instanz eines **IScanProfile-Objekts** zu erstellen, verwenden Sie die [**IScanProfileMgr::CreateProfile-Methode.**](-wia-iscanprofilemgr-createprofile.md) Verwenden Sie die [**IScanProfileMgr::OpenProfile-Methode,**](-wia-iscanprofilemgr-openprofile.md) um einen Verweis auf ein Scanprofil abzurufen, das bereits auf dem Datenträger gespeichert wurde.

Alle Scanprofile verfügen über die folgenden Elemente: `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>` und `<Properties>` . Das Standardprofil eines Geräts verfügt auch über ein `<Default>` -Element.

Die `<ProfileGUID>` Elemente und können nach dem Erstellen des `<DeviceID>` Profils nicht mehr geändert werden. Die Werte des `<ProfileName>` -Elements und des `<WiaItem>` -Elements können nach dem Erstellen des Profils geändert werden. Das `<Default>` Element kann hinzugefügt oder gelöscht werden. Dies kann programmgesteuert mit den Methoden [**IScanProfile::SetName,**](-wia-iscanprofile-setname.md) [**IScanProfile::SetItem**](-wia-iscanprofile-setitem.md)und [**IScanProfileMgr::SetDefault**](-wia-iscanprofilemgr-setdefault.md) erfolgen. Diese Eigenschaften können auch von Benutzern über die [**IScanProfileUI::ScanProfileDialog-Methode**](-wia-iscanprofileui-scanprofiledialog.md) geändert werden.

Das `<Properties>` -Element enthält `<Property>` untergeordnete Elemente. Verwenden Sie diese, um dem Profil alle WIA 2.0-Elemente oder -Geräteeigenschaften hinzuzufügen. Sie können auch eigene untergeordnete Bilder `<Property>` entwickeln. Dadurch wird das Scanprofilschema erweiterbar. (Weitere Informationen zum Erweitern des Schemas finden Sie unter [Definieren von benutzerdefinierten Eigenschaften,](-wia-defining-custom-properties.md) [**IScanProfile::GetProperty**](-wia-iscanprofile-getproperty.md)und [**IScanProfile::SetProperty**](-wia-iscanprofile-setproperty.md).)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                        |
| Idl<br/>                      | <dl> <dt>Scanprofiles.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Scanprofilschema](-wia-scan-profile-schema.md)
</dt> </dl>

 

 
