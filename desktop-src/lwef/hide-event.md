---
title: Ereignis ausblenden
description: Ereignis ausblenden
ms.assetid: vs|msagent|~\pacontrol_9yuk.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87d396fb0985cd4c3c2e9647dfe0e7c9126ad9c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856228"
---
# <a name="hide-event"></a>Ereignis ausblenden

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Tritt ein, wenn ein Zeichen ausgeblendet ist.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

**Sub** - *Agent * * * \_ Ausblenden (* *  **ByVal** - *Kenn zeichenkennung*, **ByVal** - *Ursache * * *)**



| Teil          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Merkmal-ID* | Gibt die ID des verborgenen Zeichens als Zeichenfolge zurück.                                                                                                                                                                                                                                                                                                                                                               |
| *Ursache*       | Gibt einen Wert zurück, der angibt, was das Ausblenden des Zeichens bewirkt hat. 1 Benutzer hat das Zeichen verborgen, indem er den Befehl im Popup Menü des Task leisten Symbols des Zeichens oder mithilfe von Spracheingaben ausgewählt hat.<br/> 3 die Client Anwendung hat das Zeichen verborgen.<br/> 5 eine andere Client Anwendung hat das Zeichen verborgen.<br/> 7 Benutzer hat das Zeichen verborgen, indem er den Befehl im Popup Menü des Zeichens ausgewählt hat.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Bemerkungen

Der Server sendet dieses Ereignis an alle Clients des Zeichens. Um den aktuellen Status des Zeichens abzufragen, verwenden Sie die [**Visible**](visible-property.md) -Eigenschaft.

### <a name="see-also"></a>Weitere Informationen

[**Ereignis anzeigen**](show-event.md), [ **visibilitycause**](visibilitycause-property.md)


 

 





