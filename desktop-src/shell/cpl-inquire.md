---
description: 'CPL_INQUIRE Meldung: Wird an die CPlApplet-Funktion einer Systemsteuerung Anwendung gesendet, um Informationen zu einem Dialogfeld anzufordern, das von der Anwendung unterstützt wird.'
title: CPL_INQUIRE-Nachricht (Cpl.h)
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
ms.openlocfilehash: 5998e26eab79d3e5f0b9e3628614e1cc2ecbfb7040e866a898a09ad54fa49f10
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710720"
---
# <a name="cpl_inquire-message"></a>\_CPL-BENACHRICHTIGUNGsmeldung

Wird an die [**CPlApplet-Funktion**](/windows/win32/api/cpl/nc-cpl-applet_proc) einer Systemsteuerung Anwendung gesendet, um Informationen zu einem Dialogfeld anzufordern, das von der Anwendung unterstützt wird.

## <a name="parameters"></a>Parameter

<dl> <dt>

*uAppNum* 
</dt> <dd>

Die Nummer des Dialogfelds. Diese Zahl muss im Bereich 0 (null) bis 1 kleiner als der Wert liegen, der als Antwort auf die [**CPL \_ GETCOUNT-Nachricht**](cpl-getcount.md) (CPL \_ GETCOUNT – 1) zurückgegeben wird.

</dd> <dt>

*lpcpli* 
</dt> <dd>

Die Adresse einer [**CPLINFO-Struktur.**](/windows/win32/api/cpl/ns-cpl-cplinfo) Die Anwendung muss diese Struktur mit Ressourcenbezeichnern für das Symbol, den Kurznamen, die Beschreibung und jeden benutzerdefinierten Wert füllen, der dem Dialogfeld zugeordnet ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die [**CPlApplet-Funktion**](/windows/win32/api/cpl/nc-cpl-applet_proc) diese Nachricht erfolgreich verarbeitet, sollte sie 0 (null) zurückgeben.

## <a name="remarks"></a>Hinweise

Der Systemsteuerung sendet die **\_ CPL-NACHRICHT FÜR** JEDES dialogfeld, das von Ihrer Anwendung unterstützt wird, einmal. Der Systemsteuerung sendet auch eine [**CPL \_ NEWINQUIRE-Nachricht**](cpl-newinquire.md) für jedes Dialogfeld. Diese Nachrichten werden unmittelbar nach der [**CPL \_ GETCOUNT-Nachricht**](cpl-getcount.md) gesendet. Das System garantiert jedoch nicht die Reihenfolge, in der die **\_ CPL-NACHRICHTEN UND CPL** **\_ NEWINQUIRE** gesendet werden.

Sie können die Initialisierung für das Dialogfeld ausführen, wenn Sie **\_ CPL-BENACHRICHTIGUNG** erhalten. Wenn Sie Arbeitsspeicher belegen müssen, tun Sie dies als Reaktion auf die [**\_ CPL-INIT-Nachricht.**](cpl-init.md)

Die [**CPL \_ NEWINQUIRE-Nachricht**](cpl-newinquire.md) gibt Informationen in einer Form zurück, die das System nicht zwischenspeichern kann. Aus diesem Grund sollten die meisten [**CPlApplet-Funktionen**](/windows/win32/api/cpl/nc-cpl-applet_proc) **\_ CPL-ANFORDERUNGEN** verarbeiten und **CPL \_ NEWINQUIRE** ignorieren.

Die einzigen Anwendungen, die [**CPL \_ NEWINQUIRE**](cpl-newinquire.md) verwenden sollten, sind anwendungen, die ihr Symbol ändern oder Zeichenfolgen basierend auf dem Zustand des Computers anzeigen müssen. In diesem Fall sollte Ihr **\_ CPL-HANDLER DEN** \_ CPL DYNAMIC \_ RES-Wert für die **Member idIcon,** **idName** oder **idInfo** der [**CPLINFO-Struktur**](/windows/win32/api/cpl/ns-cpl-cplinfo) angeben, anstatt einen gültigen Ressourcenbezeichner anzugeben. Dadurch sendet die Systemsteuerung die **CPL \_ NEWINQUIRE-Nachricht** jedes Mal, wenn sie das Symbol benötigt, und zeigt Zeichenfolgen an, sodass Sie Informationen basierend auf dem aktuellen Zustand des Computers angeben können. Dies ist erheblich langsamer als die Verwendung von zwischengespeicherten Informationen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Cpl.h</dt> </dl> |



 

 
