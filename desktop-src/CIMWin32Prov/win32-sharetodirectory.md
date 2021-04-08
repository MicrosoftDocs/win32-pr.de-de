---
description: Die \_ WMI-Klasse "Win32 shareesdirectory Association" verknüpft eine freigegebene Ressource auf dem Computersystem und das Verzeichnis, dem Sie zugeordnet ist.
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
ms.openlocfilehash: f02e5e1ce125a2c8495327a08c14c94ac9f48567
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747824"
---
# <a name="win32_sharetodirectory-class"></a>Win32 \_ sharededirectory-Klasse

Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) " **Win32 \_ shareesdirectory** Association" verknüpft eine freigegebene Ressource auf dem Computersystem und das Verzeichnis, dem Sie zugeordnet ist.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.

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

Die **Win32 \_ sharetodirectory** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ sharededirectory** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Teilen**
</dt> <dd> <dl> <dt>

Datentyp: **Win32- \_ Freigabe**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI- \| Win32- \_ Freigabe")
</dt> </dl>

Verweis auf die-Instanz, die die Eigenschaften einer freigegebenen Ressource darstellt, die über das Verzeichnis verfügbar ist.

</dd> <dt>

**Sharedelta**
</dt> <dd> <dl> <dt>

Datentyp: **CIM- \_ Verzeichnis**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM- \_ Verzeichnis")
</dt> </dl>

Verweis auf die-Instanz, die die Eigenschaften des Verzeichnisses darstellt, das einer freigegebenen Ressource zugeordnet wurde.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Betriebssystemklassen](./operating-system-classes.md)
</dt> </dl>

 

 
