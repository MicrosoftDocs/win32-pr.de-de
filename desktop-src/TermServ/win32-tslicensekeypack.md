---
title: Win32_TSLicenseKeyPack-Klasse
description: Stellt Methoden und Eigenschaften zum Anzeigen und Installieren Remotedesktopdienste Lizenzschlüsselpaketen zur Auswahl.
ms.assetid: 27450646-c51f-4911-bb42-410794e32003
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseKeyPack der Remotedesktopdienste
- Win32_TSLicenseKeyPack klasse Remotedesktopdienste , beschrieben
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack.KeyPackId
- Win32_TSLicenseKeyPack.Description
- Win32_TSLicenseKeyPack.KeyPackType
- Win32_TSLicenseKeyPack.ProductType
- Win32_TSLicenseKeyPack.ProductVersion
- Win32_TSLicenseKeyPack.ProductVersionID
- Win32_TSLicenseKeyPack.TotalLicenses
- Win32_TSLicenseKeyPack.IssuedLicenses
- Win32_TSLicenseKeyPack.AvailableLicenses
- Win32_TSLicenseKeyPack.ExpirationDate
- Win32_TSLicenseKeyPack.AccessRights
- Win32_TSLicenseKeyPack.TypeAndModel
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7927270f262d0a66722660bf4b2c8f15cf75f49bb807abcff604af9edf58d99b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137813"
---
# <a name="win32_tslicensekeypack-class"></a>Win32 \_ TSLicenseKeyPack-Klasse

Stellt Methoden und Eigenschaften zum Anzeigen und Installieren Remotedesktopdienste Lizenzschlüsselpaketen zur Auswahl.

## <a name="syntax"></a>Syntax

``` syntax
[dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSLicenseKeyPack
{
  uint32   KeyPackId;
  string   Description;
  uint32   KeyPackType;
  uint32   ProductType;
  string   ProductVersion;
  uint32   ProductVersionID;
  uint32   TotalLicenses;
  uint32   IssuedLicenses;
  uint32   AvailableLicenses;
  DATETIME ExpirationDate;
  uint32   AccessRights;
  string   TypeAndModel;
};
```

## <a name="members"></a>Member

Die **Win32 \_ TSLicenseKeyPack-Klasse** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ TSLicenseKeyPack-Klasse** verfügt über diese Methoden.



