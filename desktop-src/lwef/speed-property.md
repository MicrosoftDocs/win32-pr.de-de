---
title: Speed-Eigenschaft
description: Speed-Eigenschaft
ms.assetid: 43d0480b-d3a5-4992-a2a5-80eba37221e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaca342dde91965ab381f95671a39c4ba9fdcae040835f09867b3fabf5899a6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118745952"
---
# <a name="speed-property"></a>Speed-Eigenschaft

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt eine long-Ganzzahl zurück, die die aktuelle Geschwindigkeit der Sprachausgabe des Zeichens angibt.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent***. Zeichen ("**_CharacterID_*_"). Geschwindigkeit_*

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Eigenschaft gibt die aktuelle Einstellung für die Sprechausgabegeschwindigkeit für das Zeichen zurück. Für Zeichen, die die TTS-Ausgabe verwenden, gibt die -Eigenschaft die tatsächliche TTS-Ausgabeeinstellung für das Zeichen zurück. Wenn TTS nicht aktiviert ist oder das Zeichen keine TTS-Ausgabe unterstützt, spiegelt die Einstellung die Benutzereinstellung für die Ausgabegeschwindigkeit wider.

Obwohl Ihre Anwendung diesen Wert nicht schreiben kann, können Sie in Ihren Ausgabetext **Markierungen** (Speed) einschließen, die die Ausgabe für eine bestimmte Äußerung vorübergehend beschleunigen. Allerdings wirkt sich die Verwendung des **Markierungstags zum** Ändern der gesprochenen Ausgabe des Zeichens nicht auf die Einstellung der **Speed-Eigenschaft** aus. Weitere Informationen finden Sie unter [Sprachausgabetags.](microsoft-agent-speech-output-tags.md)

 

 




