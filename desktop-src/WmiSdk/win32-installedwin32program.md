---
title: Win32 \_ InstalledWin32Program-Klasse
description: Die Win32 \_ InstalledWin32Program-Klasse stellt eine installierte Win32-Anwendung dar.
ms.assetid: 2eef00da-8597-4852-b4fb-4276d05fd724
keywords:
- Win32_InstalledWin32Program-Klasse "Anwendungs- und Geräteinventuranbieter"
- Win32_InstalledWin32Program-Klasse Anwendungs- und Geräteinventuranbieter beschrieben
topic_type:
- apiref
api_name:
- Win32_InstalledWin32Program
- Win32_InstalledWin32Program.ProgramId
- Win32_InstalledWin32Program.Name
- Win32_InstalledWin32Program.Vendor
- Win32_InstalledWin32Program.Version
- Win32_InstalledWin32Program.Language
- Win32_InstalledWin32Program.MsiPackageCode
- Win32_InstalledWin32Program.MsiProductCode
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
ms.openlocfilehash: 51cfbf56591bca71f8364d97a9a4adb0d995c4c3
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122917903"
---
# <a name="win32_installedwin32program-class"></a>Win32 \_ InstalledWin32Program-Klasse

Die **Win32 \_ InstalledWin32Program-Klasse** stellt eine installierte Win32-Anwendung dar.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
class Win32_InstalledWin32Program
{
  string ProgramId;
  string Name;
  string Vendor;
  string Version;
  string Language;
  string MsiPackageCode;
  string MsiProductCode;
};
```

## <a name="members"></a>Member

Die **Win32 \_ InstalledWin32Program-Klasse** verfügt über folgende Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ InstalledWin32Program-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Sprache**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die unterstützten Sprachen für die installierte Win32-Anwendung.

</dd> <dt>

**MsiPackageCode**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der MSI-Paketcode, wenn die Win32-Anwendung mithilfe einer MSI installiert wurde.

</dd> <dt>

**MsiProductCode**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der MSI-Produktcode, wenn die Win32-Anwendung mithilfe einer MSI installiert wurde.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name der installierten Win32-Anwendung.

</dd> <dt>

**ProgramId**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Der eindeutige Bezeichner der installierten Win32-Anwendung. Dieser Wert hilft, **Win32 \_ InstalledWin32Program** mit [**Win32 \_ InstalledProgramFramework**](win32-installedprogramframework.md)zu korrelieren.

</dd> <dt>

**Hersteller**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Herausgeber der installierten Win32-Anwendung.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Version der installierten Win32-Anwendung.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



|                                     |                                                                                      |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                            |
| Namespace<br/>                | Root\\CIMv2<br/>                                                               |
| MOF<br/>                      | <dl> <dt>Aeinv.mof</dt> </dl> |



 

 