| Methode                                                                                                        | Beschreibung                                                                                                                                                                                                                               |
|:--------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ConvertLicenses**](convertlicenses-win32-tslicensekeypack.md)                                             | Konvertiert die Lizenzen im aktuellen Schlüsselpaket.<br/>                                                                                                                                                                                 |
| [**ImportAgreementLicenseKeyPack**](win32-tslicensekeypack-importagreementlicensekeypack.md)                 | Importiert von einem anderen Remotedesktop-Lizenzserver ein Remotedesktopdienste-Lizenzschlüsselpaket, das über einen Lizenzvertrag erworben wurde, und stellt automatisch eine Verbindung über das Internet zur Überprüfung der Key Pack-Lizenz sicher.<br/> |
| [**ImportLicenseKeyPackOffline**](win32-tslicensekeypack-importlicensekeypackoffline.md)                     | Importiert von einem anderen Remotedesktop-Lizenzserver ein Remotedesktopdienste-Lizenzschlüsselpaket, das eine Lizenz-ID verwendet, die über das Internet oder das Telefon empfangen wurde.<br/>                                               |
| [**ImportOpenPurchaseLicenseKeyPack**](win32-tslicensekeypack-importopenpurchaselicensekeypack.md)           | Importiert von einem anderen Remotedesktop-Lizenzserver ein Open License Remotedesktopdienste License Key Pack.<br/>                                                                                                                 |
| [**ImportRetailPurchaseLicenseKeyPack**](win32-tslicensekeypack-importretailpurchaselicensekeypack.md)       | Importiert von einem anderen Remotedesktop-Lizenzserver ein Remotedesktopdienste Lizenzschlüsselpaket, das über einen Einzelhandelskanal erworben wurde.<br/>                                                                                   |
| [**InstallAgreementLicenseKeyPack**](installagreementlicensekeypack-win32-tslicensekeypack.md)               | Installiert ein Remotedesktopdienste Lizenzschlüsselpaket, das über eine Vertragslizenz erworben wurde.<br/>                                                                                                                           |
| [**InstallLicenseKeyPack**](installlicensekeypack-win32-tslicensekeypack.md)                                 | Installiert ein Remotedesktopdienste Lizenzschlüsselpaket, das eine Lizenzschlüsselpaket-ID verwendet, die über das Internet oder das Telefon empfangen wurde.<br/>                                                                                          |
| [**InstallOpenLicenseKeyPack**](installopenlicensekeypack-win32-tslicensekeypack.md)                         | Installiert ein Remotedesktopdienste Lizenzschlüsselpaket, das über einen offenen Lizenzvertrag erworben wurde.<br/>                                                                                                                      |
| [**InstallRetailPurchaseLicenseKeyPack**](installretailpurchaselicensekeypack-win32-tslicensekeypack.md)     | Installiert ein Remotedesktopdienste Lizenzschlüsselpaket, das über einen Einzelhandelsgeschäft erworben wurde.<br/>                                                                                                                                 |
| [**ReinstallAgreementLicenseKeyPack**](win32-tslicensekeypack-reinstallagreementlicensekeypack.md)           | Installiert ein Remotedesktopdienste Lizenzschlüsselpaket neu, das über einen Lizenzvertrag erworben wurde, und stellt automatisch eine Verbindung über das Internet zur Überprüfung der Key Pack-Lizenz herstellen.<br/>                                           |
| [**ReinstallLicenseKeyPackOffline**](win32-tslicensekeypack-reinstalllicensekeypackoffline.md)               | Installiert ein Remotedesktopdienste Lizenzschlüsselpaket neu, das die Lizenz-ID verwendet, die über das Internet oder das Telefon empfangen wurde.<br/>                                                                                       |
| [**ReinstallOpenPurchaseLicenseKeyPack**](win32-tslicensekeypack-reinstallopenpurchaselicensekeypack.md)     | Installiert ein Open License Remotedesktopdienste Lizenzschlüsselpaket neu.<br/>                                                                                                                                                           |
| [**ReinstallRetailPurchaseLicenseKeyPack**](win32-tslicensekeypack-reinstallretailpurchaselicensekeypack.md) | Neuinstallation eines Remotedesktopdienste Lizenzschlüsselpakets, das über einen Einzelhandelskanal erworben wurde.<br/>                                                                                                                             |
| [**RemoveLicensesWithIdCount**](win32-tslicensekeypack-removelicenseswithidcount.md)                         | Entfernt die angegebene Anzahl Remotedesktopdienste Lizenzen aus dem angegebenen Key Pack.<br/>                                                                                                                                  |
| [**UninstallLicenseKeyPack**](win32-tslicensekeypack-uninstalllicensekeypack.md)                             | Deinstalliert ein Remotedesktopdienste Lizenzschlüsselpaket.<br/>                                                                                                                                                                         |
| [**UninstallLicenseKeyPackWithId**](win32-tslicensekeypack-uninstalllicensekeypackwithid.md)                 | Deinstalliert das Remotedesktopdienste Lizenzschlüsselpaket mit dem angegebenen Schlüsselpaketbezeichner.<br/>                                                                                                                                |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ TSLicenseKeyPack-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AccessRights**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**BitMap**](/windows/desktop/WmiSdk/standard-qualifiers) ("0", "1", "2", "3"), [**BitValues**](/windows/desktop/WmiSdk/standard-qualifiers) ("RD Session", "VDI Session", "Calzuordnung", "VDI Partners")
</dt> </dl>

Qualifizierer für ZUGRIFFsrechte des TS-Lizenzierungsschlüsselpakets

</dd> <dt>

**AvailableLicenses**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gesamtanzahl der verfügbaren Lizenzen im Remotedesktopdienste Lizenzschlüsselpaket.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Beschreibung des Remotedesktopdienste Lizenzschlüsselpakets.

