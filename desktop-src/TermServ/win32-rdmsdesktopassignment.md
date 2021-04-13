---
title: Win32_RDMSDesktopAssignment-Klasse
description: Beschreibt die Benutzer Desktop Zuweisung für die RD-Sammlung.
ms.assetid: d3370cf2-65db-4e01-9ea3-9a71340bf71b
ms.tgt_platform: multiple
keywords:
- Win32_RDMSDesktopAssignment-Klasse Remotedesktopdienste
- Win32_RDMSDesktopAssignment Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_RDMSDesktopAssignment
- Win32_RDMSDesktopAssignment.CollectionAlias
- Win32_RDMSDesktopAssignment.DesktopName
- Win32_RDMSDesktopAssignment.UserName
- Win32_RDMSDesktopAssignment.UserDomain
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72bb252bd2efb71e3192ebd16160cecf18196cb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340657"
---
# <a name="win32_rdmsdesktopassignment-class"></a>Win32 \_ rdmsdesktopzuweisung-Klasse

Beschreibt die Benutzer Desktop Zuweisung für die RD-Sammlung.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSDesktopAssignment
{
  string CollectionAlias;
  string DesktopName;
  string UserName;
  string UserDomain;
};
```

## <a name="members"></a>Member

Die **Win32 \_ rdmsdesktopzuweisung** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32-Klasse \_ rdmsdesktopzuweisung** verfügt über diese Methoden.



| Methode                                                                                 | BESCHREIBUNG                              |
|:---------------------------------------------------------------------------------------|:-----------------------------------------|
| [**Adddesktopzuweisung**](win32-rdmsdesktopassignment-adddesktopassignment.md)       | Fügt eine Desktop Zuweisung hinzu.<br/>    |
| [**Removedesktopzuweisung**](win32-rdmsdesktopassignment-removedesktopassignment.md) | Entfernt eine Desktop Zuweisung.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ rdmsdesktopzuweisung** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Collectionalias**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Alias der Auflistung.

</dd> <dt>

**Desktopname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Der Name des Desktops.

</dd> <dt>

**UserDomain**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Der Domänen Name des Benutzerkontos.

</dd> <dt>

**UserName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Der Name des Benutzerkontos.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                              |
| Namespace<br/>                | Root \\ CIMV2 \\ RDMs<br/>                                                                |
| MOF<br/>                      | <dl> <dt>Rdmanagement. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



 

