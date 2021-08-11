---
description: 'Weitere Informationen zu: JET_SNPROG-Struktur'
title: JET_SNPROG-Struktur
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
ms.openlocfilehash: 251f7948ec4d15e455720043b847abbd855e24146dd05a432b2bf3ea6d28dfef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118252767"
---
# <a name="jet_snprog-structure"></a>JET_SNPROG-Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_snprog-structure"></a>JET_SNPROG-Struktur

Die **JET_SNPROG-Struktur** enthält Informationen zum Status eines Vorgangs mit langer Ausführungslaufzeit. Wenn die Rückruffunktion aufgerufen wird, um den Status des Vorgangs zu benachrichtigen, und der Vorgang noch ausgeführt wird, ist der letzte Parameter der Rückruffunktion ein Zeiger auf eine **JET_SNPROG** Struktur.

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cunitDone;
      unsigned long cunitTotal;
    } JET_SNPROG;
```

### <a name="members"></a>Member

**cbStruct**

Die Größe der **JET_SNPROG-Struktur** in Bytes. Dieser Wert bestätigt das Vorhandensein der folgenden Felder.

**cunitDone**

Die Anzahl der Arbeitseinheiten, die bereits während der Funktion mit langer Ausführung abgeschlossen wurden.

**cunitTotal**

Die Anzahl der Arbeitseinheiten, die abgeschlossen werden müssen. Dieser Wert sollte immer größer oder gleich **cunitDone** sein.

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
<td><p>Deklariert in Esent.h.</p></td>
</tr>
</tbody>
</table>

