---
title: Win32_RDMSCollectionProperties-Klasse
description: Verwaltet die Eigenschaften einer Sammlung virtueller Desktops.
ms.assetid: 8c533284-aa7b-4c47-b0a3-33307c4c805b
ms.tgt_platform: multiple
keywords:
- Win32_RDMSCollectionProperties-Klasse Remotedesktopdienste
- Win32_RDMSCollectionProperties Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_RDMSCollectionProperties
- Win32_RDMSCollectionProperties.Alias
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopName
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopMachineName
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopHost
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopGuid
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopOsversion
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopRamsizeMB
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopArchitecture
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopRemoteFX
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopAdapters
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb7397ccc1afd350689ac1eeb984a62177140f50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391807"
---
# <a name="win32_rdmscollectionproperties-class"></a>Win32 \_ rdmscollectionproperties-Klasse

Verwaltet die Eigenschaften einer Sammlung virtueller Desktops.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSCollectionProperties
{
  string  Alias;
  string  ReferenceVirtualDesktopName;
  string  ReferenceVirtualDesktopMachineName;
  string  ReferenceVirtualDesktopHost;
  string  ReferenceVirtualDesktopGuid;
  string  ReferenceVirtualDesktopOsversion;
  uint32  ReferenceVirtualDesktopRamsizeMB;
  string  ReferenceVirtualDesktopArchitecture;
  boolean ReferenceVirtualDesktopRemoteFX = false;
  string  ReferenceVirtualDesktopAdapters[];
};
```

## <a name="members"></a>Member

Die **Win32 \_ rdmscollectionproperties** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](/windows)

### <a name="methods"></a>Methoden

Die **Win32-Klasse \_ rdmscollectionproperties** verfügt über diese Methoden.



| Methode                                                                                        | BESCHREIBUNG                                                                         |
|:----------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**Getprovisioningproperties**](getprovisioningproperties-win32-rdmscollectionproperties.md) | Ruft die Bereitstellungs Eigenschaften der Sammlung virtueller Desktops ab.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ rdmscollectionproperties** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Alias**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ruft den Alias der Auflistung ab.

</dd> <dt>

**Referencevirtualdesktopadapters**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ruft die Namen der virtuellen Netzwerkadapter der Master-VM ab und legt Sie fest.

</dd> <dt>

**Referencevirtualdesktoparchitecture**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ruft die Prozessorarchitektur der Master-VM ab und legt Sie fest.

</dd> <dt>

**Referencevirtualdesktopguid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ruft die GUID der Master-VM ab und legt Sie fest.

</dd> <dt>

**Referencevirtualdesktophost**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ruft den Namen des Host Servers der Master-VM ab und legt ihn fest.

</dd> <dt>

**Referencevirtualdesktopmachinename**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ruft den Computernamen der Master-VM ab und legt ihn fest.

</dd> <dt>

**Referencevirtualdesktopname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ruft den Namen der Master-VM ab und legt ihn fest.

</dd> <dt>

**Referencevirtualdesktoposversion**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ruft die Betriebssystemversion der Master-VM ab und legt Sie fest.

</dd> <dt>

**Referencevirtualdesktopramsizemb**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ruft die Arbeitsspeicher Größe der Master-VM ab und legt Sie fest.

</dd> <dt>

**Referencevirtualdesktopremotefx**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ruft einen Wert ab, der angibt, ob remotefx für die Master-VM aktiviert ist, oder legt ihn fest. **True** , wenn remotefx aktiviert ist. andernfalls **false**. Der Standardwert für diese Eigenschaft ist **false**.

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

 

