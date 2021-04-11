---
description: Ermöglicht die Festlegung von Grenzwerten für die Host Prozess Verwendung von Systemressourcen.
ms.assetid: 5f5ed1c6-bd1a-406d-a682-7a52059d9450
ms.tgt_platform: multiple
title: __ProviderHostQuotaConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ProviderHostQuotaConfiguration
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 443d66c8e508346444e98a92b341f1e7d67d8cd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216323"
---
# <a name="__providerhostquotaconfiguration-class"></a>\_\_Providerhostquotaconfiguration-Klasse

Die " **\_ \_ providerhostquotaconfiguration** "-System Klasse ist eine Konfigurations Klasse für Host Anbieter Prozesse. Diese Klasse befindet sich im Stamm Namespace und ermöglicht die Festlegung von Grenzwerten für die Host Prozess Verwendung von Systemressourcen.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
class __ProviderHostQuotaConfiguration : __SystemClass
{
  uint32 ThreadsPerHost;
  uint32 HandlesPerHost;
  uint32 ProcessLimitAllHosts;
  uint64 MemoryPerHost;
  uint64 MemoryAllHosts;
};
```

## <a name="members"></a>Member

Die **\_ \_ providerhostquotaconfiguration** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ providerhostquotaconfiguration** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Lenker Host**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die Anzahl der Kernel Objekt Handles, die jeder Host aufweisen kann.

</dd> <dt>

**Memoryallhosts**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Kombinierte Größe des privaten Speichers in Bytes, der von allen Hosts belegt werden kann.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**Memoryperhost**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die Menge des privaten Speichers, der von jedem Host belegt werden kann.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**Processlimitallhosts**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die Gesamtanzahl von Host Prozessen, die gleichzeitig ausgeführt werden können.

</dd> <dt>

**Threadsperhost**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Anzahl von Threads, die sich im Besitz eines Hosts befinden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Eigenschaften, die die Grenzwerte darstellen, können geändert werden, aber da es sich bei der Klasse um einen Singleton handelt, haben alle Anbieter Hosts dieselben Grenzen.

Die folgenden Parameter werden verwendet, wenn die Grenzwerte für das Auftrags Objekt für das Host Auftrags Objekt konfiguriert werden:

-   **Memoryallhosts**
-   **Memoryperhost**
-   **Processlimitallhosts**
-   **Threadsperhost**

Der Host Prozess fragt die Verwendung von Handles ab und beendet den Prozess, wenn das " **Lenker Host** "-Kontingent verletzt wird. Änderungen an diesen Werten treten nach dem Neustart des Computers in Kraft.

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
</dt> </dl>

 

