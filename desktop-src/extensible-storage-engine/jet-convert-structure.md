---
description: 'Weitere Informationen zu: JET_CONVERT-Struktur'
title: JET_CONVERT-Struktur
TOCTitle: JET_CONVERT Structure
ms:assetid: 33a0ff95-e9af-44c0-bf80-03d785771d5e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269220(v=EXCHG.10)
ms:contentKeyID: 32765523
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
ms.openlocfilehash: 9ca27bcc8024d8d3f0f634f6f8e6b23082b8d075
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480506"
---
# <a name="jet_convert-structure"></a>JET_CONVERT-Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_convert-structure"></a>JET_CONVERT-Struktur

Die **JET_CONVERT-Struktur** enthält den Namen einer früheren ESE-Versions-DLL, die zum Lesen von Datenbanken verwendet wird, die mit dieser früheren Version erstellt wurden. Darüber hinaus werden andere Flags bereitgestellt, um die Art der Konvertierung zu steuern.

**Windows Server 2003:** Das Feature in [JetCompact,](./jetcompact-function.md) das eine Konvertierung durchgeführt hat, wurde in Windows Server 2003 aus dem Produkt entfernt. Sie wird nur in Windows 2000 und Windows XP unterstützt.

```cpp
    typedef struct tagCONVERT {
      tchar* SzOldDll;
      union {
        unsigned long fFlags;
        struct {
          unsigned long fSchemaChangesOnly  :1;
        };
      };
    } JET_CONVERT;
```

### <a name="members"></a>Member

**SzOldDll**

Der Name, einschließlich Pfadinformationen, zur früheren Version der ESE-DLL.

**fFlags**

Ist für das System reserviert.

**fSchemaChangesOnly**

Ist für das System reserviert.

### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Unicode</strong></p> | <p>Implementiert als <strong>JET_CONVERT_W</strong> (Unicode) und <strong>JET_CONVERT_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Weitere Informationen

[JetCompact](./jetcompact-function.md)
