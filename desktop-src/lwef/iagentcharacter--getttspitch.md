---
title: Iagentcharacter getttspitch
description: Iagentcharacter getttspitch
ms.assetid: b21ae1f1-daf6-42e5-9c52-f28722180021
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dff1bb7999795cf27e29a7d064dd500b47bb419
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339240"
---
# <a name="iagentcharactergetttspitch"></a>Iagentcharacter:: getttspitch

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetTTSPitch(
   long * pdwPitch  // address of variable for character TTS pitch
);
```

Ruft die Einstellung für die TTS-Ausgabe Tonhöhe des Zeichens ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pdwPitch"></span><span id="pdwpitch"></span><span id="PDWPITCH"></span>*pdwpitch*
</dt> <dd>

Adresse einer Variablen, die die aktuelle TTS-Erstellungs Einstellung des Zeichens in Hertz empfängt.

</dd> </dl>

Obwohl Ihre Anwendung diesen Wert nicht schreiben kann, können Sie tagtags in den Ausgabetext einschließen, der die Tonhöhe für eine bestimmte Äußerung temporär vergrößert. Diese Methode gilt nur für Zeichen, die für die TTS-Ausgabe konfiguriert sind. Wenn die Funktion für die Sprachsynthese (TTS) nicht aktiviert (oder installiert) ist oder das Zeichen keine TTS-Ausgabe unterstützt, gibt diese Methode 0 (null) zurück.

 

 




