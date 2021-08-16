---
title: GlobalVoiceCommandsEnabled-Eigenschaft
description: GlobalVoiceCommandsEnabled-Eigenschaft
ms.assetid: d4f74019-fa33-41fc-abe7-01791ff188f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f889d242afca406ba443fd3d9a19afb837fbed0390f5c0c3d2bbd2ac2ccbccb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118751444"
---
# <a name="globalvoicecommandsenabled-property"></a>GlobalVoiceCommandsEnabled-Eigenschaft

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt zurück oder legt fest, ob die Stimme für die globalen Befehle des -Agents aktiviert ist.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_"). Commands.GlobalVoiceCommandsEnabled_*

\[ = *Boolean*\]



| Teil      | BESCHREIBUNG                                                                                                                                                                                                            |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Ein boolescher Ausdruck, der angibt, ob Sprachparameter für globale Befehle des -Agents aktiviert sind. **True-Sprachparameter** (Standard) sind aktiviert. <br/> **False** Sprachparameter sind deaktiviert.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Microsoft-Agent fügt automatisch Sprachparameter (Grammatik) zum Öffnen und Schließen des Sprachbefehlsfensters und zum Anzeigen und Ausblenden des Zeichens hinzu. Wenn Sie **GlobalVoiceCommandsEnabled** auf **False** festlegen, deaktiviert der -Agent alle Sprachparameter für diese Befehle sowie die Sprachparameter für die [**Beschriftung**](caption-property.md) der [**Commands-Objekte**](/windows/desktop/lwef/the-commands-collection-object) anderer Clients. Dadurch können Sie diese aus der aktuellen aktiven Grammatik Ihres Clients entfernen. Da dies jedoch den Sprachzugriff auf andere Clients möglicherweise blockiert, setzen Sie diese Eigenschaft nach der Verarbeitung der Spracheingabe des Benutzers auf **True** zurück.

Das Deaktivieren der -Eigenschaft wirkt sich nicht auf das Popupmenü des Zeichens aus. Die vom Server hinzugefügten globalen Befehle werden weiterhin angezeigt. Sie können sie nicht aus dem Popupmenü entfernen.

 

