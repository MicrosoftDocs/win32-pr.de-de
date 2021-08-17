---
title: ListenComplete-Ereignis
description: ListenComplete-Ereignis
ms.assetid: 29e3f424-17b4-4287-b644-ed62b80e0035
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d25e9bfbf23c6a2911c718b576c99395ef06fd802853b39b699384a9ab92429b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883892"
---
# <a name="listencomplete-event"></a>ListenComplete-Ereignis

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Tritt ein, wenn der Lauschenmodus (Spracherkennung) beendet wurde.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

 *Sub-Agent.**ListenComplete (ByVal* *  *CharacterID*, **ByVal** *Cause**)**



| Teil          | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Gibt die ID des lauschenden Zeichens als Zeichenfolge zurück.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| *Ursache*       | Gibt die Ursache des vollständigen Ereignisses als ganze Zahl zurück, die eine der folgenden sein kann: 1 Der Lauschenmodus wurde durch Programmcode deaktiviert.<br/> 2 Beim Lauschenmodus (durch Programmcode aktiviert) ist ein Time out erfolgt.<br/> 3 Time out (durch die Abhörtaste aktiviert) des Lauschenmodus.<br/> 4 Der Lauschenmodus wurde deaktiviert, da der Benutzer die Abhörtaste losgelassen hat.<br/> 5 Der Lauschenmodus wurde beendet, weil der Benutzer das Sprechen beendet hat.<br/> 6 Der Lauschenmodus wurde beendet, weil der eingabeaktive Client deaktiviert wurde.<br/> 7 Der Lauschenmodus wurde beendet, weil das Standardzeichen geändert wurde.<br/> 8 Der Lauschenmodus wurde beendet, weil der Benutzer die Spracheingabe deaktiviert hat.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Hinweise

Dieses Ereignis wird an alle Clients gesendet, wenn das Time out im Lauschenmodus endet, nachdem der Benutzer den Abhörschlüssel veröffentlicht hat, wenn der aktive Eingabeclient die [**Listen-Methode**](listen-method.md) mit **False** aufruft oder der Benutzer das Sprechen beendet hat. Sie können dieses Ereignis verwenden, um zu bestimmen, wann die Ausgabe gesprochener Zeichen (Audio) fortgesetzt werden soll.

Wenn Sie den Lauschen-Modus mithilfe der Listen-Methode aktivieren und der Benutzer dann die Abhörtaste drückt, wird der Lauschen-Modus zurückgesetzt und fortgesetzt, bis das Time out der Abhörtaste abgeschlossen ist, die Abhörtaste freigegeben wird oder der Benutzer das Sprechen beendet, je nachdem, was später erfolgt. [](listen-method.md) In diesem Fall erhalten Sie erst dann ein **ListenComplete-Ereignis,** wenn der Modus des lauschenden Schlüssels abgeschlossen ist.

Das -Ereignis gibt das Zeichen an die Clients zurück, auf denen dieses Zeichen derzeit geladen ist. Alle anderen Clients erhalten ein NULL-Zeichen (leere Zeichenfolge).

### <a name="see-also"></a>Weitere Informationen

[**ListenStart-Ereignis,**](listenstart-event.md) [ **Listen-Methode**](listen-method.md)


 

 





