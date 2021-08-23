---
title: Ereignis anzeigen
description: Ereignis anzeigen
ms.assetid: vs|msagent|~\pacontrol_7wrw.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b126c7726f8b8ed3ce1e83162cf41ad3223700630167448ff8a7655817a0604
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975739"
---
# <a name="show-event"></a>Ereignis anzeigen

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Tritt ein, wenn ein Zeichen angezeigt wird.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

 *Sub-Agent** \_ Anzeigen (ByVal* *  *CharacterID*, *ByVal-Ursache))* *



| Teil          | BESCHREIBUNG                                                                                                                                                                                                                                                                 |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Gibt die ID des Zeichens zurück, das als Zeichenfolge angezeigt wird.                                                                                                                                                                                                                          |
| *Ursache*       | Gibt einen Wert zurück, der angibt, wodurch das Zeichen angezeigt wurde. 2 Der Benutzer hat das Zeichen (über das Menü oder den Sprachbefehl) angezeigt.<br/> 4 Ihre Clientanwendung hat das Zeichen angezeigt.<br/> 6 Das Zeichen wurde von einer anderen Clientanwendung gezeigt.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Hinweise

Der Server sendet dieses Ereignis an alle Clients des Zeichens. Verwenden Sie die Visible-Eigenschaft, [](visible-property.md) um den aktuellen Zustand des Zeichens abzufragen.

### <a name="see-also"></a>Weitere Informationen

[**Ereignis ausblenden**](hide-event.md), [ **VisibilityCause**](visibilitycause-property.md)


 

 





