---
description: Die Struktur von "expertframedescriptor" enthält Informationen zu einem Frame. Wenn der Experte die Funktion "expertgetframe" erfolgreich aufruft, übergibt Netzwerkmonitor die "expertframedescriptor"-Struktur an den Experten zurück.
ms.assetid: 6cf99498-3cf9-46da-b6a0-3012229f6908
title: Struktur von "expertframedescriptor" (Netmon. h)
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
ms.openlocfilehash: 98bafae39819b16b479df22fe6560888ef15d8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484339"
---
# <a name="expertframedescriptor-structure"></a>Struktur von "expertframedescriptor"

Die Struktur von " **expertframedescriptor** " enthält Informationen zu einem Frame. Wenn der Experte die Funktion " [**expertgetframe**](expertgetframe.md) " erfolgreich aufruft, übergibt Netzwerkmonitor die " **expertframedescriptor** "-Struktur an den Experten zurück.

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

**Framezahl**
</dt> <dd>

Die Nummer eines angegebenen Frames.

</dd> <dt>

**hframe**
</dt> <dd>

Handle für einen Frame.

</dd> <dt>

**pFrame**
</dt> <dd>

Zeiger auf einen rohframe.

</dd> <dt>

**lprecognizedatabel**
</dt> <dd>

Tabelle, die angibt, wo jeder Parser den Anfang der Daten identifiziert.

</dd> <dt>

**lppropertytable**
</dt> <dd>

Tabelle mit Frame Eigenschaften, die vom Parser identifiziert werden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn der Experte \_ beim Aufrufen von " \_ [**expertgetframe**](expertgetframe.md)" Flags anfügen-Eigenschaften angibt, ist das **szpropertytext** -Element in jeder [**propertyinst**](propertyinst.md) -Struktur **null**.

Wenn der Experte \_ beim Aufrufen der Funktion "-Funktion" keine Flags anfügen- \_ Eigenschaften angibt, ist das **lppropertytable** -Element bei Rückgabe **null** . [](expertgetframe.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




