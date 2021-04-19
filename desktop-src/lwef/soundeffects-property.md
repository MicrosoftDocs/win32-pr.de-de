---
title: Soundebug-Eigenschaft
description: Soundebug-Eigenschaft
ms.assetid: 39e48e5f-b24e-48ce-b5a3-85467ac252e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fca45d373d39d479c62149a131f2a6678e5ecdf5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338179"
---
# <a name="soundeffects-property"></a>Soundebug-Eigenschaft

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt einen booleschen Wert zurück, der angibt, ob Soundeffekte (. WAV-Dateien, die als Teil der Aktionen eines Zeichens konfiguriert wurden, werden wiedergegeben.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent * * *. Audiooutput. soundeffects**



| Wert     | BESCHREIBUNG                          |
|-----------|--------------------------------------|
| **True**  | Soundeffekte für Zeichen sind aktiviert. |
| **False** | Der Soundeffekt des Zeichens ist deaktiviert. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft gibt die Option Sound Effekte für Wiedergabe Zeichen auf der Seite Ausgabe des agenteigenschaftenblatts (erweiterte Zeichen Optionen) wieder. Wenn die **soundebug** -Eigenschaft **true** zurückgibt, werden in der Definition eines Zeichens enthaltene Soundeffekte wiedergegeben. Bei " **false**" werden die Soundeffekte nicht wiedergegeben. Die-Eigenschafts Einstellung wirkt sich auf alle Zeichen aus und ist schreibgeschützt. nur der Benutzer kann diesen Eigenschafts Wert festlegen.

## <a name="see-also"></a>Weitere Informationen

[**Agentpropertychange-Ereignis**](agentpropertychange-event.md)


 

 




