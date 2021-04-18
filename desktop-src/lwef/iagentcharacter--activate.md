---
title: Aktivieren von iagentcharacter
description: Aktivieren von iagentcharacter
ms.assetid: a81eb62d-709b-46b4-9ff2-c9017f7f853e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1e86d2c094da484f528750d433e0fb6608790e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516124"
---
# <a name="iagentcharacteractivate"></a>Iagentcharacter:: Aktivierung

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT Activate(
   short sState, // topmost character or client setting
);
```

Legt fest, ob ein Client aktiv ist oder ob ein Zeichen auf oberster Ebene festgelegt ist.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.
-   Gibt " \_ false" zurück, um anzugeben, dass der Vorgang nicht erfolgreich war.

<dl> <dt>

<span id="sState"></span><span id="sstate"></span><span id="SSTATE"></span>*sState*
</dt> <dd>

Sie können die folgenden Werte für diesen Parameter angeben:



| Wert | BESCHREIBUNG                   |
|-------|-------------------------------|
| 0     | Legen Sie als nicht den aktiven Client fest. |
| 1     | Wird als aktiver Client festgelegt.     |
| 2     | Stellen Sie das oberste Zeichen dar.   |



 

</dd> </dl>

Wenn mehrere Zeichen sichtbar sind, empfängt nur eines der Zeichen Spracheingaben gleichzeitig. Wenn mehrere Client Anwendungen dasselbe Zeichen gemeinsam verwenden, empfängt auch nur einer der Clients Maus Eingaben (z. b. das Click-oder Drag-Ereignis der Microsoft-agentsteuerung) gleichzeitig. Der Zeichensatz für den Empfang von Maus-und Spracheingaben ist das oberste Zeichen, und der Client, der Eingaben empfängt, ist der aktive Client des Zeichens. (Das Fenster des obersten Zeichens wird auch am oberen Rand der z-Reihenfolge des Zeichen Fensters angezeigt.) In der Regel bestimmt der Benutzer, welches Zeichen am höchsten ist, indem es explizit ausgewählt wird. Die oberste Aktivierung ändert sich jedoch auch, wenn ein Zeichen angezeigt oder ausgeblendet wird (das Zeichen wird zu oder ist nicht mehr die oberste Stelle).

Sie können diese Methode auch verwenden, um explizit zu verwalten, wenn der Client Eingaben empfängt, die an das Zeichen weitergeleitet werden, z. b. wenn die Anwendung selbst aktiv wird. Wenn Sie z. b. " **State** " auf "2" festlegen, wird das Zeichen am meisten, und der Client empfängt alle Maus-und Spracheingabe Ereignisse, die von der Benutzerinteraktion mit dem Zeichen Daher wird der Client auch zum Eingabe aktiven Client des Zeichens. Sie können jedoch auch den aktiven Client für ein Zeichen festlegen, ohne das Zeichen am höchsten zu setzen, indem Sie **State** auf 1 festlegen. Dadurch kann der Client Eingaben empfangen, die an dieses Zeichen weitergeleitet werden, wenn das Zeichen über den höchsten Wert verfügt. Entsprechend können Sie festlegen, dass der Client nicht der aktive Client (für den Empfang von Eingaben) ist, wenn das Zeichen am höchsten ist, indem Sie **State** auf 0 festlegen. Mithilfe von [**iagentcharacter:: hasotherclients**](iagentcharacter--hasotherclients.md)können Sie feststellen, ob ein Zeichen über andere aktuelle Clients verfügt.

Vermeiden Sie das Aufrufen dieser Methode direkt nach einer [**Show**](iagentcharacter--show.md) -Methode. **Anzeigen** legt automatisch den Eingabe aktiven Client fest. Wenn das Zeichen ausgeblendet ist, kann der **Aktivierungs** Befehl fehlschlagen, wenn er verarbeitet wird, bevor die **Show** -Methode abgeschlossen wird.

Wenn Sie versuchen, diese Methode mit dem auf 2 festgelegten **State** -Parameter aufzurufen (wenn das angegebene Zeichen ausgeblendet ist), tritt ein Fehler auf. Wenn Sie den **Status** auf 0 festlegen und die Anwendung der einzige Client ist, tritt bei diesem Vorgang ein Fehler auf. Ein Zeichen muss immer über einen obersten Client verfügen.

> [!Note]  
> Wenn Sie diese Methode mit dem auf 1 festgelegten **Zustand** aufrufen, wird in der Regel kein [**agentnotifysink:: activateinputstate**](https://www.bing.com/search?q=**AgentNotifySink::ActivateInputState**) -Ereignis generiert, es sei denn, es sind keine anderen Zeichen geladen, oder die Anwendung ist bereits Eingabe aktiv.

 

## <a name="see-also"></a>Weitere Informationen

[**Iagentcharacter:: hasotherclients**](iagentcharacter--hasotherclients.md)


 

 




