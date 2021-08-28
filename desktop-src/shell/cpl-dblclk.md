---
description: Wird an die CPlApplet-Funktion einer Systemsteuerung gesendet, wenn der Benutzer auf das Symbol eines dialogfelds doppelklickt, das von der Anwendung unterstützt wird.
title: CPL_DBLCLK (Cpl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 68d74372-2fc2-45ed-8f77-574b943d28fa
api_name:
- CPL_DBLCLK
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9faf3f589e9e3e69c3b8df82bbb6eb2c075d6fba2836b9d8e773b392ad9385c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119351350"
---
# <a name="cpl_dblclk-message"></a>\_CPL-DBLCLK-Nachricht

Wird an die [**CPlApplet-Funktion**](/windows/win32/api/cpl/nc-cpl-applet_proc) einer Systemsteuerung gesendet, wenn der Benutzer auf das Symbol eines dialogfelds doppelklickt, das von der Anwendung unterstützt wird.

## <a name="parameters"></a>Parameter

<dl> <dt>

*uAppNum* 
</dt> <dd>

Die Nummer des Dialogfelds. Diese Zahl muss im Bereich 0 bis 1 kleiner als der Wert liegen, der als Antwort auf die [**CPL \_ GETCOUNT-Nachricht**](cpl-getcount.md) (CPL \_ GETCOUNT – 1) zurückgegeben wird.

</dd> <dt>

*lData* 
</dt> <dd>

Der Wert, Systemsteuerung die Anwendung in den **lpData-Member** der [**CPLINFO-**](/windows/win32/api/cpl/ns-cpl-cplinfo) oder [**NEWCPLINFO-Struktur**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) für das Dialogfeld geladen hat. Die Anwendung lädt **den lpData-Member** als Antwort auf die [**\_ CPL-Nachricht BZW. CPL**](cpl-inquire.md) [**\_ NEWINQUIRE.**](cpl-newinquire.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die [**CPlApplet-Funktion**](/windows/win32/api/cpl/nc-cpl-applet_proc) diese Nachricht erfolgreich verarbeitet, ist der Rückgabewert 0 (null). Andernfalls ist er ungleich 0 (null).

## <a name="remarks"></a>Hinweise

Als Reaktion auf diese Meldung muss Systemsteuerung Anwendung das entsprechende Dialogfeld anzeigen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Cpl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**CPL \_ SELECT**](cpl-select.md)
</dt> </dl>

 

 
