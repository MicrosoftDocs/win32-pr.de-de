---
description: 'Weitere Informationen finden Sie hier: JET_RSTINFO Struktur'
title: JET_RSTINFO Struktur
TOCTitle: JET_RSTINFO Structure
ms:assetid: 2f144d68-dcd9-4d0d-9d9e-a7d2a5c350fe
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269216(v=EXCHG.10)
ms:contentKeyID: 32765519
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3a776c84d89dfc97272c65bb0c0684faba814fdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128665"
---
# <a name="jet_rstinfo-structure"></a>JET_RSTINFO Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_rstinfo-structure"></a>JET_RSTINFO Struktur

Die **JET_RSTINFO** Struktur enthält Steuerungsinformationen für den Wiederherstellungsprozess, z. b. Informationen zur Daten Bank Verlagerung und Möglichkeit, die Wiederherstellung zu steuern

**Windows Vista:** Die **JET_RSTINFO** Struktur wird in Windows Vista eingeführt.

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_RSTMAP* rgrstmap;
      long crstmap;
      JET_LGPOS lgposStop;
      JET_LOGTIME logtimeStop;
      JET_PFNSTATUS pfnStatus;
    } JET_RSTINFO;
```

### <a name="members"></a>Member

**cbStruct**

Die Größe der-Struktur.

**rgrstmap**

Die-Struktur, die den alten und den neuen Pfad einer wiederhergestellten Datenbank beschreibt.

**crstmap**

Anzahl der Array Einträge in der rgrstmap.

**lgposstopps**

Die Protokoll Position, an der die Wiederherstellung beendet wird. Es wird keine rückgängig gemacht.

**logtimestoppt**

Für die zukünftige Verwendung reserviert.

**pfnstatus**

Eine Status Funktion zum Melden des Status der Wiederherstellung.

### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>In "ESENT. h" deklariert.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Wird als <strong>JET_RSTINFO_W</strong> (Unicode) und <strong>JET_RSTINFO_A</strong> (ANSI) implementiert.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[JetInit3](./jetinit3-function.md)
