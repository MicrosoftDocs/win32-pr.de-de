---
title: Listeningtip (Eigenschaft)
description: Listeningtip (Eigenschaft)
ms.assetid: 02a678bb-5eb6-495f-b339-35170a44b15e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 402fd970bf902f034fd6ffb713029e3a27095c8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340857"
---
# <a name="listeningtip-property"></a>Listeningtip (Eigenschaft)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt einen booleschen Wert zurück, der die aktuelle Benutzereinstellung für den hörenden Tipp angibt.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax** 
</dt> <dd>

*Agent * * *. Speechinput. listeningtip**



| Wert     | BESCHREIBUNG                    |
|-----------|--------------------------------|
| **True**  | Der Abhör Tipp ist aktiviert.  |
| **False** | Der Abhör Tipp ist deaktiviert. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **listeningtip** -Eigenschaft gibt an, ob die Option zum Anzeigen von Abhör Tipps auf der Eigenschaften Seite des Microsoft-Agents (erweiterte Zeichen Optionen) aktiviert ist. Wenn **listeningtip** **true** zurückgibt und die Spracheingabe aktiviert ist, zeigt der Server das Tip-Fenster an, wenn der Benutzer die Abhör Taste drückt.

## <a name="see-also"></a>Weitere Informationen

[**Agentpropertychange-Ereignis**](agentpropertychange-event.md)


 

 




