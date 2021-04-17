---
title: Win32_TSLicenseKeyPack-Klasse
description: Stellt Methoden und Eigenschaften zum Anzeigen und installieren Remotedesktopdienste Lizenzschlüssel Packs bereit.
ms.assetid: 27450646-c51f-4911-bb42-410794e32003
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseKeyPack-Klasse Remotedesktopdienste
- Win32_TSLicenseKeyPack Klasse Remotedesktopdienste, beschrieben
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
ms.openlocfilehash: 9d78af398ebf7c137be5b31c9db427691a66a7a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517402"
---
# <a name="win32_tslicensekeypack-class"></a>Win32- \_ Klasse "slicenabkeypack"

Stellt Methoden und Eigenschaften zum Anzeigen und installieren Remotedesktopdienste Lizenzschlüssel Packs bereit.

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

Die Win32-Klasse " **\_ zlicentarkeypack** " verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die Win32-Klasse " **\_ zlicenabkeypack** " verfügt über diese Methoden.



| Methode                                                                                                        | BESCHREIBUNG                                                                                                                                                                                                                               |
|:--------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Convertlicenses**](convertlicenses-win32-tslicensekeypack.md)                                             | Konvertiert die Lizenzen im aktuellen Schlüssel Paket.<br/>                                                                                                                                                                                 |
| [**Importagreementlicenskeypack**](win32-tslicensekeypack-importagreementlicensekeypack.md)                 | Importe von einem anderen Remotedesktop Lizenzserver, ein Remotedesktopdienste Lizenzschlüssel Paket, das über einen Lizenzvertrag gekauft wurde, und die automatische Verbindung über das Internet, um die Key Pack-Lizenz zu überprüfen.<br/> |
| [**Importlicenabkeypackoffline**](win32-tslicensekeypack-importlicensekeypackoffline.md)                     | Importe von einem anderen Remotedesktop Lizenzserver, ein Remotedesktopdienste License Key Pack, das eine Lizenz-ID verwendet, die über das Internet oder das Telefon empfangen wurde.<br/>                                               |
| [**Importopenpurchaselicenabkeypack**](win32-tslicensekeypack-importopenpurchaselicensekeypack.md)           | Importe von einem anderen Remotedesktop Lizenzserver, einem Open License Remotedesktopdienste License Key Pack.<br/>                                                                                                                 |
| [**Importretailpurchaselicenzkeypack**](win32-tslicensekeypack-importretailpurchaselicensekeypack.md)       | Importe von einem anderen Remotedesktop Lizenzserver, ein Remotedesktopdienste Lizenzschlüssel Paket, das über einen einzelhandelskanal gekauft wurde.<br/>                                                                                   |
| [**Installagreementlicenskeypack**](installagreementlicensekeypack-win32-tslicensekeypack.md)               | Installiert ein Remotedesktopdienste Lizenzschlüssel Paket, das über eine Vertrags Lizenz erworben wurde.<br/>                                                                                                                           |
| [**Installlicenskeypack**](installlicensekeypack-win32-tslicensekeypack.md)                                 | Installiert ein Remotedesktopdienste Lizenzschlüssel Paket, das eine Lizenzschlüssel Paket-ID verwendet, die über das Internet oder das Telefon empfangen wurde.<br/>                                                                                          |
| [**Installopenlicenskeypack**](installopenlicensekeypack-win32-tslicensekeypack.md)                         | Installiert ein Remotedesktopdienste Lizenzschlüssel Paket, das über einen offenen Lizenzvertrag gekauft wurde.<br/>                                                                                                                      |
| [**Installretailpurchaselicen\keypack**](installretailpurchaselicensekeypack-win32-tslicensekeypack.md)     | Installiert ein Remotedesktopdienste Lizenzschlüssel Paket, das über einen Einzelhandels Speicher gekauft wurde.<br/>                                                                                                                                 |
| [**Reinstallagreementlicenskeypack**](win32-tslicensekeypack-reinstallagreementlicensekeypack.md)           | Installiert ein Remotedesktopdienste Lizenzschlüssel Paket neu, das über einen Lizenzvertrag gekauft wurde, und stellt automatisch eine Verbindung über das Internet her, um die Key Pack-Lizenz zu überprüfen.<br/>                                           |
| [**Reinstalllicenumkeypackoffline**](win32-tslicensekeypack-reinstalllicensekeypackoffline.md)               | Installiert ein Remotedesktopdienste Lizenzschlüssel Paket, das die über das Internet oder das Telefon empfangene Lizenz-ID verwendet.<br/>                                                                                       |
| [**Reinstallopenpurchaselicenskeypack**](win32-tslicensekeypack-reinstallopenpurchaselicensekeypack.md)     | Installiert ein Open License Remotedesktopdienste License Key Pack neu.<br/>                                                                                                                                                           |
| [**Reinstallretailpurchaselicen\keypack**](win32-tslicensekeypack-reinstallretailpurchaselicensekeypack.md) | Neuinstallation eines Remotedesktopdienste Lizenzschlüssel Pakets, das über einen einzelhandelskanal gekauft wurde.<br/>                                                                                                                             |
| [**Removelicenseswithidcount**](win32-tslicensekeypack-removelicenseswithidcount.md)                         | Entfernt die angegebene Anzahl von Remotedesktopdienste Lizenzen aus dem angegebenen Schlüssel Paket.<br/>                                                                                                                                  |
| [**Uninstalllicenabkeypack**](win32-tslicensekeypack-uninstalllicensekeypack.md)                             | Deinstalliert ein Remotedesktopdienste License Key Pack.<br/>                                                                                                                                                                         |
| [**Uninstalllicenabkeypackwithid**](win32-tslicensekeypack-uninstalllicensekeypackwithid.md)                 | Deinstalliert das Remotedesktopdienste License Key Pack mit der angegebenen Key Pack-Kennung.<br/>                                                                                                                                |



 

