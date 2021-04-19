---
description: Fungiert als übergeordnete Klasse für die \_ \_ Win32Provider-System Klasse.
ms.assetid: e4cad7c6-4650-4334-b8c4-ac65381bced7
ms.tgt_platform: multiple
title: __Provider-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Provider
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 733323c106a5d682e7eddbe3a41bf9c156520c51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363520"
---
# <a name="__provider-class"></a>\_\_Anbieter Klasse

Die **\_ \_ Anbieter** System Klasse ist eine abstrakte Basisklasse, die als übergeordnete Klasse für die [**\_ \_ Win32Provider**](--win32provider.md) -System Klasse fungiert.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[abstract]
class __Provider : __SystemClass
{
  string Name;
};
```

## <a name="members"></a>Member

Die **\_ \_ Anbieter** Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ Anbieter** Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [ **Schlüssel**](standard-qualifiers.md)
</dt> </dl>

Sprachneutrale Zeichenfolge, die den Anbieter eindeutig identifiziert. Das folgende Format wird vorgeschlagen, um Namenskonflikte zu vermeiden:

Anbieter \| Version des Anbieters \|

Der Name des Anbieters steht beispielsweise für Version 1,0 von Microsoft testprovider:

"Microsoft \| Test Provider \| v 1.0"

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **\_ \_ Anbieter** Klasse wird von [**\_ \_ systemclass**](--systemclass.md)abgeleitet, die keine Eigenschaften hat.

Anbieter erstellen [**\_ \_ Win32Provider**](--win32provider.md) -Instanzen, um Informationen über ihre physische Implementierung anzugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_System Class**](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[WMI-System Klassen](wmi-system-classes.md)
</dt> <dt>

[**\_\_Win32Provider**](--win32provider.md)
</dt> </dl>

 

