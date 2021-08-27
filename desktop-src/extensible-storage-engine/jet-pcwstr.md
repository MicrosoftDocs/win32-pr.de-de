---
description: 'Weitere Informationen zu: JET_PCWSTR'
title: JET_PCWSTR
TOCTitle: JET_PCWSTR
ms:assetid: fef64bb9-c2e0-4cfb-8138-c98ae6f50952
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294145(v=EXCHG.10)
ms:contentKeyID: 32765759
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
ms.openlocfilehash: 1eda03d9c08e0e18f1a60e088405919f3982e9de
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476152"
---
# <a name="jet_pcwstr"></a>JET_PCWSTR


_**Gilt für:** Windows | Windows Server_

## <a name="jet_pcwstr"></a>JET_PCWSTR

Der **JET_PCWSTR** Datentyp enthält eine auf NULL endende, konstante **Unicode-Zeichenfolge** (char \* ).

**Windows Vista: JET_PCWSTR** wird in Windows Vista eingeführt.

```cpp
    typedef __nullterminated const WCHAR * JET_PCWSTR;
```

### <a name="data-types"></a>Datentypen

JET_PCWSTR

Null-terminierte, konstante Unicode-Zeichenfolge (char \* ).

### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 


