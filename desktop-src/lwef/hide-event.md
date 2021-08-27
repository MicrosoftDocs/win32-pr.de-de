---
title: Ereignis ausblenden
description: Ereignis ausblenden
ms.assetid: vs|msagent|~\pacontrol_9yuk.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02974d1d66a22eab24c93fc5c9d29b9c2d0e604082fef9f4f0583ebcf7354576
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062060"
---
# <a name="hide-event"></a>Ereignis ausblenden

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Tritt ein, wenn ein Zeichen ausgeblendet wird.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

 *Sub-Agent** \_ Hide(* *  **ByVal** *CharacterID*, **ByVal** *Cause**)**



| Teil          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Gibt die ID des ausgeblendeten Zeichens als Zeichenfolge zurück.                                                                                                                                                                                                                                                                                                                                                               |
| *Ursache*       | Gibt einen Wert zurück, der angibt, was dazu führte, dass das Zeichen ausblendet. 1 Der Benutzer hat das Zeichen durch Auswählen des Befehls im Popupmenü des Taskleistensymbols des Zeichens oder mithilfe der Spracheingabe verborgen.<br/> 3 Ihre Clientanwendung hat das Zeichen verborgen.<br/> 5 Das Zeichen wurde von einer anderen Clientanwendung verborgen.<br/> 7 Der Benutzer hat das Zeichen durch Auswählen des Befehls im Popupmenü des Zeichens verborgen.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Hinweise

Der Server sendet dieses Ereignis an alle Clients des Zeichens. Verwenden Sie zum Abfragen des aktuellen Status des Zeichens die [**Visible-Eigenschaft.**](visible-property.md)

### <a name="see-also"></a>Weitere Informationen

[**Ereignis anzeigen,**](show-event.md) [ **VisibilityCause**](visibilitycause-property.md)


 

 





