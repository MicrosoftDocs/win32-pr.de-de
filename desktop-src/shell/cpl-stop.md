---
description: Wird an die CPlApplet-Funktion einer System Steuerungsanwendung gesendet, wenn die Steuerungsanwendung der Systemsteuerung geschlossen wird. Die steuernde Anwendung sendet die Nachricht einmal für jedes Dialogfeld, das von der Anwendung unterstützt wird.
title: CPL_STOP Meldung (cpl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4f632b91-8200-42a3-90cc-a98889704ca4
api_name:
- CPL_STOP
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 78f8926d85b35b8cf5e55188c6cd76b014b3c4c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977337"
---
# <a name="cpl_stop-message"></a>CPL- \_ Stoppmeldung

Wird an die [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) -Funktion einer System Steuerungsanwendung gesendet, wenn die Steuerungsanwendung der Systemsteuerung geschlossen wird. Die steuernde Anwendung sendet die Nachricht einmal für jedes Dialogfeld, das von der Anwendung unterstützt wird.

## <a name="parameters"></a>Parameter

<dl> <dt>

*uappnum* 
</dt> <dd>

Die Dialogfeld Nummer.

</dd> <dt>

*ldata* 
</dt> <dd>

Der Wert, der von der System Steuerungsanwendung in den **lpdata** -Member der [**cplinfo**](/windows/win32/api/cpl/ns-cpl-cplinfo) -oder [**newcplinfo**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) -Struktur für das Dialogfeld geladen wurde. Die Anwendung lädt den **lpdata** -Member als Antwort auf die CPL-Nachrichten-oder- [**cpl \_**](cpl-newinquire.md) -Nachricht. [**\_**](cpl-inquire.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) -Funktion diese Nachricht erfolgreich verarbeitet, sollte Sie 0 (null) zurückgeben.

## <a name="remarks"></a>Bemerkungen

Als Antwort auf diese Nachricht muss eine System Steuerungsanwendung für das angegebene Dialogfeld Eine Bereinigung durchführen.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>CPL. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CPL- \_ Exit**](cpl-exit.md)
</dt> <dt>

[**CPL- \_ GetCount**](cpl-getcount.md)
</dt> </dl>

 

 
