---
title: Defaultcharacters-Änderungs Ereignis
description: Defaultcharacters-Änderungs Ereignis
ms.assetid: 14b86a44-8fd2-4719-b7b5-cdcc618d27cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab92fe04f9c42466d559e9b4610eafc8490556d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388503"
---
# <a name="defaultcharacterchange-event"></a>Defaultcharacters-Änderungs Ereignis

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Tritt ein, wenn der Benutzer das Standard Zeichen ändert.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

**Sub** - *Agent. * * * defaultcharakterienänderung* *  **(ByVal** - *GUID * * *)**



| Teil   | BESCHREIBUNG                                      |
|--------|--------------------------------------------------|
| *GUID* | Gibt den eindeutigen Bezeichner für das Zeichen zurück. |



 

</dd> </dl>

### <a name="remarks"></a>Bemerkungen

Dieses Ereignis zeigt an, dass der Benutzer das als Standard Zeichen des Benutzers zugewiesene Zeichen geändert hat. Der Server sendet dies nur an Clients, die das Standard Zeichen geladen haben.

Wenn das neue Zeichen angezeigt wird, wird die gleiche Größe wie jede bereits geladene Instanz des Zeichens oder das vorherige Standard Zeichen (in dieser Reihenfolge) angenommen.

### <a name="see-also"></a>Weitere Informationen

[**Showdefaultcharakteriproperties-Methode**](showdefaultcharacterproperties-method.md), [ **Load-Methode**](load-method.md)


 

 




