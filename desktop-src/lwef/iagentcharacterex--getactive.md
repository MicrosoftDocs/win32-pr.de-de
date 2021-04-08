---
title: Iagentcharakteriex getactive
description: Iagentcharakteriex getactive
ms.assetid: b14ae69a-a50e-4488-b5a7-33702e6555eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1dab89ee9ba89c5982e34844917334d97169b9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856656"
---
# <a name="iagentcharacterexgetactive"></a>Iagentcharakteriex:: getactive

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetActive(
   short * psState  // address of active state setting
);
```

Ruft ab, ob es sich bei der Client Anwendung um den aktiven Client des Zeichens handelt und ob es sich um das oberste Zeichen handelt.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="psState"></span><span id="psstate"></span><span id="PSSTATE"></span>*psstate*
</dt> <dd>

Adresse einer Variablen, die einen der folgenden Werte für die Zustands Einstellung empfängt:



| Wert                                                              | BESCHREIBUNG                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------|
| Konstante " **Ganzzahl ohne Vorzeichen Short** " Aktivieren von " **\_ notactive" = 0;**<br/>   | Der Client ist nicht der aktive Client des Zeichens.                |
| Konstante " **Ganzzahl ohne Vorzeichen Short** **" \_ aktiviert = 1;**<br/>      | Der Client ist der aktive Client des Zeichens.                    |
| Konstante " **Ganzzahl ohne Vorzeichen Short** **" \_ inputactive = 2;**<br/> | Der Client ist Eingabe aktiv (aktiver Client des obersten Zeichens). |



 

</dd> </dl>

Mit dieser Einstellung können Sie feststellen, ob Sie der aktive Client des Zeichens sind oder ob es sich bei dem Zeichen um das aktive Eingabezeichen handelt. Wenn mehrere Client Anwendungen dasselbe Zeichen gemeinsam verwenden, empfängt der aktive Client des Zeichens Maus Eingaben (z. b. Click-oder Drag-Ereignisse der Microsoft-agentsteuerung). Wenn mehrere Zeichen angezeigt werden, empfängt der aktive Client des obersten Zeichens (auch als Input-Active Client bezeichnet) [**iagentnotifysink:: Command**](iagentnotifysink--command.md) -Ereignisse.

Verwenden Sie die Methode " [**aktivieren**](iagentcharacter--activate.md) ", um festzulegen, ob es sich bei der Anwendung um den aktiven Client des Zeichens handelt, oder um Ihre Anwendung als aktiven Client einzugeben

## <a name="see-also"></a>Weitere Informationen

[**Iagentcharacter:: Aktivierung**](iagentcharacter--activate.md), [ **iagentnotifysinkex:: activeclientchange**](iagentnotifysinkex--activeclientchange.md)


 

 





