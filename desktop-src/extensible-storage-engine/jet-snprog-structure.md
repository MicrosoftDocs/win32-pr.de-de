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
ms.openlocfilehash: ab132d203ca2dc81e2ed3c3d8a0ce25c76a2cc71
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987733"
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


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 


