---
title: Pitch-Eigenschaft
description: Pitch-Eigenschaft
ms.assetid: 98b2ada3-93c6-4fa1-bf12-353eb229c30c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e346ea0fbb7ebb819d8f00b2fc6aab1ab95e72f391bddc696da18a49f0b2a09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118475410"
---
# <a name="pitch-property"></a>Pitch-Eigenschaft

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description_"></span><span id="description_"></span><span id="DESCRIPTION_"></span>**Beschreibung** 
</dt> <dd>

Gibt eine Long-Ganzzahl für die Tonhöheneinstellung der Sprachausgabe (Speech Output, TTS) des angegebenen Zeichens zurück.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent***. Zeichen ("**_CharacterID_*_"). Tonhöhe_*

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Eigenschaft gilt nur für Zeichen, die für die TTS-Ausgabe konfiguriert sind. Wenn das Zeichen keine TTS-Ausgabe unterstützt, gibt diese Eigenschaft 0 (null) zurück.

Obwohl Ihre Anwendung diesen Wert nicht schreiben kann, können Sie **Pit-Tags** (Tonhöhe) in Ihren Ausgabetext einschließen, der die Tonhöhe für eine bestimmte Äußerung vorübergehend erhöht. Die Verwendung des **Pit-Tags** zum Ändern der Tonhöhe ändert jedoch nicht die Einstellung der **Pitch-Eigenschaft.** Weitere Informationen finden Sie unter [Sprachausgabetags.](pit-tag.md)

 

 




