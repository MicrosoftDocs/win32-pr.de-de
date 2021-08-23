---
title: ListeningTip-Eigenschaft
description: ListeningTip-Eigenschaft
ms.assetid: 02a678bb-5eb6-495f-b339-35170a44b15e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d6a743eb26d1e2b57d106e72d77c3774938ffe7e56ca4ba4147001d74bb99f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665440"
---
# <a name="listeningtip-property"></a>ListeningTip-Eigenschaft

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt einen booleschen Wert zurück, der die aktuelle Benutzereinstellung für den Lauschenden Tipp angibt.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax** 
</dt> <dd>

*agent wird. SpeechInput.ListeningTip**



| Wert     | BESCHREIBUNG                    |
|-----------|--------------------------------|
| **True**  | Der Lauschendtipp ist aktiviert.  |
| **False** | Der Lauschendtipp ist deaktiviert. |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **ListeningTip-Eigenschaft** gibt an, ob die Option Lauschendes Trinkgeld anzeigen im Eigenschaftenblatt des Microsoft-Agents (Erweiterte Zeichenoptionen) aktiviert ist. Wenn **ListeningTip** **True** zurückgibt und die Spracheingabe aktiviert ist, zeigt der Server das Trinkgeldfenster an, wenn der Benutzer die Taste Lauschen drückt.

## <a name="see-also"></a>Weitere Informationen

[**AgentPropertyChange-Ereignis**](agentpropertychange-event.md)


 

 




