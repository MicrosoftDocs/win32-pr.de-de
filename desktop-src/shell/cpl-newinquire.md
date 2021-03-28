---
description: Wird an die CPlApplet-Funktion einer System Steuerungsanwendung gesendet, um Informationen zu einem von der Anwendung unterstützten Dialogfeld anzufordern.
title: CPL_NEWINQUIRE Meldung (cpl. h)
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
ms.openlocfilehash: 72992d4ea867bc091c29feaa99cc1a22c2a02b2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977345"
---
# <a name="cpl_newinquire-message"></a>CPL- \_ netwinquire-Nachricht

Wird an die [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) -Funktion einer System Steuerungsanwendung gesendet, um Informationen zu einem von der Anwendung unterstützten Dialogfeld anzufordern.

## <a name="parameters"></a>Parameter

<dl> <dt>

*uappnum* 
</dt> <dd>

Die Dialogfeld Nummer. Diese Zahl muss zwischen null und einem Wert liegen, der als Antwort auf die [**cpl- \_ GetCount**](cpl-getcount.md) -Nachricht (CPL \_ GetCount – 1) zurückgegeben wird.

</dd> <dt>

*lpncpli* 
</dt> <dd>

Die Adresse einer [**newcplinfo**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) -Struktur. In der System Steuerungsanwendung sollte diese Struktur mit Informationen zum Dialogfeld aufgefüllt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) -Funktion diese Nachricht erfolgreich verarbeitet, sollte Sie 0 (null) zurückgeben.

## <a name="remarks"></a>Bemerkungen

Um eine bessere Leistung zu erzielen, sollten die meisten Anwendungen **cpl \_ newinquire** ignorieren und stattdessen die [**cpl- \_ Anfrage**](cpl-inquire.md) Nachricht verarbeiten.

Die Systemsteuerung sendet für jedes von der Anwendung unterstützte Dialogfeld eine einmalige **cpl \_** -Meldung. In der Systemsteuerung wird auch eine [**cpl- \_ Anfrage**](cpl-inquire.md) Nachricht für jedes Dialogfeld gesendet. Diese Nachrichten werden unmittelbar nach der [**cpl- \_ GetCount**](cpl-getcount.md) -Nachricht gesendet. Das System garantiert jedoch nicht die Reihenfolge, in der die **cpl \_** -Anforderungen und die **cpl- \_ Netzwerkmeldungs** -Nachrichten gesendet werden.

Sie können für das Dialogfeld eine Initialisierung durchführen, wenn Sie eine [**cpl- \_ Anfrage**](cpl-inquire.md)erhalten. Wenn Sie Speicher zuweisen müssen, tun Sie dies als Reaktion auf die [**cpl- \_ Init**](cpl-init.md) -Nachricht.

[**Cpl \_ "Erkundigen**](cpl-inquire.md) " ist die bevorzugte Nachricht. Der Grund hierfür ist, dass **cpl- \_ Netzteil** Informationen in einem Format zurückgibt, das vom System nicht zwischengespeichert werden kann. Folglich müssen Anwendungen, die **cpl- \_ netzwinquire** verarbeiten, jedes Mal geladen werden, wenn die Systemsteuerung die Informationen benötigt, was zu einer deutlichen Verringerung der Leistung führt.

Die einzigen Anwendungen, die **cpl- \_ Netzteil** verwenden sollten, sind diejenigen, die Ihr Symbol ändern oder Zeichen folgen auf der Grundlage des Status des Computers anzeigen müssen. In diesem Fall sollte der [**cpl \_**](cpl-inquire.md) - \_ erstellungshandler den dynamischen cpl- \_ Res-Wert für die Member " **idion**", " **IDName**" oder " **idinfo** " der [**cplinfo**](/windows/win32/api/cpl/ns-cpl-cplinfo) -Struktur angeben, anstatt einen gültigen Ressourcen Bezeichner anzugeben. Dies bewirkt, dass in der Systemsteuerung jedes Mal, wenn das Symbol und die Anzeige Zeichenfolgen benötigt werden, die **cpl- \_ Netzteil** Zeichenfolge gesendet wird, sodass Sie basierend auf dem aktuellen Status des Computers Informationen angeben können. Dies ist natürlich deutlich langsamer als die Verwendung von zwischengespeicherten Informationen.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>CPL. h</dt> </dl> |



 

 
