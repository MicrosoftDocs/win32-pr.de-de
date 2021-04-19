---
title: Play-Methode (Features der Legacy-Windows-Umgebung)
description: Play-Methode
ms.assetid: 7e89341a-b4d3-4bea-8e7f-31c649ff06b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1d06f4275d7b4c0959a59536c8b20a95c14ab1c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106338104"
---
# <a name="play-method-legacy-windows-environment-features"></a>Play-Methode (Features der Legacy-Windows-Umgebung)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt die angegebene Animation für das angegebene Zeichen wieder.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent ***. Zeichen ("**_Merkmal-ID_*_"). Play_* "*animationname*"

</dd> </dl> 

| Teil            | BESCHREIBUNG                                                          |
|-----------------|----------------------------------------------------------------------|
| *Animationname* | Erforderlich. Eine Zeichenfolge, die den Namen einer Animationssequenz angibt. |



 

## <a name="remarks"></a>Bemerkungen

Der Name einer Animation wird definiert, wenn das Zeichen mit dem Microsoft-Agent-Zeichen-Editor kompiliert wird. Vor der Wiedergabe der angegebenen Animation versucht der Server, die Rückgabe Animation für die vorherige Animation **wiederzugeben** , sofern eine zugewiesen wurde.

Wenn Sie mithilfe eines herkömmlichen Datei Protokolls auf die Animationen eines Zeichens zugreifen, können Sie einfach die **Play** -Methode verwenden, um den Namen der Animation anzugeben. Wenn Sie jedoch das HTTP-Protokoll verwenden, um auf Daten der Zeichen Animation zuzugreifen, verwenden Sie die **Get** -Methode, um die Animation vor dem Aufrufen der **Play** -Methode zu laden.

Weitere Informationen finden Sie unter der **Get** -Methode.

Um die Syntax zu vereinfachen, können Sie einen Objekt Verweis deklarieren und ihn so festlegen, dass er auf das [**Zeichen**](/windows/desktop/lwef/the-characters-object) Objekt in der [**Zeichen**](/windows/desktop/lwef/the-characters-object) Auflistung verweist, und den Verweis als Teil der **Play** -Anweisungen verwenden:


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



Wenn Sie einen Objekt Verweis deklarieren und diesen auf diese Methode festlegen, wird ein [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt zurückgegeben. Wenn Sie außerdem eine Animation angeben, die nicht geladen wurde, oder wenn das Zeichen nicht erfolgreich geladen wurde, legt der Server die [**Status**](status-property.md) -Eigenschaft des **Anforderungs** Objekts auf "failed" (Fehler) mit einer entsprechenden Fehlernummer fest. Wenn die Animation jedoch nicht vorhanden ist und die Daten des Zeichens bereits erfolgreich geladen wurden, löst der Server einen Fehler aus.

Die **Play** -Methode macht das Zeichen nicht sichtbar. Wenn das Zeichen nicht sichtbar ist, spielt der Server die Animation unsichtbar und legt die Eigenschaft [**Status**](status-property.md) des [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekts fest.

 

 
