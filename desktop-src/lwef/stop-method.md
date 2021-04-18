---
title: Stopmethode (Features der Legacy-Windows-Umgebung)
description: Stop-Methode
ms.assetid: 68372f72-db9c-447c-a3e4-488940c730d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20192634c197559ca54bb8af3d8a29f37beb53e2
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106337280"
---
# <a name="stop-method-legacy-windows-environment-features"></a>Stopmethode (Features der Legacy-Windows-Umgebung)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Beendet die Animation für das angegebene Zeichen.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent ***. Zeichen ("**_Merkmal-ID_*_")._ *  \[ *Anforderung* Abbrechen\]



| Teil      | BESCHREIBUNG                                                                                   |
|-----------|-----------------------------------------------------------------------------------------------|
| *Anforderung* | Dies ist optional. Ein [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt, das einen bestimmten Animations Rückruf angibt. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Um den Anforderungs Parameter anzugeben, müssen Sie eine Variable erstellen und die Animations Anforderung zuweisen, die Sie abbrechen möchten. Wenn Sie den **Anforderungs** Parameter nicht festlegen, beendet der Server alle Animationen für das Zeichen, einschließlich [**Get**](get-method.md) -aufrufen in der Warteschlange, und löscht seine Animations Warteschlange, es sei denn, das Zeichen wird gerade ausgeblendet oder **zeigt** **eine Animation** an. Diese Methode beendet keine **Get** -Aufrufe, die nicht in der Warteschlange stehen.

Um eine bestimmte Animation oder einen [**Get**](get-method.md) -Befehl zu beenden, deklarieren Sie eine Objekt Variable, und weisen Sie die Animations Anforderung dieser Variablen zu:


```
   Dim MyRequest
   Dim Genie

   Agent1.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   Set Genie = Agent1.Characters ("Genie")

   Genie.Get "state", "Showing"
   Genie.Get "animation", "Greet, GreetReturn"

   Genie.Show
   
   'This animation will never play
   Set MyRequest = Genie.Play ("Greet")
   
   Genie.Stop MyRequest
```



Diese Methode generiert kein [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt.

## <a name="see-also"></a>Weitere Informationen

[**StopAll-Methode**](stopall-method.md)


 

 
