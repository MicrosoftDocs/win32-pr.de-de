---
title: Win32_TSLicenseReport-Klasse
description: Stellt Instanzen der Clientzugriffslizenz Remotedesktopdienste pro Benutzer bereit (RDS \ 160; Nutzungsberichte pro Benutzer-CAL), die auf dem Remotedesktop Lizenzserver generiert werden, sowie Methoden zum Generieren, Abrufen und Löschen von Lizenzberichten.
ms.assetid: 8d67f158-cda3-4cf4-a766-09d08c21c49e
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReport-Klasse Remotedesktopdienste
- Win32_TSLicenseReport-Klasse Remotedesktopdienste beschrieben
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport
- Win32_TSLicenseReport.FileName
- Win32_TSLicenseReport.LicenseUsageCount
- Win32_TSLicenseReport.InstalledLicenses
- Win32_TSLicenseReport.GenerationDateTime
- Win32_TSLicenseReport.ScopeType
- Win32_TSLicenseReport.ScopeValue
- Win32_TSLicenseReport.Version
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93280c00cbd20993907901e1f9b8c16330863a47bddd4e08bc86d51b4b837233
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137833"
---
# <a name="win32_tslicensereport-class"></a>Win32 \_ TSLicenseReport-Klasse

Stellt Instanzen von Nutzungsberichten Remotedesktopdienste Clientzugriffslizenz pro Benutzer (RDS per User CAL) bereit, die auf dem Remotedesktop Lizenzserver generiert werden, sowie Methoden zum Generieren, Abrufen und Löschen von Lizenzberichten.

## <a name="syntax"></a>Syntax

``` syntax
[dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSLicenseReport
{
  string   FileName;
  uint32   LicenseUsageCount;
  uint32   InstalledLicenses;
  DATETIME GenerationDateTime;
  uint32   ScopeType;
  string   ScopeValue;
  uint32   Version;
};
```

## <a name="members"></a>Member

Die **Win32 \_ TSLicenseReport-Klasse** verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ TSLicenseReport-Klasse** verfügt über diese Methoden.



| Methode                                                                                                         | Beschreibung                                                                                                                                                                                     |
|:---------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DeleteReport**](deletereport-win32-tslicensereport.md)                                                     | Löscht ein Berichtsobjekt auf dem Remotedesktop Lizenzserver. Dies ist keine statische Methode.<br/>                                                                                           |
| [**FetchReportEntries**](fetchreportentries-win32-tslicensereport.md)                                         | Ruft Einträge im Berichtsobjekt ab.<br/>                                                                                                                                              |
| [**FetchReportFailedPerUserEntries**](fetchreportfailedperuserentries-win32-tslicensereport.md)               | Ruft Details zu fehlgeschlagenen Remotedesktopdienste Clientzugriffslizenzen pro Benutzer (RDS pro Benutzer-CALs) aus dem Bericht ab.<br/>                                                             |
| [**FetchReportFailedPerUserSummaryEntries**](fetchreportfailedperusersummaryentries-win32-tslicensereport.md) | Ruft zusammenfassende Informationen zu fehlgeschlagenen Remotedesktopdienste Clientzugriffslizenzen pro Benutzer (RDS pro Benutzer-CALs) aus dem Bericht ab.<br/>                                                 |
| [**FetchReportPerDeviceEntries**](fetchreportperdeviceentries-win32-tslicensereport.md)                       | Ruft Informationen zu ausgestellten Remotedesktopdienste Clientzugriffslizenzen pro Gerät (RDS per Device CALs) aus dem Bericht ab.<br/>                                                     |
| [**FetchReportSummaryEntries**](win32-tslicensereport-fetchreportsummaryentries.md)                           | Ruft Lizenzzusammenfassungen aus dem Berichtsobjekt ab.<br/>                                                                                                                                  |
| [**GenerateReport**](generatereport-win32-tslicensereport.md)                                                 | Diese Methode wird nicht unterstützt.<br/> **Windows Server 2008 R2 und Windows Server 2008:** Generiert einen aktuellen Benutzerlizenznutzungsbericht auf dem Remotedesktop Lizenzserver.<br/> |
| [**GenerateReportEx**](generatereportex-win32-tslicensereport.md)                                             | Generiert einen aktuellen Benutzerlizenznutzungsbericht auf dem Remotedesktop Lizenzserver.<br/>                                                                                              |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ TSLicenseReport-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Der Berichtsname.

</dd> <dt>

**GenerationDateTime**
</dt> <dd> <dl> <dt>

Datentyp: **[DATETIME](/windows/desktop/WmiSdk/datetime)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Datum und Uhrzeit der Erstellung des RD-Lizenzierungsberichts.

</dd> <dt>

**InstalledLicenses**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **VERALTET**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Diese Eigenschaft wird nicht unterstützt.

**Windows Server 2008 R2 und Windows Server 2008:** Anzahl der installierten RDS-CALs pro Benutzer.

</dd> <dt>

**LicenseUsageCount**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **VERALTET**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Diese Eigenschaft wird nicht unterstützt.

**Windows Server 2008 R2 und Windows Server 2008:** Anzahl der RDS-CALs pro Benutzer, die derzeit verwendet werden.

</dd> <dt>

**ScopeType**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **VERALTET**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Diese Eigenschaft wird nicht unterstützt.

**Windows Server 2008 R2 und Windows Server 2008:** Bereichstyp des RD-Lizenzierungsberichts.

</dd> <dt>

**ScopeValue**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **VERALTET**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Diese Eigenschaft wird nicht unterstützt.

**Windows Server 2008 R2 und Windows Server 2008:** Wert des Rd-Lizenzierungsberichtsbereichs.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Version des RD-Lizenzierungsberichts.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Berichte, die mithilfe von WMI generiert werden, werden im RD-Lizenzierungs-Manager angezeigt. Berichte, die mithilfe von WMI gelöscht werden, werden ebenfalls aus dem RD-Lizenzierungs-Manager gelöscht.

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Klasse verwenden zu können.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                            |
| Namespace<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TSIssuedLicense**](win32-tsissuedlicense.md)
</dt> <dt>

[**Win32 \_ TSLicenseKeyPack**](win32-tslicensekeypack.md)
</dt> <dt>

[**Win32 \_ TSLicenseReportEntry**](win32-tslicensereportentry.md)
</dt> <dt>

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> </dl>

 

