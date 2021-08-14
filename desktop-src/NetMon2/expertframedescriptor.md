---
description: Die EXPERTFRAMEDESCRIPTOR-Struktur enthält Informationen zu einem Frame. Wenn der Experte die ExpertGetFrame-Funktion erfolgreich aufruft, übergibt Netzwerkmonitor die EXPERTFRAMEDESCRIPTOR-Struktur an den Experten zurück.
ms.assetid: 6cf99498-3cf9-46da-b6a0-3012229f6908
title: EXPERTFRAMEDESCRIPTOR-Struktur (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTFRAMEDESCRIPTOR
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4a11c131188cdd5230d309a6ff2e39a77ac7886333dafd9860d565fdcb10efc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939027"
---
# <a name="expertframedescriptor-structure"></a>EXPERTFRAMEDESCRIPTOR-Struktur

Die **EXPERTFRAMEDESCRIPTOR-Struktur** enthält Informationen zu einem Frame. Wenn der Experte die [**ExpertGetFrame-Funktion**](expertgetframe.md) erfolgreich aufruft, übergibt Netzwerkmonitor die **EXPERTFRAMEDESCRIPTOR-Struktur** an den Experten zurück.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD                FrameNumber;
  HFRAME               hFrame;
  ULPFRAME             pFrame;
  LPRECOGNIZEDATATABLE lpRecognizeDataTable;
  LPPROPERTYTABLE      lpPropertyTable;
} EXPERTFRAMEDESCRIPTOR, *LPEXPERTFRAMEDESCRIPTOR;
```



## <a name="members"></a>Member

<dl> <dt>

**FrameNumber**
</dt> <dd>

Nummer eines angegebenen Frames.

</dd> <dt>

**hFrame**
</dt> <dd>

Handle für einen Frame.

</dd> <dt>

**pFrame**
</dt> <dd>

Zeiger auf einen rohen Frame.

</dd> <dt>

**lpRecognizeDataTable**
</dt> <dd>

Tabelle, die angibt, wo jeder Parser den Anfang der Daten identifiziert.

</dd> <dt>

**lpPropertyTable**
</dt> <dd>

Tabelle der Frameeigenschaften, die der Parser identifiziert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn der Experte beim Aufrufen von ExpertGetFrame FLAGS \_ ATTACH PROPERTIES angibt, ist der \_ **szPropertyText-Member** in jeder [**PROPERTYINST-Struktur**](propertyinst.md) **NULL.** [](expertgetframe.md)

Wenn der Experte beim \_ Aufrufen der ExpertGetFrame-Funktion keine FLAGS ATTACH PROPERTIES angibt, \_ ist der **lpPropertyTable-Member** bei der Rückgabe **NULL.** [](expertgetframe.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




