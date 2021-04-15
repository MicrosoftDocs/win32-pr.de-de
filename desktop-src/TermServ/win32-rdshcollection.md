---
title: Win32_RDSHCollection-Klasse
description: Verwaltet eine Auflistung von Remotedesktop Sitzungs Hosts.
ms.assetid: 7800bf2e-9497-4e41-aed9-b318748dd83f
ms.tgt_platform: multiple
keywords:
- Win32_RDSHCollection-Klasse Remotedesktopdienste
- Win32_RDSHCollection Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_RDSHCollection
- Win32_RDSHCollection.Alias
- Win32_RDSHCollection.Name
- Win32_RDSHCollection.Description
- Win32_RDSHCollection.Type
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8196747714337890d0b27ef6db8d488eedc32fc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477079"
---
# <a name="win32_rdshcollection-class"></a>Win32 \_ rdshcollection-Klasse

Verwaltet eine Auflistung von Remotedesktop Sitzungs Hosts.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDSHCollection
{
  string Alias;
  string Name;
  string Description;
  uint32 Type;
};
```

## <a name="members"></a>Member

Die **Win32 \_ rdshcollection** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ rdshcollection** -Klasse verfügt über diese Methoden.



| Methode                                                                      | BESCHREIBUNG                                                                                                                                                                                            |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetInt32Property**](getint32property-win32-rdshcollection.md)           | Ruft einen ganzzahligen Eigenschafts Wert eines **Win32- \_ rdshcollection** -Objekts ab.<br/>                                                                                                                  |
| [**GetStringProperty**](getstringproperty-win32-rdshcollection.md)         | Ruft den Wert der Zeichen folgen Eigenschaft eines **Win32- \_ rdshcollection** -Objekts ab.<br/>                                                                                                                    |
| [**Keyvaluecompareandset**](win32-rdshcollection-keyvaluecompareandset.md) | Vergleicht den angegebenen Schlüssel in der Auflistung mit einem comparand. Stimmen Sie zu, wird der Schlüssel auf einen neuen Wert festgelegt. Wenn der Schlüssel nicht vorhanden ist, fügt die Methode den Schlüssel in die Auflistung ein.<br/> |
| [**Keyvaluedelete**](win32-rdshcollection-keyvaluedelete.md)               | Löscht den angegebenen Schlüssel (und zugeordneten Wert) aus der Auflistung.<br/>                                                                                                                       |
| [**Keyvalueget**](win32-rdshcollection-keyvalueget.md)                     | Ruft den Wert ab, der dem angegebenen Schlüssel in der Auflistung zugeordnet ist.<br/>                                                                                                                    |
| [**SetInt32Property**](setint32property-win32-rdshcollection.md)           | Aktualisiert einen ganzzahligen Eigenschafts Wert eines **Win32- \_ rdshcollection** -Objekts.<br/>                                                                                                                    |
| [**SetStringProperty**](setstringproperty-win32-rdshcollection.md)         | Aktualisiert den Wert der Zeichen folgen Eigenschaft eines **Win32- \_ rdshcollection** -Objekts.<br/>                                                                                                                      |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ rdshcollection** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Alias**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ruft den Alias der Auflistung ab und legt ihn fest.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [ **optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Ruft die Beschreibung der Auflistung ab und legt Sie fest.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ruft den Namen der Auflistung ab und legt ihn fest.

</dd> <dt>

**Type**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

**Windows Server 2012 R2 und Windows Server 2012:** Diese Eigenschaft ist vor Windows Server 2016 nicht verfügbar.

Der Typ der Auflistung.

<dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>**Regulär** (0)


</dt> <dd></dd> <dt>



 (2)


</dt> <dd>

Reserviert

</dd> <dt>



 (3)


</dt> <dd>

Reserviert

</dd> <dt>

<span id="ManualPersonal"></span><span id="manualpersonal"></span><span id="MANUALPERSONAL"></span>

<span id="ManualPersonal"></span><span id="manualpersonal"></span><span id="MANUALPERSONAL"></span>**Manualpersonal** (4)


</dt> <dd></dd> <dt>

<span id="AutoPersonal"></span><span id="autopersonal"></span><span id="AUTOPERSONAL"></span>

<span id="AutoPersonal"></span><span id="autopersonal"></span><span id="AUTOPERSONAL"></span>**Autopersonal** (5)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | Root \\ CIMV2 \\ RDMs<br/>                                                                |
| MOF<br/>                      | <dl> <dt>Rdmanagement. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Remotedesktop Management Services-Anbieter](rdms-api-reference.md)
</dt> </dl>

 

