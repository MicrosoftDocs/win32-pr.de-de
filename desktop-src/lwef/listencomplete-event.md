---
title: Listencomplete-Ereignis
description: Listencomplete-Ereignis
ms.assetid: 29e3f424-17b4-4287-b644-ed62b80e0035
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dbfe0fac272b50af3f82efdc8a422bebddbf786
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388667"
---
# <a name="listencomplete-event"></a>Listencomplete-Ereignis

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Tritt auf, wenn der Überwachungsmodus (Spracherkennung) beendet wurde.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

**Sub** *Agent. * * * listencomplete (ByVal*- *  *Kenn zeichenkennung*, **ByVal** - *Ursache * * *)**



| Teil          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Merkmal-ID* | Gibt die ID des überwachungzeichens als Zeichenfolge zurück.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| *Ursache*       | Gibt die Ursache für das Complete-Ereignis als Ganzzahl zurück, die eines der folgenden sein kann: 1 der Empfangsmodus wurde vom Programmcode ausgeschaltet.<br/> Zeitüberschreitung bei 2 Überwachungsmodus (durch Programmcode aktiviert).<br/> beim 3-Empfangsmodus (aktiviert durch den abhörenden Schlüssel) ist ein Timeout aufgetreten.<br/> 4 der Empfangsmodus wurde deaktiviert, da der Benutzer die Abhör Taste losgelassen hat.<br/> 5 der Empfangsmodus wurde beendet, da der Benutzer die Sprache beendet hat.<br/> 6 der Empfangsmodus wurde beendet, weil der Eingabe aktive Client deaktiviert wurde.<br/> 7 der Empfangsmodus wurde beendet, da das Standard Zeichen geändert wurde.<br/> 8 der Empfangsmodus wurde beendet, da der Benutzer die Spracheingabe deaktiviert hat.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Bemerkungen

Dieses Ereignis wird an alle Clients gesendet, wenn das Timeout für den Lesemodus endet, nachdem der Benutzer den Überwachungs Schlüssel losgelassen hat, wenn der aktive [**Client der Eingabe die Abhör Methode mit**](listen-method.md) **false** aufruft oder der Benutzer die Sprache beendet hat. Sie können dieses Ereignis verwenden, um zu bestimmen, wann die Ausgabe eines Zeichens (Audioausgabe) fortgesetzt werden soll.

Wenn Sie den Empfangsmodus mithilfe der Abhör Methode einschalten und der Benutzer dann die Abhör Taste drückt, wird der Lesemodus zurückgesetzt und fortgesetzt, bis das Timeout [**für die Abhör**](listen-method.md) Taste erreicht ist, der Schlüssel für die Überwachung freigegeben wird oder der Benutzer die Sprache abschließt, je nachdem, welcher Wert später angezeigt wird. In dieser Situation wird erst dann ein **listencomplete** -Ereignis empfangen, wenn der Modus des abhörenden Schlüssels abgeschlossen ist.

Das-Ereignis gibt das Zeichen an die Clients zurück, für die zurzeit dieses Zeichen geladen ist. Alle anderen Clients erhalten ein NULL-Zeichen (leere Zeichenfolge).

### <a name="see-also"></a>Weitere Informationen

[**ListenStart-Ereignis**](listenstart-event.md), Abhör [ **Methode**](listen-method.md)


 

 





