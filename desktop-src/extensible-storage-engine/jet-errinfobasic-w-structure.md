---
description: 'Weitere Informationen zu: JET_ERRINFOBASIC_W-Struktur'
title: JET_ERRINFOBASIC_W-Struktur
TOCTitle: JET_ERRINFOBASIC_W Structure
ms:assetid: fcc55cb7-718d-419a-a473-15e030c23abd
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475861(v=EXCHG.10)
ms:contentKeyID: 37033567
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: c02d9f8081040293bd154137163e13cc9d313a32
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984033"
---
# <a name="jet_errinfobasic_w-structure"></a>JET_ERRINFOBASIC_W-Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_errinfobasic_w-structure"></a>JET_ERRINFOBASIC_W-Struktur

Die **JET_ERRINFOBASIC_W-Struktur** definiert die Daten, die von der [JetGetErrorInfo()-Methode](./jetgeterrorinfow-function.md) zurückgegeben werden, wenn die JET_ErrorInfoSpecificErr InfoLevel übergeben wird.

Hinweis: Diese Dokumentation basiert auf einer vorläufigen Version der Extensible Storage Engine. Diese Informationen können geändert werden.

```cpp
typedef struct { 
    unsigned long cbStruct; 
    JET_ERR errValue; 
    JET_ERRCAT errcatMostSpecific; 
    unsigned char rgCategoricalHierarchy[8]; 
    unsigned long lSourceLine; 
    WCHAR rgszSourceFile[64]; 
} JET_ERRINFOBASIC_W;
```

### <a name="members"></a>Member

**cbStruct**

Die Größe der -Struktur in Bytes. Sie muss auf sizeof( JET_ERRINFOBASIC ) festgelegt werden.

**errValue**

Der Fehlerwert, der ausgewertet wurde, wie für das *pvResult-Argument* an [JetGetErrorInfo()](./jetgeterrorinfow-function.md)übergeben.

**errcatMostSpecific**

Die niedrigste Ebene [JET_ERRCAT](./jet-errcat.md) Konstante, die dem Fehler zugeordnet ist. Das heißt, die Kategorie auf Blattebene in der Kategoriehierarchie, die in [JET_ERRCAT](./jet-errcat.md)dokumentiert ist.

**rgCategoricalHierarchy \[ 8\]**

Die Hierarchie der Fehlerkategorien, die dem Fehler zugeordnet ist. Position 0 ist die höchste Ebene in der Hierarchie von [JET_ERRCAT,](./jet-errcat.md)und die übrigen sind Unterkategorien, bis die spezifischste Kategorie festgelegt ist, nach der alle Kategorien JET_errcatUnknown werden.

**lSourceLine**

Reserviert.

**rgszSourceFile \[ 64\]**

Reserviert.

### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows 8.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows 8 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 

