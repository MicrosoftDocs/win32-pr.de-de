---
title: IAgentCharacter Activate
description: IAgentCharacter Activate
ms.assetid: a81eb62d-709b-46b4-9ff2-c9017f7f853e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7256b1d155b051985c72120283e60896026218ea81d8b2b9c37dc94fb52bb63a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750996"
---
# <a name="iagentcharacteractivate"></a>IAgentCharacter::Activate

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT Activate(
   short sState, // topmost character or client setting
);
```

Legt fest, ob ein Client aktiv oder ein Zeichen ganz oben ist.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.
-   Gibt S \_ FALSE zurück, um anzugeben, dass der Vorgang nicht erfolgreich war.

<dl> <dt>

<span id="sState"></span><span id="sstate"></span><span id="SSTATE"></span>*sState*
</dt> <dd>

Sie können die folgenden Werte für diesen Parameter angeben:



| Wert | BESCHREIBUNG                   |
|-------|-------------------------------|
| 0     | Legen Sie als nicht den aktiven Client fest. |
| 1     | Legen Sie als aktiver Client fest.     |
| 2     | Stellen Sie das oberste Zeichen ein.   |



 

</dd> </dl>

Wenn mehrere Zeichen sichtbar sind, empfängt nur eines der Zeichen spracheingaben gleichzeitig. Wenn mehrere Clientanwendungen dasselbe Zeichen verwenden, empfängt auch nur einer der Clients gleichzeitig Mauseingaben (z. B. Klick- oder Ziehereignisse des Microsoft-Agent-Steuerelements). Der Zeichensatz zum Empfangen von Maus- und Spracheingaben ist das oberste Zeichen, und der Client, der Eingaben empfängt, ist der aktive Client des Zeichens. (Das Fenster des obersten Zeichens wird auch oben in der Z-Reihenfolge des Zeichenfensters angezeigt.) In der Regel bestimmt der Benutzer, welches Zeichen am weitesten oben steht, indem er es explizit auswählt. Die oberste Aktivierung ändert sich jedoch auch, wenn ein Zeichen angezeigt oder ausgeblendet wird (das Zeichen wird bzw. ist nicht mehr das oberste Zeichen).

Sie können diese Methode auch verwenden, um explizit zu verwalten, wann Ihr Client Eingaben empfängt, die an das Zeichen gerichtet sind, z. B. wenn Ihre Anwendung selbst aktiv wird. Wenn Sie beispielsweise **State** auf 2 festlegen, wird das Zeichen ganz oben angezeigt, und Ihr Client empfängt alle Maus- und Spracheingabeereignisse, die aus der Benutzerinteraktion mit dem Zeichen generiert wurden. Aus diesem Grund wird Ihr Client auch zum eingabeaktiven Client des Zeichens. Sie können jedoch auch den aktiven Client für ein Zeichen festlegen, ohne das Zeichen ganz oben zu setzen, indem Sie **State** auf 1 festlegen. Dadurch kann Ihr Client Eingaben empfangen, die an dieses Zeichen geleitet werden, wenn das Zeichen ganz oben wird. Auf ähnliche Weise können Sie festlegen, dass Ihr Client nicht der aktive Client ist (um keine Eingabe zu empfangen), wenn das Zeichen oberster Punkt wird, indem Sie **State** auf 0 festlegen. Sie können mithilfe von [**IAgentCharacter::HasOtherClients**](iagentcharacter--hasotherclients.md)ermitteln, ob ein Zeichen über andere aktuelle Clients verfügt.

Vermeiden Sie den Aufruf dieser Methode direkt nach einer [**Show-Methode.**](iagentcharacter--show.md) **Show** legt den eingabeaktiven Client automatisch fest. Wenn das Zeichen ausgeblendet ist, kann der **Activate-Aufruf** fehlschlagen, wenn er verarbeitet wird, bevor die **Show-Methode** abgeschlossen ist.

Beim Versuch, diese Methode mit dem **State-Parameter** auf 2 (wenn das angegebene Zeichen ausgeblendet ist) auf den Wert 2 zu rufen, wird ein Fehler angezeigt. Wenn Sie State  auf 0 festlegen und Ihre Anwendung der einzige Client ist, schlägt dieser Aufruf ebenfalls fehl. Ein Zeichen muss immer über einen obersten Client verfügen.

> [!Note]  
> Wenn Sie  diese Methode aufrufen, deren Status auf 1 festgelegt ist, wird in der Regel kein [**AgentNotifySink::ActivateInputState-Ereignis**](https://www.bing.com/search?q=**AgentNotifySink::ActivateInputState**) generiert, es sei denn, es werden keine anderen Zeichen geladen, oder Ihre Anwendung ist bereits eingabeaktiv.

 

## <a name="see-also"></a>Weitere Informationen

[**IAgentCharacter::HasOtherClients**](iagentcharacter--hasotherclients.md)


 

 




