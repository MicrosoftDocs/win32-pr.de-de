---
title: Stop-Methode (Legacy Windows Umgebungsfeatures)
description: Stop-Methode
ms.assetid: 68372f72-db9c-447c-a3e4-488940c730d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 572a93db5697aaae0dcfed6b45a834323c106bba447d2d9a8e94109f788af25c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118745962"
---
# <a name="stop-method-legacy-windows-environment-features"></a>Stop-Methode (Legacy Windows Umgebungsfeatures)

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Beendet die Animation für das angegebene Zeichen.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent***. Zeichen ("**_CharacterID_*_"). Anforderung_ *  \[ *beenden*\]



| Teil      | Beschreibung                                                                                   |
|-----------|-----------------------------------------------------------------------------------------------|
| *Anforderung* | Optional. Ein [**Request-Objekt,**](/windows/desktop/lwef/the-request-object) das einen bestimmten Animationsaufruf an gibt. |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Um den Anforderungsparameter anzugeben, müssen Sie eine Variable erstellen und die Animationsanforderung zuweisen, die Sie beenden möchten. Wenn Sie den **Request-Parameter** nicht festlegen, beendet der Server alle [](get-method.md) Animationen für das Zeichen, einschließlich get-Aufrufe in der Warteschlange, und bricht seine Animationswarteschlange ab, es sei denn, das Zeichen gibt derzeit seine **Hiding-** oder **Showing-Animation** wieder. Diese Methode stoppt get-Aufrufe, die nicht in der **Warteschlange** stehen, nicht.

Um eine bestimmte Animation oder einen [**Get-Aufruf**](get-method.md) zu beenden, deklarieren Sie eine Objektvariable, und weisen Sie ihre Animationsanforderung dieser Variablen zu:


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



Diese Methode generiert kein [**Request-Objekt.**](/windows/desktop/lwef/the-request-object)

## <a name="see-also"></a>Weitere Informationen

[**StopAll-Methode**](stopall-method.md)


 

 
