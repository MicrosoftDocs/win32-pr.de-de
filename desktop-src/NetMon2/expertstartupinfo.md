---
description: Enthält Daten, die einen Experten beim Start beschreiben.
ms.assetid: 9ecd5395-d10c-411b-a6bd-fbac724d8603
title: EXPERTSTARTUPINFO-Struktur (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTSTARTUPINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: f49fcf3c87795dbd7c9e65745e1b5560331c96c471d8ff7b2c8a24560b143cb1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911050"
---
# <a name="expertstartupinfo-structure"></a>EXPERTSTARTUPINFO-Struktur

Die **EXPERTSTARTUPINFO-Struktur** enthält Daten, die einen Experten beim Start beschreiben.

## <a name="syntax"></a>Syntax


```C++
typedef struct _EXPERTSTARTUPINFO {
  DWORD          Flags;
  HCAPTURE       hCapture;
  char           szCaptureFile[MAX_PATH];
  DWORD          dwFrameNumber;
  HPROTOCOL      hProtocol;
  LPPROPERTYINST lpPropertyInst;
  struct {
    BYTE BitNumber;
    BOOL bOn;
  } sBitfield;
} EXPERTSTARTUPINFO, *PEXPERTSTARTUPINFO;
```



## <a name="members"></a>Member

<dl> <dt>

**Flags**
</dt> <dd>

Flags, die den Experten beschreiben.

</dd> <dt>

**hCapture**
</dt> <dd>

Handle für eine Erfassung.

</dd> <dt>

**szCaptureFile**
</dt> <dd>

Name der Erfassungsdatei.

</dd> <dt>

**dwFrameNumber**
</dt> <dd>

Framenummer.

</dd> <dt>

**hProtocol**
</dt> <dd>

Handle für das Protokoll.

</dd> <dt>

**lpPropertyInst**
</dt> <dd>

Zeiger auf eine [**PROPERTYINST-Struktur.**](propertyinst.md)

</dd> <dt>

**sBitfield**
</dt> <dd> <dl> <dt>

**BitNumber**
</dt> <dd>

Wird nur verwendet, wenn **der DataQualifier-Member** der [**PROPERTYINST-Struktur**](propertyinst.md) auf PROP \_ QUAL \_ FLAGS festgelegt ist.

</dd> <dt>

**Bon**
</dt> <dd>

Wird nur verwendet, wenn **der DataQualifier-Member** der [**PROPERTYINST-Struktur**](propertyinst.md) auf PROP \_ QUAL \_ FLAGS festgelegt ist.

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




