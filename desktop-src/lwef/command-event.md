---
title: Befehls Ereignis
description: Befehls Ereignis
ms.assetid: 3e180286-dfa0-4b34-90ee-3267ed6f48af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5647e7eac3aaba0a6094be6b52cc3726eba34ad7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038959"
---
# <a name="command-event"></a>Befehls Ereignis

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Tritt ein, wenn der Benutzer einen (Client)-Befehl auswählt.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

**Sub-** *Agent*- \_ **Befehl** **(ByVal** *UserInput * * *)**



| Teil        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *UserInput* | Identifiziert das [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt, das vom Server zurückgegeben wird. <br/> Der Zugriff auf die folgenden Eigenschaften kann über das [**Command**](/windows/desktop/lwef/the-command-object) -Objekt erfolgen:<br/> Merkmal-ID <br/> Ein Zeichen folgen Wert, der den Namen (ID) des Zeichens identifiziert, das den Befehl empfangen hat. <br/> [**Name**](name-property.md)<br/> Ein Zeichen folgen Wert, der den Namen (ID) des Befehls identifiziert.<br/> [**Confidence**](confidence-property.md)<br/> Ein Long Integer-Wert, der die Vertrauenswürdigkeit für den Befehl angibt. <br/> [**Sprache**](voice-property.md) <br/> Ein Zeichen folgen Wert, der den sprach Text für den Befehl identifiziert.<br/> Alt1Name <br/> Ein Zeichen folgen Wert, der den Namen des nächsten (zweiten) besten Befehls identifiziert.<br/> Alt1Confidence <br/> Ein Long Integer-Wert, der die vertrauensbewertung für den nächsten (zweiten) besten Befehl angibt.<br/> Alt1Voice <br/> Ein Zeichen folgen Wert, der den Stimm Text für die nächste beste Alternative Befehls Übereinstimmung identifiziert.<br/> Alt2Name <br/> Ein Zeichen folgen Wert, der den Namen der dritten optimalen Befehls Übereinstimmung identifiziert.<br/> Alt2Confidence <br/> Eine lange ganze Zahl, die die Vertrauenswürdigkeit für die dritte beste Befehls Übereinstimmung identifiziert.<br/> Alt2Voice <br/> Ein Zeichen folgen Wert, der den sprach Text für die dritte beste Befehls Übereinstimmung identifiziert.<br/> [**Countdown**](count-property.md) <br/> Long Integer-Wert, der die Anzahl der zurückgegebenen Alternativen angibt.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Bemerkungen

Der Server benachrichtigt Sie mit diesem Ereignis, wenn die Anwendung aktiv ist, und der Benutzer wählt einen Befehl durch eine gesprochene Eingabe oder ein Popupmenü des Zeichens aus. Das Ereignis gibt die Anzahl der möglichen übereinstimmenden Befehle in [**count**](count-property.md) sowie den Namen, die vertrauensbewertung und den Stimm Text für diese Übereinstimmungen zurück.

Wenn die Spracheingabe dieses Ereignis auslöst, gibt der Server eine Zeichenfolge zurück, die die beste Entsprechung im [**Name**](name-property.md) -Parameter sowie die zweite und dritte Entsprechung in Alt1Name und Alt2Name angibt. Eine leere Zeichenfolge gibt an, dass die Eingabe keinem von der Anwendung definierten Befehl entspricht. Dies kann z. b. einer der definierten Befehle des Servers sein. , Wenn der Befehl mit dem Befehl des Agents übereinstimmt. Wenn Sie z. b. ausblenden, wird eine leere Zeichenfolge im **Name** -Parameter zurückgegeben, aber Sie erhalten weiterhin den im [**Voice**](voice-property.md) -Parameter gehörenden Text.

Möglicherweise erhalten Sie denselben Befehlsnamen, der in mehr als einem Eintrag zurückgegeben wurde. Die Parameter " [**Confidence**](confidence-property.md)", "Alt1Confidence" und "Alt2Confidence" geben die relativen Bewertungen im Bereich von-100 bis 100 zurück, die von der sprach Erkennungs-Engine für jede entsprechende Entsprechung zurückgegeben werden. Die Parameter [**Voice**](voice-property.md), Alt1Voice und Alt2Voice geben den sprach Text zurück, den die sprach Erkennungs-Engine für jede Alternative abgeglichen hat. Wenn [**count**](count-property.md) 0 (null) zurückgibt, hat der Server gesprochene Eingaben erkannt, aber es wurde festgestellt, dass es keinen übereinstimmenden Befehl gab.

Wenn die Spracheingabe nicht die Quelle für den Befehl war, z. b. wenn der Benutzer den Befehl aus dem Popupmenü des Zeichens ausgewählt hat, gibt der Server den Namen (ID) des Befehls zurück, der in der [**Name**](name-property.md)-Eigenschaft ausgewählt ist. Außerdem wird der Wert des " [**Confidence**](confidence-property.md) "-Parameters als "100" und der Wert der [**sprach**](voice-property.md) Parameter als leere Zeichenfolge ("") zurückgegeben. Alt1Name und Alt2Name geben auch leere Zeichen folgen zurück. Alt1Confidence und Alt2Confidence geben 0 (null) zurück, und Alt1Voice und Alt2Voice geben leere Zeichen folgen zurück. [**Count**](count-property.md) gibt 1 zurück.

> [!Note]  
> Nicht alle Spracherkennungs-Engines geben möglicherweise alle Werte für alle Parameter dieses Ereignisses zurück. Wenden Sie sich an den Hersteller Ihrer Hersteller, um zu ermitteln, ob die Engine die Microsoft Speech API-Schnittstelle für das Zurückgeben von Alternativen und Vertrauens Bewertungen

 

 

