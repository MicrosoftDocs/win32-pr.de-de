---
title: Geschwindigkeit (Eigenschaft)
description: Geschwindigkeit (Eigenschaft)
ms.assetid: 43d0480b-d3a5-4992-a2a5-80eba37221e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24738ac17d7efac45f2aefe7e4beb5ec018915a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342046"
---
# <a name="speed-property"></a>Geschwindigkeit (Eigenschaft)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt einen Long Integer-Wert zurück, der die aktuelle Geschwindigkeit der Sprachausgabe des Zeichens angibt.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent ***. Zeichen ("*** Merkmal-ID * * *"). Beschleunigt**

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft gibt die aktuelle Sprechgeschwindigkeit der Ausgabegeschwindigkeit für das Zeichen zurück. Für Zeichen, die die TTS-Ausgabe verwenden, gibt die-Eigenschaft die tatsächliche TTS-Ausgabe Einstellung für das Zeichen zurück. Wenn "TTS" nicht aktiviert ist oder das Zeichen keine TTS-Ausgabe unterstützt, gibt die Einstellung die Benutzereinstellung für die Ausgabegeschwindigkeit wieder.

Obwohl Ihre Anwendung diesen Wert nicht schreiben kann, können Sie **SPD** -Tags (Geschwindigkeit) in den Ausgabetext einschließen, um die Ausgabe für eine bestimmte Äußerung vorübergehend zu beschleunigen. Die Verwendung des **SPD** -Tags zum Ändern der gesprochenen Ausgabe des Zeichens wirkt sich jedoch nicht auf die Einstellung für die **Geschwindigkeits** Eigenschaft aus. Weitere Informationen finden Sie unter [Sprachausgabe Tags](microsoft-agent-speech-output-tags.md).

 

 




