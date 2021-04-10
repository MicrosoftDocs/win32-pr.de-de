---
title: Win32_TSLicenseReport-Klasse
description: Stellt Instanzen von Remotedesktopdienste pro Benutzer-Client Zugriffslizenz bereit (RDS \ 160; Pro Benutzer-CAL) Verwendungs Berichte, die auf dem Remotedesktop-Lizenzserver generiert werden, sowie Methoden zum generieren, abrufen und Löschen von Lizenz Berichten.
ms.assetid: 8d67f158-cda3-4cf4-a766-09d08c21c49e
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReport-Klasse Remotedesktopdienste
- Win32_TSLicenseReport Klasse Remotedesktopdienste, beschrieben
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
ms.openlocfilehash: de997056222c1b525253f320f6fe191f017614f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858696"
---
# <a name="win32_tslicensereport-class"></a>Win32-Klasse "" \_

Stellt Instanzen von Remotedesktopdienste Client Zugriffslizenz-Verwendungs Berichte pro Benutzer (RDS pro Benutzer) bereit, die auf dem Remotedesktop-Lizenzserver generiert werden, sowie Methoden zum generieren, abrufen und Löschen von Lizenz Berichten.

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

Die Win32-Klasse " **\_ zlicensereport** " verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die Win32-Klasse " **\_ zlicensereport** " verfügt über diese Methoden.



| Methode                                                                                                         | BESCHREIBUNG                                                                                                                                                                                     |
|:---------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DeleteReport**](deletereport-win32-tslicensereport.md)                                                     | Löscht ein Berichts Objekt auf dem Remotedesktop-Lizenzserver. Dabei handelt es sich nicht um eine statische Methode.<br/>                                                                                           |
| [**Fetchreportentries**](fetchreportentries-win32-tslicensereport.md)                                         | Ruft Einträge im Berichts Objekt ab.<br/>                                                                                                                                              |
| [**Fetchreportfailedperuserentries**](fetchreportfailedperuserentries-win32-tslicensereport.md)               | Ruft Details der fehlerhaften Remotedesktopdienste pro Benutzer-Client Zugriffs Lizenzen (RDS pro Benutzer-CALs) aus dem Bericht ab.<br/>                                                             |
| [**Fetchreportfailedperusersummaryentries**](fetchreportfailedperusersummaryentries-win32-tslicensereport.md) | Hiermit werden zusammenfassende Informationen zu fehlerhaften Remotedesktopdienste pro Benutzer-Client Zugriffs Lizenzen (RDS pro Benutzer-CALs) aus dem Bericht abgerufen.<br/>                                                 |
| [**Fetchreportperdeviceentries**](fetchreportperdeviceentries-win32-tslicensereport.md)                       | Ruft Informationen zu ausgestellten Remotedesktopdienste pro Geräte-Client Zugriffs Lizenzen (RDS pro Gerät CALs) aus dem Bericht ab.<br/>                                                     |
| [**Fetchreportsummaryentries**](win32-tslicensereport-fetchreportsummaryentries.md)                           | Ruft Lizenz Zusammenfassungen aus dem Berichts Objekt ab.<br/>                                                                                                                                  |
| [**GenerateReport**](generatereport-win32-tslicensereport.md)                                                 | Diese Methode wird nicht unterstützt.<br/> **Windows Server 2008 R2 und Windows Server 2008:** Generiert einen aktuellen Bericht pro Benutzer-Lizenz Verwendung auf dem Remotedesktop-Lizenzserver.<br/> |
| [**Generatereportex**](generatereportex-win32-tslicensereport.md)                                             | Generiert einen aktuellen Bericht pro Benutzer-Lizenz Verwendung auf dem Remotedesktop-Lizenzserver.<br/>                                                                                              |



 

### <a name="properties"></a>Eigenschaften

Die Win32-Klasse " **\_ slicensereport** " verfügt über diese Eigenschaften.

<dl> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Der Name des Berichts.

</dd> <dt>

**Generationdatetime**
</dt> <dd> <dl> <dt>

**[Datentyp: DateTime](/windows/desktop/WmiSdk/datetime)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

RD-Lizenzierung Datum und Uhrzeit der Berichtsgenerierung.

</dd> <dt>

**Installedlicenses**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Diese Eigenschaft wird nicht unterstützt.

**Windows Server 2008 R2 und Windows Server 2008:** Anzahl der installierten RDS-pro-Benutzer-CALs.

</dd> <dt>

**Licenseusagecount**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Diese Eigenschaft wird nicht unterstützt.

**Windows Server 2008 R2 und Windows Server 2008:** Anzahl der RDS-Client Zugriffs Lizenzen pro Benutzer, die zurzeit verwendet werden.

</dd> <dt>

**ScopeType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Diese Eigenschaft wird nicht unterstützt.

**Windows Server 2008 R2 und Windows Server 2008:** RD-Lizenzierung Berichts Bereichstyp.

</dd> <dt>

**Bereich**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Diese Eigenschaft wird nicht unterstützt.

**Windows Server 2008 R2 und Windows Server 2008:** RD-Lizenzierung Berichts Bereichs Wert.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

RD-Lizenzierung Berichts Version.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Berichte, die mithilfe von WMI generiert werden, werden in RD-Lizenzierungs-Manager angezeigt. Berichte, die mithilfe von WMI gelöscht werden, werden auch aus RD-Lizenzierungs-Manager gelöscht.

Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Klasse verwenden zu können.

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                            |
| Namespace<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>Tltaumiprov. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32-" \_ tsissuedlicense"**](win32-tsissuedlicense.md)
</dt> <dt>

[**Win32-Schlüssel-Lizenz-Schlüssel \_ ACK**](win32-tslicensekeypack.md)
</dt> <dt>

[**Win32-Wert für "- \_ Lizenzserver"**](win32-tslicensereportentry.md)
</dt> <dt>

[**Win32- \_ Lizenznehmer**](win32-tslicenseserver.md)
</dt> </dl>

 