</dd> <dt>

**ExpirationDate**
</dt> <dd> <dl> <dt>

Datentyp: **[DATETIME](/windows/desktop/WmiSdk/datetime)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Ablaufdatum des Remotedesktopdienste Lizenzschlüsselpakets.

</dd> <dt>

**IssuedLicenses**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gesamtanzahl der ausgestellten Lizenzen im Remotedesktopdienste Lizenzschlüsselpaket.

</dd> <dt>

**KeyPackId**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Bezeichner für das Remotedesktopdienste Lizenzschlüsselpaket.

</dd> <dt>

**KeyPackType**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Typ des Schlüsselpakets für den Remotedesktop Lizenzserver.

| Wert | Beschreibung |
|-------|-------------|
| 0 | Der Remotedesktopdienste Lizenzschlüsselpakettyp ist unbekannt. |
| 1 | Der Remotedesktopdienste Lizenzschlüsselpakettyp ist ein Einzelhandelskauf. |
| 2 | Der Remotedesktopdienste Lizenzschlüsselpakettyp ist ein Volumenkauf. |
| 3 | Der Remotedesktopdienste Lizenzschlüsselpakettyp ist eine gleichzeitige Lizenz. |
| 4 | Der Remotedesktopdienste Lizenzschlüsselpakettyp ist temporär. |
| 5 | Der Remotedesktopdienste Lizenzschlüsselpakettyp ist eine offene Lizenz. |
| 6 | Wird nicht unterstützt. |

**ProductType**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Produkttyp des Remotedesktopdienste Lizenzschlüsselpakets.

| Wert | Beschreibung |
|-------|-------------|
| 0 | Der Produkttyp Remotedesktopdienste Lizenzschlüsselpakets ist pro Gerät. Daher muss jedes Gerät, das eine Verbindung mit dem RD-Sitzungshost-Server herstellt, über eine Lizenz verfügen. |
| 1 | Der Produkttyp Remotedesktopdienste Lizenzschlüsselpakets ist pro Benutzer. Daher muss jeder Benutzer, der eine Verbindung mit dem RD-Sitzungshost-Server herstellt, über eine Lizenz verfügen. |
| 2 | Dieser Produkttyp ist ungültig. |

**ProductVersion**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Produktversion für das Remotedesktopdienste Lizenzschlüsselpaket.

| Wert | Beschreibung |
|-------|-------------|
| "Windows Server 2012" | Mit dieser Lizenz werden nur Server unterstützt, auf denen Windows Server 2012, Windows Server 2008 R2 oder Windows Server 2008 ausgeführt wird. |
| "Windows Server 7" | Mit dieser Lizenz werden nur Server unterstützt, auf denen Windows Server 2008 R2 oder Windows Server 2008 ausgeführt wird. |
| "Windows Server 2008" | Dieses Schlüsselpaket unterstützt nur Server, auf denen Windows Server 2008 ausgeführt wird. |

**ProductVersionID**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Produktversionsbezeichner für das Remotedesktopdienste Lizenzschlüsselpaket.

| Wert | Beschreibung |
|-------|-------------|
| 0 | Nicht unterstützt |
| 1 | Nicht unterstützt |
| 2 | Windows Server 2008 |
| 3 | Windows Server 2008 R2 |
| 4 | Windows Server 2012/Windows Server 2012 R2 |
| 5 | Windows Server 2016 |
| 6 | Windows Server 2019 |

**TotalLicenses**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gesamtzahl der Lizenzen im Remotedesktopdienste-Lizenzschlüsselpaket.

</dd> <dt>

**TypeAndModel**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Qualifizierer für Schlüsselpakettyp und -modell der TS-Lizenzierung. Beispiele: VDI-Abonnementlizenz pro Gerät, TS pro Benutzer-CAL

</dd> </dl>

## <a name="remarks"></a>Hinweise

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

[**Win32 \_ TSLicenseReport**](win32-tslicensereport.md)
</dt> <dt>

[**Win32 \_ TSLicenseReportEntry**](win32-tslicensereportentry.md)
</dt> <dt>

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> </dl>

 

