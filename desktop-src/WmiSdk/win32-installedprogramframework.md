---
title: Win32 \_ InstalledProgramFramework-Klasse
description: Die Win32 InstalledProgramFramework-Klasse stellt ein Technologieframework dar, für das eine \_ Win32 InstalledWin32Program-Instanz zur Laufzeit kompiliert oder \_ verwendet wird.
ms.assetid: bb5c18c7-ec71-4579-8190-942de4fccd9e
keywords:
- Win32_InstalledProgramFramework-Klasse Anwendungs- und Geräteinventuranbieter
- Win32_InstalledProgramFramework Der Anwendungs- und Geräteinventuranbieter wird beschrieben.
topic_type:
- apiref
api_name:
- Win32_InstalledProgramFramework
- Win32_InstalledProgramFramework.FrameworkName
- Win32_InstalledProgramFramework.FrameworkPublisher
- Win32_InstalledProgramFramework.FrameworkVersion
- Win32_InstalledProgramFramework.FrameworkVersionActual
- Win32_InstalledProgramFramework.ProgramId
- Win32_InstalledProgramFramework.IsPrivate
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
ms.openlocfilehash: 3e447544dbfdebd6e4f4dd12752171089b8da041
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122917895"
---
# <a name="win32_installedprogramframework-class"></a>Win32 \_ InstalledProgramFramework-Klasse

Die **Win32 \_ InstalledProgramFramework-Klasse** stellt ein Technologieframework dar, für das eine [**Win32 \_ InstalledWin32Program-Instanz**](win32-installedwin32program.md) zur Laufzeit kompiliert oder verwendet wird. Frameworks, die diese Klasse derzeit melden kann, sind OpenSSL, Visual Basic, Visual C++ .NET, Visual C++, Java (erkennt nur die Binärdateien der Java-Runtime) und CLR.

> [!Note]  
> Der Satz von Frameworks, die von dieser Klasse erkannt werden können, kann im Laufe der Zeit aktualisiert werden.

 

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
class Win32_InstalledProgramFramework
{
  string  FrameworkName;
  string  FrameworkPublisher;
  string  FrameworkVersion;
  string  FrameworkVersionActual;
  string  ProgramId;
  boolean IsPrivate;
};
```

## <a name="members"></a>Member

Die **Win32 \_ InstalledProgramFramework-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ InstalledProgramFramework-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Frameworkname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Der Name des Frameworks, von dem die durch **ProgramId identifizierte** Anwendung abhängig ist.

</dd> <dt>

**FrameworkPublisher**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Der Herausgeber des Frameworks.

</dd> <dt>

**FrameworkVersion**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Die Version des Frameworks, von der die Anwendung abhängig ist.

</dd> <dt>

**FrameworkVersionActual**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Die Version des Frameworks, die die Anwendung tatsächlich zur Laufzeit verwendet, wenn das Framework erkannt werden kann.

</dd> <dt>

**Isprivate**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

TRUE, wenn die Anwendung eine private Kopie des Frameworks bündelt.

</dd> <dt>

**ProgramId**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Der eindeutige Bezeichner der [**Win32 \_ InstalledWin32Program-Instanz,**](win32-installedwin32program.md) der die Frameworkdaten zugeordnet sind.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



|                                     |                                                                                      |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                            |
| Namespace<br/>                | Root\\CIMv2<br/>                                                               |
| MOF<br/>                      | <dl> <dt>Aeinv.mof</dt> </dl> |



 

 





