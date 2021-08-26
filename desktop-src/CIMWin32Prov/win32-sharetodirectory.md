---
description: Die WMI-Klasse für die Win32 ShareToDirectory-Zuordnung bezieht sich auf eine freigegebene Ressource auf dem Computersystem und auf das Verzeichnis, dem \_ sie zugeordnet ist.
ms.assetid: f8562539-2cb4-4661-8ef9-8b665e76a292
ms.tgt_platform: multiple
title: Win32_ShareToDirectory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShareToDirectory
- Win32_ShareToDirectory.Share
- Win32_ShareToDirectory.SharedElement
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d041209dcdbd1d9a39d08acb75180ec9cf292f01934c21762418571d44a32460
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119917540"
---
# <a name="win32_sharetodirectory-class"></a>Win32 \_ ShareToDirectory-Klasse

Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) für die **Win32 \_ ShareToDirectory-Zuordnung** bezieht sich auf eine freigegebene Ressource auf dem Computersystem und auf das Verzeichnis, dem sie zugeordnet ist.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{8502C511-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ShareToDirectory
{
  Win32_Share   REF Share;
  CIM_Directory REF SharedElement;
};
```

## <a name="members"></a>Member

Die **Win32 \_ ShareToDirectory-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ ShareToDirectory-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Teilen**
</dt> <dd> <dl> <dt>

Datentyp: **\_ Win32-Freigabe**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**schlüssel**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Share")
</dt> </dl>

Verweis auf die -Instanz, die die Eigenschaften einer freigegebenen Ressource darstellt, die über das Verzeichnis verfügbar ist.

</dd> <dt>

**SharedElement**
</dt> <dd> <dl> <dt>

Datentyp: **\_ CIM-Verzeichnis**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| \_ CIM-Verzeichnis")
</dt> </dl>

Verweis auf die -Instanz, die die Eigenschaften des Verzeichnisses darstellt, das einer freigegebenen Ressource zugeordnet wurde.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Betriebssystemklassen](./operating-system-classes.md)
</dt> </dl>

 

 
