---
description: Die übergeordnete Klasse, von der alle System Ereignis-Ablauf Verfolgungs Klassen abgeleitet werden. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 27979d9c-eca7-426f-8f8e-99443e5a0188
title: MSNT_SystemTrace-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSNT_SystemTrace
- MSNT_SystemTrace.Flags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2eb0044029761a93a353a08a955d39d76c267f9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977817"
---
# <a name="msnt_systemtrace-class"></a>MSNT \_ systemtrace-Klasse

Die übergeordnete Klasse, von der alle System Ereignis-Ablauf Verfolgungs Klassen abgeleitet werden.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[Guid("{9e814aad-3204-11d2-9a82-006008a86939}")]
class MSNT_SystemTrace : EventTrace
{
  uint32 Flags;
};
```

## <a name="members"></a>Member

Die **MSNT \_ systemtrace** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSNT \_ systemtrace** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Flags**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **definevalues {"ereignisablaufverfolgungsflag \_ \_ \_ verarbeiten", "ereignisablaufverfolgungsflag-Thread", "ereignisablaufverfolgungsflag zum Laden von Ereignissen", "Ereignis Ablauf Verfolgungs Kennzeichen- \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ Prozess \_ Zähler" Ereignis Ablaufverfolgungsflag für Datenträger-e/a \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ "," Ereignis Ablauf \_ Verfolgung Flag Datenträger Datei-e/a " \_ \_ \_ \_ ," Ereignis Ablaufverfolgungsflag für Datenträger-e/a-Vorgänge \_ \_ \_ \_ \_ "," \_ \_ \_ ereignisablaufverfolgungsflag-Verteiler "," Ereignis Ablauf Verfolgung \_ Flag Arbeits \_ \_ Speicher \_ Seiten \_ Fehler "ereignisablaufverfolgungsflag- \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ Registrierung", "ereignisablaufverfolgungsflag \_ \_ \_ ALPC", "Ereignis Ablaufverfolgungsflag \_ \_ \_ Split IO", "ereignisablaufverfolgungsflag-Treiber", "ereignisablaufverfolgungsflag- \_ \_ \_ \_ \_ \_ \_ Profil", "ereignisablaufverfolgungsflag für \_ \_ \_ Datei \_ \_ \_ \_ \_ \_** **map {" 0x00000001 "," 0x00000002 "," 0x00000004 "," 0x00000008 "," 0x00000010 "," 0x00000020 "," 0x00000040 "," 0x00000080 "," 0x00000100 " , "0x00000200", "0x00000400", "0x00000800", "0x00001000", "0x00002000", "0x00004000", "0x00010000 bis", "0x00020000", "0x00100000", "0x00200000", "0x00800000", "0x01000000", "0x02000000", "0x04000000"}**
</dt> </dl>

Aktivieren Sie das Flag, das die aktivierten Kernel Anbieter angibt.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



 

 




