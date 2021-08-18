---
description: Wird gesendet, um CPlApplet zu benachrichtigen, dass der Benutzer das symbol ausgewählt hat, das einem bestimmten Dialogfeld zugeordnet ist. CPlApplet sollte das entsprechende Dialogfeld anzeigen und alle vom Benutzer angegebenen Aufgaben ausführen.
title: CPL_STARTWPARMS (Cpl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 04ac5117-39c9-4d3f-b32d-8f8d2b515be1
api_name:
- CPL_STARTWPARMS
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f836f868b81daa49e87eb4efc804442bed25690ce126852891327d0eb042aaec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118460609"
---
# <a name="cpl_startwparms-message"></a>CPL \_ STARTWPARMS-Nachricht

Wird gesendet, um [**CPlApplet zu benachrichtigen,**](/windows/win32/api/cpl/nc-cpl-applet_proc) dass der Benutzer das symbol ausgewählt hat, das einem bestimmten Dialogfeld zugeordnet ist. **CPlApplet sollte** das entsprechende Dialogfeld anzeigen und alle vom Benutzer angegebenen Aufgaben ausführen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*uAppNum* 
</dt> <dd>

Die Nummer des Dialogfelds. Diese Zahl muss im Bereich 0 bis 1 kleiner als der Wert liegen, der als Antwort auf die [**CPL \_ GETCOUNT-Nachricht**](cpl-getcount.md) (CPL \_ GETCOUNT – 1) zurückgegeben wird.

</dd> <dt>

*lpszExtra* 
</dt> <dd>

Eine Zeichenfolge mit zusätzlichen Anweisungen für die Ausführung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn die Nachricht behandelt wurde, andernfalls **FALSE.**

## <a name="remarks"></a>Hinweise

**CPL \_ STARTWPARMS** ähnelt [**CPL \_ DBLCLK,**](cpl-dblclk.md) ermöglicht ihnen jedoch, eine Zeichenfolge an [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) statt an **int zu übergeben.** Sie können diese Zeichenfolge als flexible Möglichkeit verwenden, um detaillierte Anweisungen für die Ausführung zur Verfügung zu stellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional nur Windows \[ XP-Desktop-Apps\]<br/>           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Cpl.h</dt> </dl> |



 

 
