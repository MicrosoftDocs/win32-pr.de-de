---
description: Enthält die Attributdaten für eine Datei.
ms.assetid: f23f801c-826c-4269-bf96-0e01430484f4
title: Attrinfo-Struktur
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
ms.openlocfilehash: 01c061330db3e97989e0700452fd4a205488a9fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860614"
---
# <a name="attrinfo-structure"></a>Attrinfo-Struktur

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

**tattrierer**
</dt> <dd>

Der Attributtyp. Siehe [Tagtypen](tag-types.md).

</dd> <dt>

**dwFlags**
</dt> <dd>

Die Flags für dieses Attribut.



| Wert                                                                                                                                                                                                                                           | Bedeutung                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="ATTRIBUTE_AVAILABLE"></span><span id="attribute_available"></span><dl> <dt>**Attribut \_ Verfügbare**</dt> <dt>0x00000001</dt> </dl> | Das-Attribut ist verfügbar.<br/>                             |
| <span id="ATTRIBUTE_FAILED"></span><span id="attribute_failed"></span><dl> <dt>**Attribut \_**</dt>Fehler bei <dt>0x00000002</dt> . </dl>          | Der-Rückruf ist fehlgeschlagen, da das-Attribut nicht verfügbar ist.<br/> |



 

</dd> <dt>

**ullattr**
</dt> <dd>

Ein **QWORD** -Wert (wenn der Tagtyp **\_ \_ QWORD** ist).

</dd> <dt>

**dwattr**
</dt> <dd>

Ein **DWORD** -Wert (wenn der Tagtyp **\_ \_ DWORD** ist).

</dd> <dt>

**lpattr**
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge (wenn der Tagtyp **" \_ TagType \_**" ist).

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sdbformatattribute**](sdbformatattribute.md)
</dt> <dt>

[**Sdbfrefileattribute**](sdbfreefileattributes.md)
</dt> <dt>

[**Sdbgetfileattribute**](sdbgetfileattributes.md)
</dt> </dl>

 

 




