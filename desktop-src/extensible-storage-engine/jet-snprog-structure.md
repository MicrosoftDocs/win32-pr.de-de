---
description: 'Weitere Informationen finden Sie hier: JET_SNPROG Struktur'
title: JET_SNPROG Struktur
TOCTitle: JET_SNPROG Structure
ms:assetid: 8b4224e4-ad4d-440f-8915-8eb43b0885f0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269328(v=EXCHG.10)
ms:contentKeyID: 32765618
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 961e9cf264652924cfb1d870fa1a04aabc7fb61a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484267"
---
# <a name="jet_snprog-structure"></a>JET_SNPROG Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_snprog-structure"></a>JET_SNPROG Struktur

Die **JET_SNPROG** -Struktur enthält Informationen zum Fortschritt eines Vorgangs mit langer Ausführungszeit. Wenn die Rückruffunktion aufgerufen wird, um den Status des Vorgangs zu benachrichtigen, und der Vorgang noch ausgeführt wird, ist der letzte Parameter der Rückruffunktion ein Zeiger auf eine **JET_SNPROG** Struktur.

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cunitDone;
      unsigned long cunitTotal;
    } JET_SNPROG;
```

### <a name="members"></a>Member

**cbStruct**

Die Größe der **JET_SNPROG** Struktur in Bytes. Dieser Wert bestätigt, dass die folgenden Felder vorhanden sind.

**cunitdone**

Die Anzahl der Arbeitseinheiten, die während der Funktion mit langer Laufzeit bereits abgeschlossen sind.

**cunittotal**

Die Anzahl der Arbeitseinheiten, die abgeschlossen werden müssen. Dieser Wert sollte immer größer oder gleich **cunitdone** sein.

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
</tbody>
</table>

