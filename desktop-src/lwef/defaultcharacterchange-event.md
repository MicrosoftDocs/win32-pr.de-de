---
title: DefaultCharacterChange-Ereignis
description: DefaultCharacterChange-Ereignis
ms.assetid: 14b86a44-8fd2-4719-b7b5-cdcc618d27cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eed166608d3f3b874e975ff58f600d24b73b50e293333b841039b2240780b4de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963130"
---
# <a name="defaultcharacterchange-event"></a>DefaultCharacterChange-Ereignis

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Tritt ein, wenn der Benutzer das Standardzeichen ändert.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

 *Sub-Agent.**DefaultCharacterChange* *  **(ByVal-GUID))** *



| Teil   | BESCHREIBUNG                                      |
|--------|--------------------------------------------------|
| *GUID* | Gibt den eindeutigen Bezeichner für das Zeichen zurück. |



 

</dd> </dl>

### <a name="remarks"></a>Hinweise

Dieses Ereignis gibt an, wenn der Benutzer das als Standardzeichen des Benutzers zugewiesene Zeichen geändert hat. Der Server sendet dies nur an Clients, die das Standardzeichen geladen haben.

Wenn das neue Zeichen angezeigt wird, wird die gleiche Größe angenommen wie jede bereits geladene Instanz des Zeichens oder das vorherige Standardzeichen (in dieser Reihenfolge).

### <a name="see-also"></a>Weitere Informationen

[**ShowDefaultCharacterProperties-Methode,**](showdefaultcharacterproperties-method.md) [ **Load-Methode**](load-method.md)


 

 




