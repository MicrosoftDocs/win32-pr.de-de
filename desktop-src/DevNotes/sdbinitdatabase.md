---
description: Öffnet die Shimdatenbank.
ms.assetid: ece1bd39-20a1-42e6-8e2b-1d38f7223d42
title: Sdbinitdatabase-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbInitDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 7a3c63fa712aec988dbf13c4fb7f9fddbf159fdd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482894"
---
# <a name="sdbinitdatabase-function"></a>Sdbinitdatabase-Funktion

Öffnet die Shimdatenbank.

## <a name="syntax"></a>Syntax


```C++
HSDB WINAPI SdbInitDatabase(
  _In_ DWORD   dwFlags,
  _In_ LPCTSTR pszDatabasePath
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Dieser Parameter gibt das Format des Pfads im *pszdatabasepath* -Parameter an. Dieses Argument einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                                                      | Bedeutung                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span id="HID_DOS_PATHS"></span><span id="hid_dos_paths"></span><dl> <dt>**Versteckt \_ DOS- \_ Pfade**</dt> <dt>0x00000001</dt> </dl>                             | Ein MS-DOS-stilpfad.<br/>                                                                       |
| <span id="HID_DATABASE_FULLPATH"></span><span id="hid_database_fullpath"></span><dl> <dt>**Versteckt \_ Daten Bank \_ Vollständiger Pfad**</dt> <dt>0x00000002</dt> </dl>     | Ein vollständiger Pfad.<br/>                                                                                |
| <span id="HID_NO_DATABASE"></span><span id="hid_no_database"></span><dl> <dt>**Versteckt \_ Keine \_ Datenbank**</dt> <dt>0x00000004</dt> </dl>                       | Der *pszdatabasepath* -Parameter wird ignoriert, und es wird keine Datenbank geöffnet.<br/>                       |
| <span id="HID_DATABASE_TYPE_MASK"></span><span id="hid_database_type_mask"></span><dl> <dt>**Versteckt \_ Datenbank \_ - \_ typmaske**</dt> <dt>0xF 00F 0000</dt> </dl> | Dieser Parameter gibt eine vordefinierte Datenbank an. Der *pszdatabasepath* -Parameter wird ignoriert.<br/> |



 

Wenn *dwFlags* eine **versteckte \_ \_ Datentyp \_ Maske** enthält, kann dieser Parameter auch einen der folgenden Werte enthalten.



| Wert                                                                                                                                                                                                                                                               | Bedeutung                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="SDB_DATABASE_MAIN_SHIM"></span><span id="sdb_database_main_shim"></span><dl> <dt>**SDB \_ Datenbank- \_ Haupt- \_ Shim**</dt> <dt>0x80030000</dt> </dl>          | Anwendungsshimdatenbank.<br/>         |
| <span id="SDB_DATABASE_MAIN_MSI"></span><span id="sdb_database_main_msi"></span><dl> <dt>**SDB \_ Datenbank- \_ Haupt- \_ MSI**</dt> <dt>0x80020000</dt> </dl>             | MSI-Datenbank.<br/>                      |
| <span id="SDB_DATABASE_MAIN_DRIVERS"></span><span id="sdb_database_main_drivers"></span><dl> <dt>**SDB \_ \_Haupt \_ Treiber der Datenbank**</dt> <dt>0x80040000</dt> </dl> | Die Datenbank der zu blockierenden Treiber.<br/> |



 

</dd> <dt>

*pszdatabasepath* \[ in\]
</dt> <dd>

Der Pfad zur Datenbank. Dieser Parameter kann **null** sein, wenn der *dwFlags* -Parameter eine vordefinierte Datenbank angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Funktion gibt ein Handle für die geöffnete Datenbank zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sdbgetapppatchdir**](sdbgetapppatchdir.md)
</dt> <dt>

[**Sdbgetmatchingexe**](sdbgetmatchingexe.md)
</dt> <dt>

[**Sdbreleasematchingexe**](sdbreleasematchingexe.md)
</dt> <dt>

[**Sdbtagrebtotagid**](sdbtagreftotagid.md)
</dt> </dl>

 

 




