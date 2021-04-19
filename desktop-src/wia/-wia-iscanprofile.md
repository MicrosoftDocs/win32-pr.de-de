---
description: Die iscanprofile-Schnittstelle stellt ein einzelnes Überprüfungs Profil dar und ermöglicht Anwendungen das Festlegen und Abrufen der Eigenschaften des Profils.
ms.assetid: 5cd76256-d64e-4934-8cc2-0a467c7e34a9
title: Iscanprofile-Schnittstelle
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
ms.openlocfilehash: 2e02352eef16a9b899e4c635f11c5d10b3ab5113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359061"
---
# <a name="iscanprofile-interface"></a>Iscanprofile-Schnittstelle

Die **iscanprofile** -Schnittstelle stellt ein einzelnes Überprüfungs Profil dar und ermöglicht Anwendungen das Festlegen und Abrufen der Eigenschaften des Profils.

## <a name="members"></a>Member

Die **iscanprofile** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Iscanprofile** verfügt auch über die folgenden Typen von Mitgliedern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iscanprofile** -Schnittstelle verfügt über diese Methoden.



| Methode                                                     | BESCHREIBUNG                                                                                                                                         |
|:-----------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Getallpropids**](-wia-iscanprofile-getallpropids.md)   | Ruft alle verfügbaren Eigenschaften-IDs in einem Profil ab.<br/>                                                                                            |
| [**GetDeviceID**](-wia-iscanprofile-getdeviceid.md)       | Gibt die ID des Geräts zurück.<br/>                                                                                                            |
| [**GetGUID**](-wia-iscanprofile-getguid.md)               | Gibt die GUID des Profils zurück.<br/>                                                                                                         |
| [**GetItem**](-wia-iscanprofile-getitem.md)               | Ruft die GUID der Kategorie des WIA 2,0-Elements ab, dem das Profil zugeordnet ist.<br/>                                                   |
| [**GetName**](-wia-iscanprofile-getname.md)               | Ruft den anzeigen amen des Profils ab.<br/>                                                                                                   |
| [**Getnumpropids**](-wia-iscanprofile-getnumpropids.md)   | Ruft die Anzahl der Eigenschaften-IDs in einem Profil ab.<br/>                                                                                            |
| [**GetProperty**](-wia-iscanprofile-getproperty.md)       | Ruft den Wert der angegebenen untergeordneten Eigenschaften im- `<Properties>` Element eines Scan Profils ab.<br/>                                            |
| [**IsDefault**](-wia-iscanprofile-isdefault.md)           | Ruft einen Wert ab, der angibt, ob das Profil das Standard Überprüfungs Profil eines zugeordneten [**IWiaItem2**](-wia-iwiaitem2.md) -Geräts ist.<br/> |
| [**RemoveProperty**](-wia-iscanprofile-removeproperty.md) | Entfernt eine angegebene Liste von untergeordneten Eigenschaften im- `<Properties>` Element eines Scan Profils.<br/>                                            |
| [**Speichern**](-wia-iscanprofile-save.md)                     | Speichert Änderungen an einem Profil auf der Festplatte.<br/>                                                                                                      |
| [**-Element**](-wia-iscanprofile-setitem.md)               | Legt die GUID der Kategorie eines WIA-2,0-Elements fest, dem das Profil zugeordnet ist.<br/>                                                       |
| [**SetName**](-wia-iscanprofile-setname.md)               | Legt den anzeigen amen des Profils fest.<br/>                                                                                                   |
| [**SetProperty**](-wia-iscanprofile-setproperty.md)       | Legt den Wert der angegebenen untergeordneten Eigenschaften im- `<Properties>` Element eines Scan Profils fest.<br/>                                            |



 

## <a name="remarks"></a>Bemerkungen

Jedes [**IWiaItem2**](-wia-iwiaitem2.md) -Gerät kann über ein Überprüfungs Profil verfügen. Allerdings können **IWiaItem2** Items von Typen, \_ die mit einer Kategorie \_ fertiggestellt \_ wurden, die Datei fertiggestellt \_ \_ haben

Wenn ein Überprüfungs Profil mithilfe der [**iscanprofile:: Save**](-wia-iscanprofile-save.md) -Methode gespeichert wird, wird es als XML-Datei unter% User Profile% \\ Application Data \\ Microsoft \\ Document Center \\ userscanprofiles gespeichert.

Um eine Instanz eines **iscanprofile** -Objekts zu erstellen, verwenden Sie die [**iscanprofilemgr:: kreateprofile**](-wia-iscanprofilemgr-createprofile.md) -Methode. Um einen Verweis auf ein Überprüfungs Profil zu erhalten, das bereits auf dem Datenträger gespeichert wurde, verwenden Sie die [**iscanprofilemgr:: openprofile**](-wia-iscanprofilemgr-openprofile.md) -Methode.

Alle Scan Profile verfügen über die folgenden Elemente: `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>` , und `<Properties>` . Das Standardprofil eines Geräts weist auch ein- `<Default>` Element auf.

Das `<ProfileGUID>` -Element und das- `<DeviceID>` Element können nicht geändert werden, nachdem das Profil erstellt wurde. Die Werte des `<ProfileName>` -Elements und des- `<WiaItem>` Elements können nach dem Erstellen des Profils geändert werden. Das- `<Default>` Element kann hinzugefügt oder gelöscht werden. Dies kann Programm gesteuert mit den Methoden [**iscanprofile:: SetName**](-wia-iscanprofile-setname.md), [**iscanprofile:: SetItem**](-wia-iscanprofile-setitem.md)und [**iscanprofilemgr:: SetDefault**](-wia-iscanprofilemgr-setdefault.md) erfolgen. Diese Eigenschaften können auch von Benutzern über die [**iscanprofileui:: scanprofiledialog**](-wia-iscanprofileui-scanprofiledialog.md) -Methode geändert werden.

Das- `<Properties>` Element enthält untergeordnete Elemente `<Property>` . Verwenden Sie diese, um dem Profil eine beliebige WIA 2,0-Element-oder-Geräte Eigenschaft hinzuzufügen. Sie können auch Ihre eigenen Image-Erstell-untergeordneten Elemente entwickeln `<Property>` . Dadurch ist das Scan Profil Schema erweiterbar. (Weitere Informationen zum Erweitern des Schemas finden Sie unter [Definieren von benutzerdefinierten Eigenschaften](-wia-defining-custom-properties.md), [**iscanprofile:: GetProperty**](-wia-iscanprofile-getproperty.md)und [**iscanprofile:: SetProperty**](-wia-iscanprofile-setproperty.md).)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                        |
| IDL<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Profil Schema überprüfen](-wia-scan-profile-schema.md)
</dt> </dl>

 

 
