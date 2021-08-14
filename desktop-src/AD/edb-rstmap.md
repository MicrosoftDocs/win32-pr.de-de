---
title: EDB_RSTMAP-Struktur (Ntdsbcli.h)
description: Wird mit der DsRestoreRegister-Funktion zum Zuordnen einer gesicherten Datenbank zu einer neuen Datenbank verwendet.
ms.assetid: b2c5d30a-3617-4807-82e8-57f7179b817c
ms.tgt_platform: multiple
keywords:
- EDB_RSTMAP-Struktur von Active Directory
- PEDB_RSTMAP Strukturzeiger Active Directory
topic_type:
- apiref
api_name:
- EDB_RSTMAP
- EDB_RSTMAPA
- EDB_RSTMAPW
api_location:
- Ntdsbcli.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c81fe35d8d41818d279df094a57c041b8ea52212d2ce2f0cdc379628f5d5971
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191691"
---
# <a name="edb_rstmap-structure"></a>\_EDB-RSTMAP-Struktur

Die **\_ EDB-RSTMAP-Struktur** wird mit der [**DsRestoreRegister-Funktion**](dsrestoreregister.md) verwendet, um eine sicherte Datenbank einer neuen Datenbank zuzuordnen.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  LPTSTR szDatabaseName;
  LPTSTR szNewDatabaseName;
} EDB_RSTMAP, *PEDB_RSTMAP;
```



## <a name="members"></a>Member

<dl> <dt>

**szDatabaseName**
</dt> <dd>

Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen der Datenbank enthält, als sie gesichert wurde.

</dd> <dt>

**szNewDatabaseName**
</dt> <dd>

Zeiger auf eine auf NULL endende Zeichenfolge, die ggf. den neuen Namen der Datenbank einschließlich des neuen Speicherorts enthält.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                        |
| Header<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **EDB \_ RSTMAPW** (Unicode) und **EDB \_ RSTMIMA** (ANSI)<br/>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DsRestoreRegister**](dsrestoreregister.md)
</dt> <dt>

[Verzeichnissicherungsstrukturen](directory-backup-structures.md)
</dt> </dl>

 

 





