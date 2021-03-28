---
description: Wird gesendet, um das CPlApplet zu benachrichtigen, dass der Benutzer das Symbol ausgewählt hat, das einem bestimmten Dialogfeld zugeordnet ist. CPlApplet sollte das entsprechende Dialogfeld anzeigen und alle benutzerdefinierten Tasks ausführen.
title: CPL_STARTWPARMS Meldung (cpl. h)
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
ms.openlocfilehash: 790779c1c45acbc211fe36e28b2e55d5ae2e60da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958771"
---
# <a name="cpl_startwparms-message"></a>CPL- \_ startwparser-Meldung

Wird gesendet, um das [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) zu benachrichtigen, dass der Benutzer das Symbol ausgewählt hat, das einem bestimmten Dialogfeld zugeordnet ist. **CPlApplet** sollte das entsprechende Dialogfeld anzeigen und alle benutzerdefinierten Tasks ausführen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*uappnum* 
</dt> <dd>

Die Dialogfeld Nummer. Diese Zahl muss zwischen null und einem Wert liegen, der als Antwort auf die [**cpl- \_ GetCount**](cpl-getcount.md) -Nachricht (CPL \_ GetCount – 1) zurückgegeben wird.

</dd> <dt>

*lpszextra* 
</dt> <dd>

Eine Zeichenfolge mit zusätzlichen Ausführungs Anweisungen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn die Meldung behandelt wurde, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

**Cpl \_ Startwparamems** ähnelt [**cpl \_ dblclk**](cpl-dblclk.md) , ermöglicht Ihnen jedoch, eine Zeichenfolge an [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) anstatt an **int** zu übergeben. Sie können diese Zeichenfolge als flexible Möglichkeit zum Bereitstellen von detaillierten Ausführungs Anweisungen verwenden.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>CPL. h</dt> </dl> |



 

 
