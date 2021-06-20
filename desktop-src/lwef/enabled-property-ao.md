---
title: Enabled-Eigenschaft (AudioOutput-Objekt)
description: Erfahren Sie mehr über die Enabled AudioOutput-Objekteigenschaft. Der Microsoft-Agent ist ab Windows 7 veraltet.
ms.assetid: 6526f249-be13-4732-b79e-a9952489461f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b807b4cadcc9a0157b4efa400dd9d0e3cb5cf21a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407343"
---
# <a name="enabled-property-audiooutput-object"></a>Enabled-Eigenschaft (AudioOutput-Objekt)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt einen booleschen Wert zurück, der angibt, ob die Audioausgabe (gesprochen) aktiviert ist.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent wird. AudioOutput.Enabled**



| Wert     | BESCHREIBUNG                               |
|-----------|-------------------------------------------|
| **True**  | (Standard) Die Ausgabe gesprochener Audiodaten ist aktiviert. |
| **False** | Die Ausgabe gesprochener Audiodaten ist deaktiviert.          |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft spiegelt die Option Audioausgabe wiedergeben auf der Seite Ausgabe des Eigenschaftenblatts agent (Erweiterte Zeichenoptionen) wider. Wenn die [**Enabled-Eigenschaft**](enabled-property.md) **True** zurückgibt, erzeugt die [**Speak-Methode**](speak-method.md) eine Audioausgabe, wenn eine kompatible TTS-Engine installiert ist oder Sie Audiodateien für die gesprochene Ausgabe verwenden. Wenn **False** zurückgegeben wird, bedeutet dies, dass die Sprachausgabe nicht installiert ist oder vom Benutzer deaktiviert wurde. Die Eigenschafteneinstellung gilt für alle -Agent-Zeichen und ist schreibgeschützt. nur der Benutzer kann diesen Eigenschaftswert festlegen.

## <a name="see-also"></a>Weitere Informationen

[AgentPropertyChange-Ereignis](agentpropertychange-event.md)


 

 




