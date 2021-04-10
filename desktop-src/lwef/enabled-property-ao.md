---
title: Aktivierte Eigenschaft (Audiooutput-Objekt)
description: Enabled-Eigenschaft
ms.assetid: 6526f249-be13-4732-b79e-a9952489461f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5dff9153a1aa7a6bf5346d46f43f80bf48809c9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104040006"
---
# <a name="enabled-property-audiooutput-object"></a>Aktivierte Eigenschaft (Audiooutput-Objekt)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt einen booleschen Wert zurück, der angibt, ob die (gesprochene) Audioausgabe aktiviert ist.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent * * *. Audiooutput. aktiviert**



| Wert     | BESCHREIBUNG                               |
|-----------|-------------------------------------------|
| **True**  | Vorgegebene Die gesprochene Audioausgabe ist aktiviert. |
| **False** | Die gesprochene Audioausgabe ist deaktiviert.          |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft gibt die Option Wiedergabe Audioausgabe auf der Seite Ausgabe des agenteigenschaftenblatts (erweiterte Zeichen Optionen) wieder. Wenn die [**aktivierte**](enabled-property.md) Eigenschaft **true** zurückgibt, erzeugt die [**Sprech**](speak-method.md) Methode eine Audioausgabe, wenn eine kompatible TTS-Engine installiert ist, oder Sie verwenden Audiodateien für die gesprochene Ausgabe. Wenn **false** zurückgegeben wird, bedeutet dies, dass die Sprachausgabe nicht installiert ist oder vom Benutzer deaktiviert wurde. Die-Eigenschafts Einstellung gilt für alle agentzeichen und ist schreibgeschützt. nur der Benutzer kann diesen Eigenschafts Wert festlegen.

## <a name="see-also"></a>Weitere Informationen

[Agentpropertychange-Ereignis](agentpropertychange-event.md)


 

 




