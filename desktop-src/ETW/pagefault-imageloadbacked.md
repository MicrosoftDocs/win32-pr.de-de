---
description: Diese Klasse ist die Ereignistypklasse für das Laden von Bildern in Seitendateiereignissen. Die folgende Syntax wird durch einen MOF-Code vereinfacht.
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
ms.openlocfilehash: 75104fcf923ed59bfcc99e214e66a235549b7059ca0e36c41b6f90d308a3efff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811770"
---
# <a name="pagefault_imageloadbacked-class"></a>PageFault \_ ImageLoadBacked-Klasse

Diese Klasse ist die Ereignistypklasse für das Laden von Bildern in Seitendateiereignissen.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

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

Die **PageFault \_ ImageLoadBacked-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **PageFault \_ ImageLoadBacked-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**DeviceChar**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(2), Format("x")
</dt> </dl>

Reserviert.

</dd> <dt>

**FileChar**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(3), Format("x")
</dt> </dl>

Reserviert.

</dd> <dt>

**FileObject**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(1), Zeiger
</dt> </dl>

Übereinstimmung mit dem Wert dieses Zeigers mit dem **FileObject-Zeigerwert** in einem [**FileIo \_ Name-Ereignis,**](fileio-name.md) um den Namen der Datei zu bestimmen.

</dd> <dt>

**LoadFlags**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(4), Format("x")
</dt> </dl>

Reserviert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das Ereignis wird während der Erstellung eines Imageabschnitts protokolliert (z. B. beim Laden einer DLL), wenn der Speicher-Manager feststellt, dass das Image kopiert und aus der Seitendatei ausgeführt werden muss. In der Regel werden Bilder aus der Quelldatei ausgeführt, aber die Seitendateisicherung kann auftreten, wenn der Speicher-Manager feststellt, dass die Quelldatei von vorhandenen Writern asynchron geändert werden kann oder wenn sich die Quelldatei auf einem Wechselmedium oder einem Remotegerät befindet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PageFault \_ V2**](pagefault-v2.md)
</dt> </dl>

 

 




