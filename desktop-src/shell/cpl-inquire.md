---
description: 'CPL_INQUIRE: Wird an die CPlApplet-Funktion einer Systemsteuerung-Anwendung gesendet, um Informationen zu einem dialogfeld an anforderungsbasierten Dialog zu erhalten, das von der Anwendung unterstützt wird.'
title: CPL_INQUIRE (Cpl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: daca87b7-f1ee-40f4-95d2-3150b595151e
api_name:
- CPL_INQUIRE
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f9962ff94e8bf80041d7b61ecf97220d573131fb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104468"
---
# <a name="cpl_inquire-message"></a>\_CPL-NACHRICHT ZU 10000000

Wird an die [**CPlApplet-Funktion**](/windows/win32/api/cpl/nc-cpl-applet_proc) einer Systemsteuerung, um Informationen zu einem Von der Anwendung unterstützten Dialogfeld an fordern.

## <a name="parameters"></a>Parameter

<dl> <dt>

*uAppNum* 
</dt> <dd>

Die Nummer des Dialogfelds. Diese Zahl muss im Bereich 0 bis 1 kleiner als der Wert liegen, der als Antwort auf die [**CPL \_ GETCOUNT-Nachricht**](cpl-getcount.md) (CPL \_ GETCOUNT – 1) zurückgegeben wird.

</dd> <dt>

*lpcpli* 
</dt> <dd>

Die Adresse einer [**CPLINFO-Struktur.**](/windows/win32/api/cpl/ns-cpl-cplinfo) Die Anwendung muss diese Struktur mit Ressourcenbezeichnern für das Symbol, den Kurznamen, die Beschreibung und alle benutzerdefinierten Werte füllen, die dem Dialogfeld zugeordnet sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die [**CPlApplet-Funktion**](/windows/win32/api/cpl/nc-cpl-applet_proc) diese Nachricht erfolgreich verarbeitet, sollte sie 0 (null) zurückgeben.

## <a name="remarks"></a>Bemerkungen

Der Systemsteuerung sendet die **\_ CPL-NACHRICHT FÜR ALLE** Dialogfelder, die von Ihrer Anwendung unterstützt werden, einmal. Der Systemsteuerung sendet auch eine [**CPL \_ NEWINQUIRE-Nachricht**](cpl-newinquire.md) für jedes Dialogfeld. Diese Nachrichten werden unmittelbar nach der [**CPL \_ GETCOUNT-Nachricht**](cpl-getcount.md) gesendet. Das System garantiert jedoch nicht die Reihenfolge, in der **die \_ CPL-NACHRICHTEN FÜR DIE NACHRICHTEN ZU UND** **\_ NEWINQUIRE** gesendet werden.

Sie können die Initialisierung für das Dialogfeld ausführen, wenn Sie **\_ CPL-BENACHRICHTIGUNG erhalten.** Wenn Sie Arbeitsspeicher zuordnen müssen, tun Sie dies als Reaktion auf die [**\_ CPL-INIT-Nachricht.**](cpl-init.md)

Die [**\_ CPL-Nachricht NEWINQUIRE**](cpl-newinquire.md) gibt Informationen in einer Form zurück, die das System nicht zwischenspeichern kann. Aus diesem Grund sollten die [**meisten CPlApplet-Funktionen**](/windows/win32/api/cpl/nc-cpl-applet_proc) **\_ CPL-11000000111888888CPL- UND CPL** **\_ NEWINQUIRE-Funktionen ignorieren.**

Die einzigen Anwendungen, die [**CPL \_ NEWINQUIRE**](cpl-newinquire.md) verwenden sollten, sind diejenigen, die ihr Symbol ändern oder Zeichenfolgen basierend auf dem Zustand des Computers anzeigen müssen. In diesem Fall sollte Ihr **\_ CPL-HANDLER DEN** \_ DYNAMISCHEN \_ RES-Wert für die Member **idIcon,** **idName** oder **idInfo** der [**CPLINFO-Struktur**](/windows/win32/api/cpl/ns-cpl-cplinfo) angeben, anstatt einen gültigen Ressourcenbezeichner anzugeben. Dadurch sendet die Systemsteuerung die **CPL \_ NEWINQUIRE-Nachricht** jedes Mal, wenn sie das Symbol benötigt, und zeigt Zeichenfolgen an, sodass Sie Informationen basierend auf dem aktuellen Status des Computers angeben können. Dies ist erheblich langsamer als die Verwendung zwischengespeicherter Informationen.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ XP-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Cpl.h</dt> </dl> |



 

 
