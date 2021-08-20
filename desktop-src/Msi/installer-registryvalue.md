---
description: Die RegistryValue-Methode des Installer-Objekts liest Informationen zu einem angegebenen Registrierungsschlüssel des Werts.
ms.assetid: 63c258f9-8649-419d-9f79-3681f9f97302
title: Installer.RegistryValue-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.RegistryValue
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: eea77074a19ada084493bf5e24edaf49e25b659b0accdad16dab6c5781078f4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074920"
---
# <a name="installerregistryvalue-method"></a>Installer.RegistryValue-Methode

Die **RegistryValue-Methode** des [**Installer-Objekts**](installer-object.md) liest Informationen zu einem angegebenen Registrierungsschlüssel des Werts. Wenn der angegebene Schlüssel oder Wert nicht vorhanden ist, gibt die Methode den Fehler 9, "Subscript out of Range", zurück.

## <a name="syntax"></a>Syntax


```JScript
Installer.RegistryValue(
  root,
  key,
  value
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*root* 
</dt> <dd>

In Windows NT 4.0 ist der Registrierungsstamm entweder ein numerischer Stammschlüssel oder ein Computername als Zeichenfolge. Computernamen sind immer Zeichenfolgen. In Windows 95, Windows 98 oder Windows Me ist der Registrierungsstamm nur ein numerischer Stammschlüssel. Sie können auf HKLM nur auf einem Remotecomputer zugreifen.



| Root                                                                                                                                                                                   | Bedeutung      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| <span id="HKEY_CLASSES_ROOT"></span><span id="hkey_classes_root"></span><dl> <dt>**HKEY \_ CLASSES \_ ROOT**</dt> </dl>             | 0<br/> |
| <span id="HKEY_CURRENT_USER"></span><span id="hkey_current_user"></span><dl> <dt>**AKTUELLER \_ \_ HKEY-BENUTZER**</dt> </dl>             | 1<br/> |
| <span id="HKEY_LOCAL_MACHINE"></span><span id="hkey_local_machine"></span><dl> <dt>**HKEY \_ LOCAL \_ MACHINE**</dt> </dl>          | 2<br/> |
| <span id="HKEY_USERS"></span><span id="hkey_users"></span><dl> <dt>**\_HKEY-BENUTZER**</dt> </dl>                                   | 3<br/> |
| <span id="HKEY_PERFORMANCE_DATA"></span><span id="hkey_performance_data"></span><dl> <dt>**\_HKEY-LEISTUNGSDATEN \_**</dt> </dl> | 4<br/> |
| <span id="HKEY_CURRENT_CONFIG"></span><span id="hkey_current_config"></span><dl> <dt>**AKTUELLE \_ \_ HKEY-KONFIGURATION**</dt> </dl>       | 5<br/> |
| <span id="HKEY_DYN_DATA"></span><span id="hkey_dyn_data"></span><dl> <dt>**HKEY \_ DYN \_ DATA**</dt> </dl>                         | 6<br/> |



 

</dd> <dt>

*key* 
</dt> <dd>

Eine Zeichenfolge, die den vollständigen Schlüsselpfad aus dem Stamm enthält.

</dd> <dt>

*value* 
</dt> <dd>

Dieser optionale Parameter legt fest, welcher zugeordnete Wert für den angegebenen Schlüssel zurückgegeben werden soll. Der Wert ist einer der in der folgenden Tabelle aufgeführten Werte.



| Wert                                                                                                                                                                                                    | Bedeutung                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Missing_or_blank"></span><span id="missing_or_blank"></span><span id="MISSING_OR_BLANK"></span><dl> <dt>**Fehlt oder leer**</dt> </dl> | Gibt einen booleschen Wert zurück, der angibt, ob der Schlüssel vorhanden ist.<br/>                                                                                        |
| <span id="String"></span><span id="string"></span><span id="STRING"></span><dl> <dt>**String**</dt> </dl>                                         | Gibt die daten zurück, die dem benannten Wert zugeordnet sind, schlägt fehl, wenn der Wertname nicht vorhanden ist.<br/>                                                   |
| <span id="Positive_integer"></span><span id="positive_integer"></span><span id="POSITIVE_INTEGER"></span><dl> <dt>**Positive ganze Zahl**</dt> </dl> | Gibt den 1-basierten Aufzählungswertnamen zurück. Er ist leer, wenn er nicht vorhanden ist. Diese Option verwendet die [**RegEnumValue-Funktion.**](/windows/win32/api/winreg/nf-winreg-regenumvaluea)<br/> |
| <span id="Negative_integer"></span><span id="negative_integer"></span><span id="NEGATIVE_INTEGER"></span><dl> <dt>**Negative ganze Zahl**</dt> </dl> | Gibt den 1-basierten enumerierten Unterschlüsselnamen zurück. Dieser ist leer, wenn er nicht vorhanden ist. Diese Option verwendet die [**RegEnumKey-Funktion.**](/windows/win32/api/winreg/nf-winreg-regenumkeya)<br/>  |
| <span id="Zero_integer"></span><span id="zero_integer"></span><span id="ZERO_INTEGER"></span><dl> <dt>**Null ganze Zahl**</dt> </dl>                 | Gibt den Namen der Zeichenfolgenklasse für den angegebenen Schlüssel zurück.<br/>                                                                                        |
| <span id="Empty_string____"></span><span id="empty_string____"></span><span id="EMPTY_STRING____"></span><dl> <dt>**Leere Zeichenfolge " " "**</dt> </dl> | Gibt den Standardwert des Registrierungsschlüssels zurück.<br/>                                                                                               |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-0000000000046 definiert.<br/>                                                                                                                                                                           |



 

 
