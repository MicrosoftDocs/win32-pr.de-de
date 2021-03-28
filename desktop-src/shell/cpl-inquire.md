---
description: Wird an die CPlApplet-Funktion einer System Steuerungsanwendung gesendet, um Informationen zu einem von der Anwendung unterstützten Dialogfeld anzufordern.
title: CPL_INQUIRE Meldung (cpl. h)
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
ms.openlocfilehash: 8f4c75a2610dab9e94a97eb7920c9de43cf44efc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128464"
---
# <a name="cpl_inquire-message"></a>CPL- \_ Anfrage Nachricht

Wird an die [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) -Funktion einer System Steuerungsanwendung gesendet, um Informationen zu einem von der Anwendung unterstützten Dialogfeld anzufordern.

## <a name="parameters"></a>Parameter

<dl> <dt>

*uappnum* 
</dt> <dd>

Die Dialogfeld Nummer. Diese Zahl muss zwischen null und einem Wert liegen, der als Antwort auf die [**cpl- \_ GetCount**](cpl-getcount.md) -Nachricht (CPL \_ GetCount – 1) zurückgegeben wird.

</dd> <dt>

*lpcpli* 
</dt> <dd>

Die Adresse einer [**cplinfo**](/windows/win32/api/cpl/ns-cpl-cplinfo) -Struktur. Die Anwendung muss diese Struktur mit Ressourcen Bezeichner für das Symbol, den Kurznamen, die Beschreibung und jeden benutzerdefinierten Wert ausfüllen, der dem Dialogfeld zugeordnet ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) -Funktion diese Nachricht erfolgreich verarbeitet, sollte Sie 0 (null) zurückgeben.

## <a name="remarks"></a>Bemerkungen

Die Systemsteuerung sendet die **cpl- \_ Anfrage** Nachricht einmal für jedes von der Anwendung unterstützte Dialogfeld. In der Systemsteuerung wird auch eine [**cpl- \_ netzernachricht**](cpl-newinquire.md) für jedes Dialogfeld gesendet. Diese Nachrichten werden unmittelbar nach der [**cpl- \_ GetCount**](cpl-getcount.md) -Nachricht gesendet. Das System garantiert jedoch nicht die Reihenfolge, in der die **cpl \_** -Anforderungen und die **cpl- \_ Netzwerkmeldungs** -Nachrichten gesendet werden.

Sie können für das Dialogfeld eine Initialisierung durchführen, wenn Sie eine **cpl- \_ Anfrage** erhalten. Wenn Sie Speicher zuweisen müssen, tun Sie dies als Reaktion auf die [**cpl- \_ Init**](cpl-init.md) -Nachricht.

Die [**cpl- \_ Netzteil**](cpl-newinquire.md) Meldung gibt Informationen in einem Format zurück, das vom System nicht zwischengespeichert werden kann. Aus diesem Grund sollten die meisten [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) -Funktionen **cpl- \_ Anfragen** verarbeiten und **cpl- \_ newinquire** ignorieren.

Die einzigen Anwendungen, die [**cpl- \_ Netzteil**](cpl-newinquire.md) verwenden sollten, sind diejenigen, die Ihr Symbol ändern oder Zeichen folgen auf der Grundlage des Status des Computers anzeigen müssen. In diesem Fall sollte der **cpl \_** - \_ erstellungshandler den dynamischen cpl- \_ Res-Wert für die Member " **idion**", " **IDName**" oder " **idinfo** " der [**cplinfo**](/windows/win32/api/cpl/ns-cpl-cplinfo) -Struktur angeben, anstatt einen gültigen Ressourcen Bezeichner anzugeben. Dies bewirkt, dass in der Systemsteuerung jedes Mal, wenn das Symbol und die Anzeige Zeichenfolgen benötigt werden, die **cpl- \_ Netzteil** Zeichenfolge gesendet wird, sodass Sie basierend auf dem aktuellen Status des Computers Informationen angeben können. Dies ist deutlich langsamer als die Verwendung von zwischengespeicherten Informationen.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>CPL. h</dt> </dl> |



 

 
