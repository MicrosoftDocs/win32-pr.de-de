---
title: SoundEffects-Eigenschaft
description: SoundEffects-Eigenschaft
ms.assetid: 39e48e5f-b24e-48ce-b5a3-85467ac252e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3894782ec3a038831f7bab7d6d5fe0701936baf1c1add136ad5c2c3446f78867
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118246256"
---
# <a name="soundeffects-property"></a>SoundEffects-Eigenschaft

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt einen booleschen Wert zurück, der angibt, ob Soundeffekte (. WAV)-Dateien, die als Teil der Aktionen eines Zeichens konfiguriert sind, werden wiedergegeben.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent wird. AudioOutput.SoundEffects**



| Wert     | BESCHREIBUNG                          |
|-----------|--------------------------------------|
| **True**  | Zeichentoneffekte sind aktiviert. |
| **False** | Der Zeichentoneffekt ist deaktiviert. |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Eigenschaft spiegelt die Option Soundeffekte wiedergeben auf der Seite Ausgabe des Eigenschaftenblatts agent (Erweiterte Zeichenoptionen) wider. Wenn die **SoundEffects-Eigenschaft** **True** zurückgibt, werden Soundeffekte wiedergegeben, die in der Definition eines Zeichens enthalten sind. False gibt an, dass die Soundeffekte nicht wiedergegeben werden. Die Eigenschafteneinstellung wirkt sich auf alle Zeichen aus und ist schreibgeschützt. nur der Benutzer kann diesen Eigenschaftswert festlegen.

## <a name="see-also"></a>Weitere Informationen

[**AgentPropertyChange-Ereignis**](agentpropertychange-event.md)


 

 




