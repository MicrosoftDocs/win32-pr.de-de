---
title: Activate-Methode
description: Activate-Methode
ms.assetid: 8111139d-1453-416e-8f08-38c06669ff4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21df1965abaeed35e9e440a0f559f5e12d68d6fe
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106340489"
---
# <a name="activate-method"></a>Activate-Methode

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>[**Beschreibung**](../wmformat/description.md)
</dt> <dd>

Legt den aktiven Client oder das Zeichen fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent ***. Zeichen ("*** Merkmal-ID * * *").* *  \[ *Zustand* aktivieren\]



| Teil    | Beschreibung                                                                                                                                                                           |
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Zustand* | Dies ist optional. Sie können die folgenden Werte für diesen Parameter angeben: 0 nicht der aktive Client.<br/> 1 der aktive Client. <br/> 2 (Standard) das oberste Zeichen.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn mehrere Zeichen sichtbar sind, empfängt nur eines der Zeichen Spracheingaben gleichzeitig. Wenn mehrere Client Anwendungen dasselbe Zeichen gemeinsam verwenden, empfängt auch nur einer der Clients Maus Eingaben (z. b. Click-oder Drag-Ereignisse der Microsoft-agentsteuerung). Der Zeichensatz für den Empfang von Maus-und Spracheingaben ist das oberste Zeichen, und der Client, der die Eingabe empfängt, ist der aktive Client dieses Zeichens. (Das Fenster des obersten Zeichens wird auch am oberen Rand der z-Reihenfolge des Zeichen Fensters angezeigt.) In der Regel bestimmt der Benutzer das oberste Zeichen, indem das Zeichen explizit ausgewählt wird. Die oberste Aktivierung ändert sich jedoch auch, wenn ein Zeichen angezeigt oder ausgeblendet wird (das Zeichen wird zu oder ist nicht mehr die oberste Stelle).

Sie können diese Methode auch verwenden, um explizit zu verwalten, wann der Client Eingaben erhält, die an das Zeichen weitergeleitet werden, z. b. wenn die Anwendung selbst aktiv wird Wenn Sie z. b. " *State* " auf "2" festlegen, wird das Zeichen am meisten, und der Client empfängt alle Maus-und Spracheingabe Ereignisse, die von der Benutzerinteraktion mit dem Daher wird der Client auch zum Eingabe aktiven Client des Zeichens.

Sie können sich jedoch auch als aktiver Client für ein Zeichen festlegen, ohne das Zeichen am höchsten zu machen, indem Sie *State* auf 1 festlegen. Dadurch kann der Client Eingaben empfangen, die an dieses Zeichen weitergeleitet werden, wenn das Zeichen über den höchsten Wert verfügt. Auf ähnliche Weise können Sie festlegen, dass der Client nicht der aktive Client (nicht für den Empfang von Eingaben) ist, wenn das Zeichen am meisten ist, indem Sie den *Status* auf 0 festlegen.

Vermeiden Sie das Aufrufen dieser Methode direkt nach einer [**Show**](/previous-versions/visualstudio/foxpro/d79z7xxa(v=vs.71)) -Methode. **Anzeigen** legt automatisch den Eingabe aktiven Client fest. Wenn das Zeichen ausgeblendet ist, kann der [**Aktivierungs**](/previous-versions/visualstudio/foxpro/01ayxx68(v=vs.71)) Befehl fehlschlagen, wenn er verarbeitet wird, bevor die **Show** -Methode abgeschlossen wird.

Wenn Sie diese Methode für eine Funktion aufzurufen, wird ein boolescher Wert zurückgegeben, der angibt, ob die Methode erfolgreich ausgeführt wurde. Wenn Sie versuchen, diese Methode mit dem *State* -Parameter aufzurufen, wenn das angegebene Zeichen ausgeblendet ist, tritt ein Fehler auf. Wenn Sie den *Status* auf 0 festlegen und die Anwendung der einzige Client ist, tritt bei diesem Vorgang ein Fehler auf, da ein Zeichen immer über den obersten Client verfügen muss.


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
> Wenn Sie diese Methode mit einem auf 1 festgelegten *Zustand* aufrufen, wird in der Regel kein [**activateinput**](https://www.bing.com/search?q=**ActivateInput**) -Ereignis generiert, es sei denn, es sind keine anderen Zeichen geladen, oder die Anwendung ist bereits Eingabe aktiv.

 

## <a name="see-also"></a>Weitere Informationen

[**Activateinput-Ereignis**](activateinput-event.md), [ **Ereignis "deaktiviert** "](deactivateinput-event.md)


 

