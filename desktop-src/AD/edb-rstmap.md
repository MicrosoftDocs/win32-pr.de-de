---
title: EDB_RSTMAP Struktur (ntdsbcli. h)
description: Wird mit der dsrestoreregiester-Funktion verwendet, um eine gesicherte Datenbank einer neuen Datenbank zuzuordnen.
ms.assetid: b2c5d30a-3617-4807-82e8-57f7179b817c
ms.tgt_platform: multiple
keywords:
- EDB_RSTMAP Struktur Active Directory
- PEDB_RSTMAP Struktur Zeiger Active Directory
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
ms.openlocfilehash: be2c960ab7ebc687508131deac6cd8e7b99bbe81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040725"
---
# <a name="edb_rstmap-structure"></a>EDB- \_ rstmap-Struktur

Die **EDB- \_ rstmap** -Struktur wird mit der [**dsrestoreregiester**](dsrestoreregister.md) -Funktion verwendet, um eine gesicherte Datenbank einer neuen Datenbank zuzuordnen.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  LPTSTR szDatabaseName;
  LPTSTR szNewDatabaseName;
} EDB_RSTMAP, *PEDB_RSTMAP;
```



## <a name="members"></a>Member

<dl> <dt>

**szdatabasename**
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen der Datenbank enthält, als Sie gesichert wurde.

</dd> <dt>

**sznewdatabasename**
</dt> <dd>

Zeiger auf eine auf NULL endende Zeichenfolge, die den neuen Namen der Datenbank enthält, einschließlich des neuen Speicher Orts, falls zutreffend.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                        |
| Header<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **EDB \_ Rstmapw** (Unicode) und **EDB \_ rstmapa** (ANSI)<br/>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Dsrestoreregiester**](dsrestoreregister.md)
</dt> <dt>

[Struktur der Verzeichnis Sicherung](directory-backup-structures.md)
</dt> </dl>

 

 





