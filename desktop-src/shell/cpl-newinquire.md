---
description: 'CPL_NEWINQUIRE Meldung: Wird an die CPlApplet-Funktion einer Systemsteuerung Anwendung gesendet, um Informationen zu einem Dialogfeld anzufordern, das von der Anwendung unterstützt wird.'
title: CPL_NEWINQUIRE-Nachricht (Cpl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: af52889c-7180-4690-8ed1-a0eb0a9dff35
api_name:
- CPL_NEWINQUIRE
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f9455f6f2b89d7b63ad663bcd17d31363ab2c97fd1ba923ba22ebec62e0b04d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119456350"
---
# <a name="cpl_newinquire-message"></a>CPL \_ NEWINQUIRE-Nachricht

Wird an die [**CPlApplet-Funktion**](/windows/win32/api/cpl/nc-cpl-applet_proc) einer Systemsteuerung Anwendung gesendet, um Informationen zu einem Dialogfeld anzufordern, das von der Anwendung unterstützt wird.

## <a name="parameters"></a>Parameter

<dl> <dt>

*uAppNum* 
</dt> <dd>

Die Nummer des Dialogfelds. Diese Zahl muss im Bereich 0 (null) bis 1 kleiner als der Wert liegen, der als Antwort auf die [**CPL \_ GETCOUNT-Nachricht**](cpl-getcount.md) (CPL \_ GETCOUNT – 1) zurückgegeben wird.

</dd> <dt>

*lpncpli* 
</dt> <dd>

Die Adresse einer [**NEWCPLINFO-Struktur.**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) Die Systemsteuerung Anwendung sollte diese Struktur mit Informationen zum Dialogfeld füllen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die [**CPlApplet-Funktion**](/windows/win32/api/cpl/nc-cpl-applet_proc) diese Nachricht erfolgreich verarbeitet, sollte sie 0 (null) zurückgeben.

## <a name="remarks"></a>Hinweise

Um eine bessere Leistung zu erzielen, sollten die meisten Anwendungen **CPL \_ NEWINQUIRE** ignorieren und stattdessen die [**\_ CPL-NACHRICHT FÜR ANFORDERUNGEN**](cpl-inquire.md) verarbeiten.

Der Systemsteuerung sendet die **CPL \_ NEWINQUIRE-Nachricht** einmal für jedes dialogfeld, das von Ihrer Anwendung unterstützt wird. Der Systemsteuerung sendet auch eine [**\_ CPL-BENACHRICHTIGUNGsnachricht**](cpl-inquire.md) für jedes Dialogfeld. Diese Nachrichten werden unmittelbar nach der [**CPL \_ GETCOUNT-Nachricht**](cpl-getcount.md) gesendet. Das System garantiert jedoch nicht die Reihenfolge, in der die **\_ CPL-NACHRICHTEN UND CPL** **\_ NEWINQUIRE** gesendet werden.

Sie können die Initialisierung für das Dialogfeld ausführen, wenn Sie [**\_ CPL-BENACHRICHTIGUNG**](cpl-inquire.md)erhalten. Wenn Sie Arbeitsspeicher belegen müssen, tun Sie dies als Reaktion auf die [**\_ CPL-INIT-Nachricht.**](cpl-init.md)

[**CPL \_ DIE BENACHRICHTIGUNG**](cpl-inquire.md) ist die bevorzugte Nachricht. Dies liegt daran, dass **CPL \_ NEWINQUIRE** Informationen in einer Form zurückgibt, die das System nicht zwischenspeichern kann. Folglich müssen Anwendungen, die **CPL \_ NEWINQUIRE** verarbeiten, jedes Mal geladen werden, wenn die Systemsteuerung die Informationen benötigt, was zu einer erheblichen Leistungsreduzierung führt.

Die einzigen Anwendungen, die **CPL \_ NEWINQUIRE** verwenden sollten, sind anwendungen, die ihr Symbol ändern oder Zeichenfolgen basierend auf dem Zustand des Computers anzeigen müssen. In diesem Fall sollte Ihr [**\_ CPL-HANDLER DEN**](cpl-inquire.md) \_ DYNAMISCHEN \_ RES-Wert für die Member **idIcon,** **idName** oder **idInfo** der [**CPLINFO-Struktur**](/windows/win32/api/cpl/ns-cpl-cplinfo) angeben, anstatt einen gültigen Ressourcenbezeichner anzugeben. Dadurch sendet die Systemsteuerung die **CPL \_ NEWINQUIRE-Nachricht** jedes Mal, wenn sie das Symbol benötigt, und zeigt Zeichenfolgen an, sodass Sie Informationen basierend auf dem aktuellen Zustand des Computers angeben können. Dies ist natürlich deutlich langsamer als die Verwendung zwischengespeicherter Informationen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Cpl.h</dt> </dl> |



 

 