### <a name="properties"></a>Eigenschaften

Die Win32-Klasse " **\_ slicenabkeypack** " verfügt über diese Eigenschaften.

<dl> <dt>

**AccessRights**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Bitmap**](/windows/desktop/WmiSdk/standard-qualifiers) ("0", "1", "2", "3"), [**BitValues**](/windows/desktop/WmiSdk/standard-qualifiers) ("RD-Sitzung", "VDI-Sitzung", "Calista", "VDI-Partner")
</dt> </dl>

Qualifizierer für Terminaldienstelizenzierungs-Schlüssel Paket

</dd> <dt>

**Availablelicenses**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Gesamtanzahl der verfügbaren Lizenzen im Remotedesktopdienste License Key Pack.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Beschreibung des Remotedesktopdienste License Key Pack.

</dd> <dt>

**ExpirationDate**
</dt> <dd> <dl> <dt>

**[Datentyp: DateTime](/windows/desktop/WmiSdk/datetime)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Ablaufdatum des Remotedesktopdienste License Key Pack.

</dd> <dt>

**Issuedlicenses**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Gesamtanzahl der ausgestellten Lizenzen im Remotedesktopdienste License Key Pack.

</dd> <dt>

**Keypackid**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Bezeichner für das Remotedesktopdienste License Key Pack.

</dd> <dt>

**Keypacktype**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Typ des Schlüssel Pakets für den Remotedesktop-Lizenzserver.

| Wert | BESCHREIBUNG |
|-------|-------------|
| 0 | Der Typ Remotedesktopdienste License Key Pack ist unbekannt. |
| 1 | Der Typ der Remotedesktopdienste License Key Pack ist ein Einzelhandels Einkauf. |
| 2 | Der Typ Remotedesktopdienste License Key Pack ist ein Volume Purchase. |
| 3 | Der Remotedesktopdienste License Key Pack-Typ ist eine gleichzeitige Lizenz. |
| 4 | Der Typ Remotedesktopdienste License Key Pack ist temporär. |
| 5 | Der Remotedesktopdienste License Key Pack-Typ ist eine offene Lizenz. |
| 6 | Wird nicht unterstützt. |

**ProductType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Produkttyp des Remotedesktopdienste License Key Pack.

| Wert | BESCHREIBUNG |
|-------|-------------|
| 0 | Der Produkttyp Remotedesktopdienste License Key Pack ist pro Gerät. Daher muss jedes Gerät, das eine Verbindung mit dem RD-Sitzungshost Server herstellt, über eine Lizenz verfügen. |
| 1 | Der Product Type für Remotedesktopdienste License Key Pack ist pro Benutzer. Daher muss jeder Benutzer, der eine Verbindung mit dem RD-Sitzungshost Server herstellt, über eine Lizenz verfügen. |
| 2 | Der Produkttyp ist ungültig. |

**ProductVersion**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Produktversion für das Remotedesktopdienste License Key Pack.

| Wert | BESCHREIBUNG |
|-------|-------------|
| "Windows Server 2012" | Nur Server, auf denen Windows Server 2012, Windows Server 2008 R2 oder Windows Server 2008 ausgeführt wird, werden mit dieser Lizenz unterstützt. |
| "Windows Server 7" | Nur Server, auf denen Windows Server 2008 R2 oder Windows Server 2008 ausgeführt wird, werden mit dieser Lizenz unterstützt. |
| "Windows Server 2008" | Nur Server, auf denen Windows Server 2008 ausgeführt wird, werden von diesem Schlüssel Paket unterstützt. |

**Productversionid**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Produkt Versions Kennung für das Remotedesktopdienste License Key Pack.

| Wert | BESCHREIBUNG |
|-------|-------------|
| 0 | Nicht unterstützt |
| 1 | Nicht unterstützt |
| 2 | Windows Server 2008 |
| 3 | Windows Server 2008 R2 |
| 4 | Windows Server 2012/Windows Server 2012 R2 |
| 5 | Windows Server 2016 |
| 6 | Windows Server 2019 |

**Totallicenses**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Gesamtanzahl der Lizenzen im Remotedesktopdienste License Key Pack.

</dd> <dt>

**Typeandmodel**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Qualifizierer für Terminaldienstelizenzierungs-Key Pack-Typ Beispiele: VDI pro Geräte Abonnementlizenz, TS pro Benutzer-CAL

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

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

[**Win32-Datei- \_ /licensereport**](win32-tslicensereport.md)
</dt> <dt>

[**Win32-Wert für "- \_ Lizenzserver"**](win32-tslicensereportentry.md)
</dt> <dt>

[**Win32- \_ Lizenznehmer**](win32-tslicenseserver.md)
</dt> </dl>

 

