---
description: Enthält die Attributdaten für eine Datei.
ms.assetid: f23f801c-826c-4269-bf96-0e01430484f4
title: ATTRINFO-Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ATTRINFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 090f2ab58d8bf1eb4e379166086d31389b533712a3df23f987bba1331f990891
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103730"
---
# <a name="attrinfo-structure"></a>ATTRINFO-Struktur

Enthält die Attributdaten für eine Datei.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagATTRINFO {
  TAG   tAttrID;
  DWORD dwFlags;
  union {
    ULONGLONG ullAttr;
    DWORD     dwAttr;
    TCHAR     *lpAttr;
  };
} ATTRINFO, *PATTRINFO;
```



## <a name="members"></a>Member

<dl> <dt>

**tAttrID**
</dt> <dd>

Der Attributtyp. Weitere Informationen [finden Sie unter TAG-Typen.](tag-types.md)

</dd> <dt>

**dwFlags**
</dt> <dd>

Die Flags für dieses Attribut.



| Wert                                                                                                                                                                                                                                           | Bedeutung                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="ATTRIBUTE_AVAILABLE"></span><span id="attribute_available"></span><dl> <dt>**ATTRIBUTE \_ VERFÜGBARE**</dt> <dt>0X00000001</dt> </dl> | Das -Attribut ist verfügbar.<br/>                             |
| <span id="ATTRIBUTE_FAILED"></span><span id="attribute_failed"></span><dl> <dt>**ATTRIBUTE \_ FEHLER**</dt> <dt>0x00000002</dt> </dl>          | Fehler beim Aufruf, weil das Attribut nicht verfügbar ist.<br/> |



 

</dd> <dt>

**ullAttr**
</dt> <dd>

Ein **QWORD-Wert** (wenn der Tagtyp **TAG TYPE \_ \_ QWORD ist).**

</dd> <dt>

**dwAttr**
</dt> <dd>

Ein **DWORD-Wert** (wenn der Tagtyp **TAG TYPE \_ \_ DWORD ist).**

</dd> <dt>

**lpAttr**
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge (wenn der Tagtyp **TAG \_ TYPE \_ STRINGREF ist).**

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SdbFormatAttribute**](sdbformatattribute.md)
</dt> <dt>

[**SdbFreeFileAttributes**](sdbfreefileattributes.md)
</dt> <dt>

[**SdbGetFileAttributes**](sdbgetfileattributes.md)
</dt> </dl>

 

 




