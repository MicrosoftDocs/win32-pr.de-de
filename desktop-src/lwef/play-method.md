---
title: Play-Methode (Legacy Windows Umgebungsfeatures)
description: Play-Methode
ms.assetid: 7e89341a-b4d3-4bea-8e7f-31c649ff06b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 980c13cbf11e86a25485558fb3ff2ade703010eb180e86291f206ea152f3c0be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247086"
---
# <a name="play-method-legacy-windows-environment-features"></a>Play-Methode (Legacy Windows Umgebungsfeatures)

\[Microsoft Agent ist ab Version Windows 7 veraltet und möglicherweise in nachfolgenden Versionen von Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt die angegebene Animation für das angegebene Zeichen wieder.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent***. Zeichen ("**_CharacterID_*_"). Play_* "*AnimationName*"

</dd> </dl> 

| Teil            | BESCHREIBUNG                                                          |
|-----------------|----------------------------------------------------------------------|
| *AnimationName* | Erforderlich. Eine Zeichenfolge, die den Namen einer Animationssequenz angibt. |



 

## <a name="remarks"></a>Hinweise

Der Name einer Animation wird definiert, wenn das Zeichen mit dem Microsoft Agent-Zeichen-Editor kompiliert wird. Vor der Wiedergabe der angegebenen Animation versucht der Server, die **Return-Animation** für die vorherige Animation wieder zu spielen, sofern eine animation zugewiesen wurde.

Wenn Sie mithilfe eines herkömmlichen Dateiprotokolls auf die Animationen eines Zeichens zugreifen, können Sie einfach die **Play-Methode** verwenden, die den Namen der Animation an gibt. Wenn Sie jedoch das HTTP-Protokoll für den Zugriff  auf Zeichenanimationsdaten verwenden, verwenden Sie die Get-Methode, um die Animation zu laden, bevor Sie die **Play-Methode** aufrufen.

Weitere Informationen finden Sie unter **Get-Methode.**

Um die Syntax zu vereinfachen, können Sie einen Objektverweis deklarieren und so festlegen, dass er auf das [**Character-Objekt**](/windows/desktop/lwef/the-characters-object) in der [**Characters-Sammlung**](/windows/desktop/lwef/the-characters-object) verweist, und den Verweis als Teil Ihrer **Play-Anweisungen** verwenden:


```
   Dim Genie   
   Agent1.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   Set Genie = Agent1.Characters ("Genie")
   
   Genie.Get "state", "Showing"
   Genie.Show

   Genie.Get "animation", "Greet, GreetReturn"
   Genie.Play "Greet"
   Genie.Speak "Hello."
```



Wenn Sie einen Objektverweis deklarieren und auf diese Methode festlegen, wird ein [**Request-Objekt**](/windows/desktop/lwef/the-request-object) zurückgegeben. Wenn Sie außerdem eine Animation angeben, die nicht geladen wird, oder wenn das Zeichen nicht erfolgreich geladen wurde, legt der Server die [**Status-Eigenschaft**](status-property.md) des **Anforderungsobjekts** mit einer entsprechenden Fehlernummer auf "failed" fest. Wenn die Animation jedoch nicht vorhanden ist und die Daten des Zeichens bereits erfolgreich geladen wurden, löst der Server einen Fehler aus.

Die **Play-Methode** macht das Zeichen nicht sichtbar. Wenn das Zeichen nicht sichtbar ist, gibt der Server die Animation unsichtbar wieder und legt die [**Status-Eigenschaft**](status-property.md) des [**Request-Objekts**](/windows/desktop/lwef/the-request-object) fest.

 

 
