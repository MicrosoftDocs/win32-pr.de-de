---
description: Diese Klasse ist die Ereignistyp Klasse für das Laden von Bildern in Auslagerungs Datei Ereignissen. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 7d2f08e8-ec1f-4630-922a-548b55eadfda
title: PageFault_ImageLoadBacked-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_ImageLoadBacked
- PageFault_ImageLoadBacked.FileObject
- PageFault_ImageLoadBacked.DeviceChar
- PageFault_ImageLoadBacked.FileChar
- PageFault_ImageLoadBacked.LoadFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1644db74c5c7c361acda796219ae1415ecc262bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980088"
---
# <a name="pagefault_imageloadbacked-class"></a>Pagefault \_ imageloadbackup-Klasse

Diese Klasse ist die Ereignistyp Klasse für das Laden von Bildern in Auslagerungs Datei Ereignissen.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType{105}, EventTypeName{"ImageLoadBacked"}]
class PageFault_ImageLoadBacked : PageFault_V2
{
  uint32 FileObject;
  uint32 DeviceChar;
  uint16 FileChar;
  uint16 LoadFlags;
};
```

## <a name="members"></a>Member

Die **Pagefault \_ imageloadbackup** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Pagefault \_ imageloadbackup** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Devicechar**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (2), Format ("x")
</dt> </dl>

Reserviert.

</dd> <dt>

**Filechar**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (3), Format ("x")
</dt> </dl>

Reserviert.

</dd> <dt>

**File Object**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (1), Zeiger
</dt> </dl>

Vergleichen Sie den Wert dieses Zeigers mit dem **FileObject** -Zeiger Wert in einem [**FileIO- \_ namens**](fileio-name.md) Ereignis, um den Namen der Datei zu bestimmen.

</dd> <dt>

**Loadflags**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (4), Format ("x")
</dt> </dl>

Reserviert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das Ereignis wird während der Erstellung eines Bild Abschnitts (z. b. beim Laden einer DLL) protokolliert, wenn der Speicher-Manager feststellt, dass das Image in die Auslagerungs Datei kopiert und aus dieser ausgeführt werden muss. In der Regel werden Bilder aus der Quelldatei ausgeführt, aber eine Auslagerungs Datei kann auftreten, wenn der Speicher-Manager feststellt, dass die Quelldatei asynchron durch vorhandene Writer geändert werden kann oder wenn sich die Quelldatei auf einem Wechselmedium oder einem Remote Gerät befindet.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Pagefault \_ v2**](pagefault-v2.md)
</dt> </dl>

 

 




