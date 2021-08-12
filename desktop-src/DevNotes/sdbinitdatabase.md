---
description: Öffnet die Shim-Datenbank.
ms.assetid: ece1bd39-20a1-42e6-8e2b-1d38f7223d42
title: SdbInitDatabase-Funktion
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
ms.openlocfilehash: 0504b12254658250820cb3ecac3e9e47ee2a6ca242b15600fa69241b597bb0dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118666381"
---
# <a name="sdbinitdatabase-function"></a>SdbInitDatabase-Funktion

Öffnet die Shim-Datenbank.

## <a name="syntax"></a>Syntax


```C++
HSDB WINAPI SdbInitDatabase(
  _In_ DWORD   dwFlags,
  _In_ LPCTSTR pszDatabasePath
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Dieser Parameter gibt das Format des Pfads im *pszDatabasePath-Parameter* an. Dieses Argument einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                                                      | Bedeutung                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span id="HID_DOS_PATHS"></span><span id="hid_dos_paths"></span><dl> <dt>**HID \_ \_DOS-PFADE**</dt> <dt>0x00000001</dt> </dl>                             | Ein MS-DOS-Stilpfad.<br/>                                                                       |
| <span id="HID_DATABASE_FULLPATH"></span><span id="hid_database_fullpath"></span><dl> <dt>**HID \_ DATABASE \_ FULLPATH-0x00000002**</dt> <dt></dt> </dl>     | Ein vollständiger Pfad.<br/>                                                                                |
| <span id="HID_NO_DATABASE"></span><span id="hid_no_database"></span><dl> <dt>**HID \_ NO \_ DATABASE**</dt> <dt>0x00000004</dt> </dl>                       | Der *pszDatabasePath-Parameter* wird ignoriert, und es wird keine Datenbank geöffnet.<br/>                       |
| <span id="HID_DATABASE_TYPE_MASK"></span><span id="hid_database_type_mask"></span><dl> <dt>**HID \_ DATABASE \_ TYPE \_ MASK**</dt> <dt>0xF00F0000</dt> </dl> | Dieser Parameter gibt eine vordefinierte Datenbank an. Der *pszDatabasePath-Parameter* wird ignoriert.<br/> |



 

Wenn *dwFlags* **HID DATA TYPE MASK \_ \_ \_ enthält,** kann dieser Parameter auch einen der folgenden Werte enthalten.



| Wert                                                                                                                                                                                                                                                               | Bedeutung                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="SDB_DATABASE_MAIN_SHIM"></span><span id="sdb_database_main_shim"></span><dl> <dt>**SDB \_ DATABASE \_ MAIN \_ SHIM**</dt> <dt>0x80030000</dt> </dl>          | Anwendungss shim-Datenbank.<br/>         |
| <span id="SDB_DATABASE_MAIN_MSI"></span><span id="sdb_database_main_msi"></span><dl> <dt>**SDB \_ \_ \_ DATENBANK-MSI-0X80020000**</dt> <dt></dt> </dl>             | MSI-Datenbank.<br/>                      |
| <span id="SDB_DATABASE_MAIN_DRIVERS"></span><span id="sdb_database_main_drivers"></span><dl> <dt>**SDB \_ \_ \_ DATENBANK-HAUPTTREIBER**</dt> <dt>0X80040000</dt> </dl> | Datenbank mit zu blockierenden Treibern.<br/> |



 

</dd> <dt>

*pszDatabasePath* \[ In\]
</dt> <dd>

Der Pfad zur Datenbank. Dieser Parameter kann NULL **sein,** wenn *der dwFlags-Parameter* eine vordefinierte Datenbank angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt ein Handle an die geöffnete Datenbank zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SdbGetAppPatchDir**](sdbgetapppatchdir.md)
</dt> <dt>

[**SdbGetMatchingExe**](sdbgetmatchingexe.md)
</dt> <dt>

[**SdbReleaseMatchingExe**](sdbreleasematchingexe.md)
</dt> <dt>

[**SdbTagRefToTagID**](sdbtagreftotagid.md)
</dt> </dl>

 

 




