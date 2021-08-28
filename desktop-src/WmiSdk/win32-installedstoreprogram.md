---
title: Win32 \_ InstalledStoreProgram-Klasse
description: Die Win32 \_ InstalledStoreProgram-Klasse stellt eine installierte Windows Store-Anwendung dar.
ms.assetid: 154c19c7-f2e5-48bd-b05b-3022e45f2aa4
keywords:
- Win32_InstalledStoreProgram-Klasse Anwendungs- und Geräteinventuranbieter
- Win32_InstalledStoreProgram Der Anwendungs- und Geräteinventuranbieter wird beschrieben.
topic_type:
- apiref
api_name:
- Win32_InstalledStoreProgram
- Win32_InstalledStoreProgram.ProgramId
- Win32_InstalledStoreProgram.Name
- Win32_InstalledStoreProgram.Vendor
- Win32_InstalledStoreProgram.Version
- Win32_InstalledStoreProgram.Language
- Win32_InstalledStoreProgram.Architecture
api_location:
- Root\CIMv2
api_type:
- Schema
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 613baba9990da8403417aa4f8639ed7e9b5a7a5f
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122917909"
---
# <a name="win32_installedstoreprogram-class"></a>Win32 \_ InstalledStoreProgram-Klasse

Die **Win32 \_ InstalledStoreProgram-Klasse** stellt eine installierte Windows Store-Anwendung dar.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
class Win32_InstalledStoreProgram
{
  string ProgramId;
  string Name;
  string Vendor;
  string Version;
  string Language;
  string Architecture;
};
```

## <a name="members"></a>Member

Die **Win32 \_ InstalledStoreProgram-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ InstalledStoreProgram-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Architektur**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die unterstützten Prozessorarchitekturen für die Windows-Speicheranwendung.

</dd> <dt>

**Sprache**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die unterstützten Sprachen für die Windows Store-Anwendung.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name der Windows Speicheranwendung.

</dd> <dt>

**ProgramId**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Der eindeutige Bezeichner der Windows Speicheranwendung.

</dd> <dt>

**Hersteller**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Herausgeber der Windows Store-Anwendung.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Version der Windows Store-Anwendung.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



|                                     |                                                                                      |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                            |
| Namespace<br/>                | Root\\CIMv2<br/>                                                               |
| MOF<br/>                      | <dl> <dt>Aeinv.mof</dt> </dl> |



 

 





