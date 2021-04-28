---
description: 'CPL_NEWINQUIRE: Wird an die CPlApplet-Funktion einer Systemsteuerung-Anwendung gesendet, um Informationen zu einem Dialogfeld an fordern, das von der Anwendung unterstützt wird.'
title: CPL_NEWINQUIRE (Cpl.h)
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
ms.openlocfilehash: 90c5adf31c01fbab1b62aafd0714d165092f4e23
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104438"
---
# <a name="cpl_newinquire-message"></a>CPL \_ NEWINQUIRE-Nachricht

Wird an die [**CPlApplet-Funktion**](/windows/win32/api/cpl/nc-cpl-applet_proc) einer Systemsteuerung, um Informationen zu einem Von der Anwendung unterstützten Dialogfeld an fordern.

## <a name="parameters"></a>Parameter

<dl> <dt>

*uAppNum* 
</dt> <dd>

Die Nummer des Dialogfelds. Diese Zahl muss im Bereich 0 bis 1 kleiner als der Wert liegen, der als Antwort auf die [**CPL \_ GETCOUNT-Nachricht**](cpl-getcount.md) (CPL \_ GETCOUNT – 1) zurückgegeben wird.

</dd> <dt>

*lpncpli* 
</dt> <dd>

Die Adresse einer [**NEWCPLINFO-Struktur.**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) Die Systemsteuerung-Anwendung sollte diese Struktur mit Informationen zum Dialogfeld füllen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die [**CPlApplet-Funktion**](/windows/win32/api/cpl/nc-cpl-applet_proc) diese Nachricht erfolgreich verarbeitet, sollte sie 0 (null) zurückgeben.

## <a name="remarks"></a>Bemerkungen

Um eine bessere Leistung zu erzielen, sollten die meisten Anwendungen **CPL \_ NEWINQUIRE** ignorieren und stattdessen die [**\_ CPL-Nachricht FÜR DEN VORGANG VERARBEITEN.**](cpl-inquire.md)

Der Systemsteuerung sendet die **CPL \_ NEWINQUIRE-Nachricht** einmal für jedes Dialogfeld, das von Ihrer Anwendung unterstützt wird. Der Systemsteuerung sendet auch eine [**\_ CPL-NACHRICHT FÜR JEDES**](cpl-inquire.md) Dialogfeld. Diese Nachrichten werden unmittelbar nach der [**CPL \_ GETCOUNT-Nachricht**](cpl-getcount.md) gesendet. Das System garantiert jedoch nicht die Reihenfolge, in der **die \_ CPL-NACHRICHTEN FÜR DIE NACHRICHTEN ZU UND** **\_ NEWINQUIRE** gesendet werden.

Sie können die Initialisierung für das Dialogfeld ausführen, wenn Sie [**\_ CPL-BENACHRICHTIGUNG erhalten.**](cpl-inquire.md) Wenn Sie Arbeitsspeicher zuordnen müssen, tun Sie dies als Reaktion auf die [**\_ CPL-INIT-Nachricht.**](cpl-init.md)

[**CPL \_ DIE**](cpl-inquire.md) VORZUGSMELDUNG ist die bevorzugte Nachricht. Dies liegt **daran, dass CPL \_ NEWINQUIRE** Informationen in einer Form zurückgibt, die das System nicht zwischenspeichern kann. Folglich müssen Anwendungen, die **CPL \_ NEWINQUIRE** verarbeiten, jedes Mal geladen werden, wenn die Systemsteuerung die Informationen benötigt, was zu einer erheblichen Leistungsreduzierung führt.

Die einzigen Anwendungen, die **CPL \_ NEWINQUIRE** verwenden sollten, sind anwendungen, die ihr Symbol ändern oder Zeichenfolgen basierend auf dem Zustand des Computers anzeigen müssen. In diesem Fall sollte Ihr [**\_ CPL-HANDLER DEN**](cpl-inquire.md) \_ DYNAMISCHEN \_ RES-Wert für die Member **idIcon,** **idName** oder **idInfo** der [**CPLINFO-Struktur**](/windows/win32/api/cpl/ns-cpl-cplinfo) angeben, anstatt einen gültigen Ressourcenbezeichner anzugeben. Dadurch sendet die Systemsteuerung die **CPL \_ NEWINQUIRE-Nachricht** jedes Mal, wenn sie das Symbol benötigt, und zeigt Zeichenfolgen an, sodass Sie Informationen basierend auf dem aktuellen Status des Computers angeben können. Dies ist natürlich deutlich langsamer als die Verwendung zwischengespeicherter Informationen.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ XP-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Cpl.h</dt> </dl> |



 

 
