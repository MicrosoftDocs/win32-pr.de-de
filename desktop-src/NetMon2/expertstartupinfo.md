---
description: Enthält Daten, die einen Experten beschreiben, wenn er gestartet wird.
ms.assetid: 9ecd5395-d10c-411b-a6bd-fbac724d8603
title: Expertstartupinfo-Struktur (Netmon. h)
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
ms.openlocfilehash: 627d47cec09a683f80c16374561899ab008d0596
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958727"
---
# <a name="expertstartupinfo-structure"></a>Expertstartupinfo-Struktur

Die Struktur " **expertstartupinfo** " enthält Daten, die einen Experten beschreiben, wenn er gestartet wird.

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

**hcapture**
</dt> <dd>

Handle für eine Erfassung.

</dd> <dt>

**szcapturefile**
</dt> <dd>

Der Name der Erfassungs Datei.

</dd> <dt>

**dwframennummer**
</dt> <dd>

Frame Nummer.

</dd> <dt>

**hprotocol**
</dt> <dd>

Handle für das Protokoll.

</dd> <dt>

**lppropertyinst**
</dt> <dd>

Zeiger auf eine [**propertyinst**](propertyinst.md) -Struktur.

</dd> <dt>

**sbitfield**
</dt> <dd> <dl> <dt>

**Bitzahl**
</dt> <dd>

Wird nur verwendet, wenn der **dataqualifizierermember** der [**propertyinst**](propertyinst.md) -Struktur auf Prop Qual Flags festgelegt ist \_ \_ .

</dd> <dt>

**Böller**
</dt> <dd>

Wird nur verwendet, wenn der **dataqualifizierermember** der [**propertyinst**](propertyinst.md) -Struktur auf Prop Qual Flags festgelegt ist \_ \_ .

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




