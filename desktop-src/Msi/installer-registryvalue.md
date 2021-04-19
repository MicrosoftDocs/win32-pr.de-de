---
description: Die REGISTRYVALUE-Methode des Installer-Objekts liest Informationen zu einem angegebenen Registrierungsschlüssel mit dem Wert.
ms.assetid: 63c258f9-8649-419d-9f79-3681f9f97302
title: Installer. REGISTRYVALUE-Methode
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
ms.openlocfilehash: e6da79ff08eebe62ad177119a35bfc29b21c9350
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358128"
---
# <a name="installerregistryvalue-method"></a>Installer. REGISTRYVALUE-Methode

Die **REGISTRYVALUE** -Methode des [**Installer**](installer-object.md) -Objekts liest Informationen zu einem angegebenen Registrierungsschlüssel mit dem Wert. Wenn der angegebene Schlüssel oder Wert nicht vorhanden ist, gibt die Methode den Fehler "9", "außerhalb des gültigen Bereichs", zurück.

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

In Windows NT 4,0 ist der Registrierungs Stamm entweder ein numerischer Stamm Schlüssel oder ein Computername als Zeichenfolge. Computernamen sind immer Zeichen folgen. In Windows 95, Windows 98 oder Windows Me ist der Registrierungs Stamm nur ein numerischer Stamm Schlüssel. Sie können auf einem Remote Computer nur auf HKLM zugreifen.



| Root                                                                                                                                                                                   | Bedeutung      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| <span id="HKEY_CLASSES_ROOT"></span><span id="hkey_classes_root"></span><dl> <dt>**HKEY- \_ Klassen Stamm \_**</dt> </dl>             | 0<br/> |
| <span id="HKEY_CURRENT_USER"></span><span id="hkey_current_user"></span><dl> <dt>**Aktueller HKEY- \_ \_ Benutzer**</dt> </dl>             | 1<br/> |
| <span id="HKEY_LOCAL_MACHINE"></span><span id="hkey_local_machine"></span><dl> <dt>**lokaler HKEY- \_ \_ Computer**</dt> </dl>          | 2<br/> |
| <span id="HKEY_USERS"></span><span id="hkey_users"></span><dl> <dt>**HKEY- \_ Benutzer**</dt> </dl>                                   | 3<br/> |
| <span id="HKEY_PERFORMANCE_DATA"></span><span id="hkey_performance_data"></span><dl> <dt>**HKEY- \_ Leistungs \_ Daten**</dt> </dl> | 4<br/> |
| <span id="HKEY_CURRENT_CONFIG"></span><span id="hkey_current_config"></span><dl> <dt>**aktuelle HKEY- \_ \_ Konfiguration**</dt> </dl>       | 5<br/> |
| <span id="HKEY_DYN_DATA"></span><span id="hkey_dyn_data"></span><dl> <dt>**HKEY- \_ dyn- \_ Daten**</dt> </dl>                         | 6<br/> |



 

</dd> <dt>

*key* 
</dt> <dd>

Eine Zeichenfolge, die den gesamten Schlüssel Pfad aus dem Stamm enthält.

</dd> <dt>

*value* 
</dt> <dd>

Dieser optionale Parameter legt fest, welcher zugeordnete Wert für den angegebenen Schlüssel zurückgegeben werden soll. Der Wert ist einer der Werte, die in der folgenden Tabelle angezeigt werden.



| Wert                                                                                                                                                                                                    | Bedeutung                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Missing_or_blank"></span><span id="missing_or_blank"></span><span id="MISSING_OR_BLANK"></span><dl> <dt>**Fehlt oder ist leer.**</dt> </dl> | Gibt einen booleschen Wert zurück, der angibt, ob der Schlüssel vorhanden ist.<br/>                                                                                        |
| <span id="String"></span><span id="string"></span><span id="STRING"></span><dl> <dt>**Schnür**</dt> </dl>                                         | Gibt die dem benannten Wert zugeordneten Daten zurück, schlägt fehl, wenn der Wertname nicht vorhanden ist.<br/>                                                   |
| <span id="Positive_integer"></span><span id="positive_integer"></span><span id="POSITIVE_INTEGER"></span><dl> <dt>**Positive ganze Zahl**</dt> </dl> | Gibt den 1-basierten enumerationswertnamen zurück, wenn er nicht vorhanden ist. Diese Option verwendet die Funktion " [**regenenvalue**](/windows/win32/api/winreg/nf-winreg-regenumvaluea) ".<br/> |
| <span id="Negative_integer"></span><span id="negative_integer"></span><span id="NEGATIVE_INTEGER"></span><dl> <dt>**Negative Ganzzahl**</dt> </dl> | Gibt den 1-basierten enumerierten Unterschlüssel Namen zurück. dieser ist leer, wenn er nicht vorhanden ist. Diese Option verwendet die Funktion " [**regenenkey**](/windows/win32/api/winreg/nf-winreg-regenumkeya) ".<br/>  |
| <span id="Zero_integer"></span><span id="zero_integer"></span><span id="ZERO_INTEGER"></span><dl> <dt>**0 (null)**</dt> </dl>                 | Gibt den Namen der Zeichen folgen Klasse für den angegebenen Schlüssel zurück.<br/>                                                                                        |
| <span id="Empty_string____"></span><span id="empty_string____"></span><span id="EMPTY_STRING____"></span><dl> <dt>**Leere Zeichenfolge ""**</dt> </dl> | Gibt den Standardwert des Registrierungsschlüssels zurück.<br/>                                                                                               |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 
