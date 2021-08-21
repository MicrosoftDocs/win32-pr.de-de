---
title: ListenStart-Ereignis
description: ListenStart-Ereignis
ms.assetid: 59feacd6-0b9f-4bf4-b544-48de49384312
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0017b628af3ca266058de74508d379bd665c94f94c64207f4d7bef5487a0f4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976110"
---
# <a name="listenstart-event"></a>ListenStart-Ereignis

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Tritt ein, wenn der Lauschenmodus (Spracherkennung) beginnt.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

 *Sub-Agent.**ListenStart (ByVal* *  *CharacterID))**



| Teil          | BESCHREIBUNG                                            |
|---------------|--------------------------------------------------------|
| *CharacterID* | Gibt die ID des lauschenden Zeichens als Zeichenfolge zurück. |



 

</dd> </dl>

### <a name="remarks"></a>Hinweise

Dieses Ereignis wird an alle Clients gesendet, wenn der Lauschenmodus beginnt, da der Benutzer die Abhörtaste oder den eingabeaktiven Client gedrückt hat, der als [**Listen-Methode**](listen-method.md) mit **TRUE bezeichnet wird.** Sie können dieses Ereignis verwenden, um zu vermeiden, dass Ihr Zeichen spricht, während der Lauschen-Modus aktiviert ist.

Wenn Sie den Abhörmodus [](listen-method.md) mit der Listen-Methode aktivieren und der Benutzer dann die Abhörtaste drückt, wird der Lauschen-Modus zurückgesetzt und fortgesetzt, bis das Time out der Abhörtaste abgeschlossen ist, die Abhörtaste freigegeben wird oder der Benutzer das Sprechen beendet, je nachdem, was später erfolgt. Wenn in diesem Fall der Lauschen-Modus bereits aktiviert ist, erhalten Sie kein zusätzliches **ListenStart-Ereignis,** wenn der Benutzer die Abhörtaste drückt.

Das -Ereignis gibt das Zeichen an die Clients zurück, auf denen dieses Zeichen derzeit geladen ist. Alle anderen Clients erhalten ein NULL-Zeichen (leere Zeichenfolge).

### <a name="see-also"></a>Weitere Informationen

[**ListenComplete-Ereignis,**](listencomplete-event.md) [ **Listen-Methode**](listen-method.md)


 

 




