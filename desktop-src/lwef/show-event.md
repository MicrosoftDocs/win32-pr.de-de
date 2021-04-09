---
title: Ereignis anzeigen
description: Ereignis anzeigen
ms.assetid: vs|msagent|~\pacontrol_7wrw.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6964164e14c759a971e5ceeda542a5c27131663
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855771"
---
# <a name="show-event"></a>Ereignis anzeigen

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Tritt ein, wenn ein Zeichen angezeigt wird.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

**Sub** *Agent * * * \_ Show (ByVal*- *  *Kenn zeichenkennung*, **ByVal** - *Ursache * * *)**



| Teil          | BESCHREIBUNG                                                                                                                                                                                                                                                                 |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Merkmal-ID* | Gibt die ID des Zeichens zurück, das als Zeichenfolge angezeigt wird.                                                                                                                                                                                                                          |
| *Ursache*       | Gibt einen Wert zurück, der angibt, wodurch das Zeichen angezeigt wurde. 2 der Benutzer hat das Zeichen (mit dem Menü-oder Sprachbefehl) angezeigt.<br/> 4 Ihre Client Anwendung hat das Zeichen angezeigt.<br/> 6 eine andere Client Anwendung hat das Zeichen angezeigt.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Bemerkungen

Der Server sendet dieses Ereignis an alle Clients des Zeichens. Um den aktuellen Status des Zeichens abzufragen, verwenden Sie die [**Visible**](visible-property.md) -Eigenschaft.

### <a name="see-also"></a>Weitere Informationen

[**Ereignis ausblenden**](hide-event.md), [ **visibilitycause**](visibilitycause-property.md)


 

 





