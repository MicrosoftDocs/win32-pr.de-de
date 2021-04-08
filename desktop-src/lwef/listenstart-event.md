---
title: ListenStart-Ereignis
description: ListenStart-Ereignis
ms.assetid: 59feacd6-0b9f-4bf4-b544-48de49384312
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19b8cc19ad727f8e9c4606bbbfba7b2e03e7d638
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856788"
---
# <a name="listenstart-event"></a>ListenStart-Ereignis

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Tritt auf, wenn der Empfangsmodus beginnt (Spracherkennung).

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

**Sub** - *Agent. * * * ListenStart (ByVal*- *  *Merkmal-ID * * *)**



| Teil          | BESCHREIBUNG                                            |
|---------------|--------------------------------------------------------|
| *Merkmal-ID* | Gibt die ID des überwachungzeichens als Zeichenfolge zurück. |



 

</dd> </dl>

### <a name="remarks"></a>Bemerkungen

Dieses Ereignis wird an alle Clients gesendet, wenn der Empfangsmodus beginnt, da der Benutzer die Abhör Taste gedrückt hat oder der Eingabe aktive [**Client die Abhör Methode mit**](listen-method.md) **true** aufgerufen hat. Sie können dieses Ereignis verwenden, um zu vermeiden, dass Ihr Zeichen in den Modus "on" (lauschen) wechselt.

Wenn Sie den Empfangsmodus mit der Abhör [**Methode aktivieren**](listen-method.md) und der Benutzer dann die Abhör Taste drückt, wird der Lesemodus zurückgesetzt und fortgesetzt, bis das Timeout für die Überwachung abgeschlossen ist, der Schlüssel für die Überwachung freigegeben wird oder der Benutzer die Sprache abschließt, je nachdem, welcher Wert später angezeigt wird. Wenn der Überwachungsmodus bereits auf on on ist, wird ein zusätzliches **ListenStart** -Ereignis nicht angezeigt, wenn der Benutzer die Abhör Taste drückt.

Das-Ereignis gibt das Zeichen an die Clients zurück, für die zurzeit dieses Zeichen geladen ist. Alle anderen Clients erhalten ein NULL-Zeichen (leere Zeichenfolge).

### <a name="see-also"></a>Weitere Informationen

[**Listencomplete-Ereignis**](listencomplete-event.md), Abhör [ **Methode**](listen-method.md)


 

 




