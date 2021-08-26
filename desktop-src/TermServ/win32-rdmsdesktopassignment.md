---
title: Win32_RDMSDesktopAssignment-Klasse
description: Beschreibt die Zuweisung des Rd-Sammlungsbenutzerdesktops.
ms.assetid: d3370cf2-65db-4e01-9ea3-9a71340bf71b
ms.tgt_platform: multiple
keywords:
- Win32_RDMSDesktopAssignment-Remotedesktopdienste
- Win32_RDMSDesktopAssignment klasse Remotedesktopdienste , beschrieben
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
ms.openlocfilehash: 88576607777fe55d2fb2d4d9232ddc9d4b23849503e56f53fe4cd99f3931ddea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868210"
---
# <a name="win32_rdmsdesktopassignment-class"></a>Win32 \_ RDMSDesktopAssignment-Klasse

Beschreibt die Zuweisung des Rd-Sammlungsbenutzerdesktops.

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

Die **Win32 \_ RDMSDesktopAssignment-Klasse** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ RDMSDesktopAssignment-Klasse** verfügt über diese Methoden.



| Methode                                                                                 | BESCHREIBUNG                              |
|:---------------------------------------------------------------------------------------|:-----------------------------------------|
| [**AddDesktopAssignment**](win32-rdmsdesktopassignment-adddesktopassignment.md)       | Fügt eine Desktopzuweisung hinzu.<br/>    |
| [**RemoveDesktopAssignment**](win32-rdmsdesktopassignment-removedesktopassignment.md) | Entfernt eine Desktopzuweisung.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ RDMSDesktopAssignment-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**CollectionAlias**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Alias der Auflistung.

</dd> <dt>

**DesktopName**
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

Der Domänenname des Benutzerkontos.

</dd> <dt>

**UserName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Der Benutzername.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                              |
| Namespace<br/>                | Root \\ cimv2 \\ rdms<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



 

