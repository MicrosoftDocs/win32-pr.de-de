---
title: Activate-Methode
description: Activate-Methode
ms.assetid: 8111139d-1453-416e-8f08-38c06669ff4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5032c7c7f2faf7ec53028a0cc0ce55847fe300864bb531968fc8190b4e00d164
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753159"
---
# <a name="activate-method"></a>Activate-Methode

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>[**Beschreibung**](../wmformat/description.md)
</dt> <dd>

Legt den aktiven Client oder das aktive Zeichen fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent***. Zeichen ("**_CharacterID_*_"). Status_ *  \[ *aktivieren*\]



| Teil    | Beschreibung                                                                                                                                                                           |
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Zustand* | Optional. Sie können die folgenden Werte für diesen Parameter angeben: 0 Nicht der aktive Client.<br/> 1 Der aktive Client. <br/> 2 (Standard) Das oberste Zeichen.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn mehrere Zeichen sichtbar sind, empfängt nur eines der Zeichen spracheingaben gleichzeitig. Wenn mehrere Clientanwendungen dasselbe Zeichen verwenden, empfängt auch nur einer der Clients Mauseingaben (z. B. Klick- oder Ziehereignisse des Microsoft Agent-Steuerelements). Der Zeichensatz zum Empfangen von Maus- und Spracheingaben ist das oberste Zeichen, und der Client, der die Eingabe empfängt, ist der aktive Client dieses Zeichens. (Das Fenster des obersten Zeichens wird auch oben in der Z-Reihenfolge des Zeichenfensters angezeigt.) In der Regel bestimmt der Benutzer das oberste Zeichen, indem er das Zeichen explizit auswählt. Die oberste Aktivierung ändert sich jedoch auch, wenn ein Zeichen angezeigt oder ausgeblendet wird (das Zeichen wird bzw. ist nicht mehr das oberste Zeichen).

Sie können diese Methode auch verwenden, um explizit zu verwalten, wann Ihr Client Eingaben empfängt, die an das Zeichen gerichtet sind, z. B. wenn Ihre Anwendung selbst aktiv wird. Wenn Sie beispielsweise *State* auf 2 festlegen, wird das Zeichen ganz oben angezeigt, und Ihr Client empfängt alle Maus- und Spracheingabeereignisse, die aus der Benutzerinteraktion mit dem Zeichen generiert wurden. Aus diesem Grund wird Ihr Client auch zum eingabeaktiven Client des Zeichens.

Sie können sich jedoch auch selbst als aktiven Client für ein Zeichen festlegen, ohne das Zeichen ganz oben zu setzen, indem Sie *State* auf 1 festlegen. Dadurch kann Ihr Client Eingaben empfangen, die an dieses Zeichen geleitet werden, wenn das Zeichen ganz oben wird. Auf ähnliche Weise können Sie festlegen, dass Ihr Client nicht der aktive Client ist (keine Eingabe zu empfangen), wenn das Zeichen oberster Punkt wird, indem Sie *State* auf 0 festlegen.

Vermeiden Sie den Aufruf dieser Methode direkt nach einer [**Show-Methode.**](/previous-versions/visualstudio/foxpro/d79z7xxa(v=vs.71)) **Show** legt den eingabeaktiven Client automatisch fest. Wenn das Zeichen ausgeblendet ist, kann der [**Activate-Aufruf**](/previous-versions/visualstudio/foxpro/01ayxx68(v=vs.71)) fehlschlagen, wenn er verarbeitet wird, bevor die **Show-Methode** abgeschlossen ist.

Wenn Sie diese Methode für eine Funktion aufrufen, wird ein boolescher Wert zurückgegeben, der angibt, ob die Methode erfolgreich war. Beim Versuch, diese Methode mit dem *State-Parameter* auf 2 aufrufen, wenn das angegebene Zeichen ausgeblendet ist, wird ein Fehler angezeigt. Wenn Sie State  auf 0 festlegen und Ihre Anwendung der einzige Client ist, schlägt dieser Aufruf fehl, da ein Zeichen immer über einen obersten Client verfügen muss.


```
   Dim Genie as Object

   Sub FormLoad()

   Agent1.Characters.Load "Genie", "Genie.acs"

   Set Genie = Agent1.Characters ("Genie")

   If (Genie. Activate = True) Then
      'I'm active

   Else
      'I must be hidden or something

   End If 
   
   End Sub
```



> [!Note]  
> Wenn Sie diese Methode aufrufen, für die *State* auf 1 festgelegt ist, wird in der Regel kein [**ActivateInput-Ereignis**](https://www.bing.com/search?q=**ActivateInput**) generiert, es sei denn, es werden keine anderen Zeichen geladen, oder Ihre Anwendung ist bereits eingabeaktiv.

 

## <a name="see-also"></a>Weitere Informationen

[**ActivateInput-Ereignis,**](activateinput-event.md) [ **DeactivateInput-Ereignis**](deactivateinput-event.md)


 

