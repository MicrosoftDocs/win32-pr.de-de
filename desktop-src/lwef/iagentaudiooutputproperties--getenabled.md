---
title: Iagentaudiooutputproperties GetEnabled
description: Iagentaudiooutputproperties GetEnabled
ms.assetid: a1e555e1-98f1-4a3d-b6ba-4cd35348db2b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e86b82c720971ae1e14ee294e6d097fd35ca80a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036920"
---
# <a name="iagentaudiooutputpropertiesgetenabled"></a>Iagentaudiooutputproperties:: GetEnabled

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetEnabled(
long * pbEnabled  // address of variable for audio output Enabled setting 
);                      
```

Ruft einen Wert ab, der angibt, ob die Ausgabe der Zeichensprache aktiviert ist.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbenabled*
</dt> <dd>

Adresse einer Variablen, die **true** empfängt, wenn die Sprachausgabe aktuell aktiviert ist, und **false** , wenn Sie deaktiviert ist.

</dd> </dl>

Da sich diese Einstellung auf die gesprochene Ausgabe (TTS und Audiodatei) für alle Zeichen auswirkt, kann nur der Benutzer diese Eigenschaft auf der Eigenschaften Seite des Microsoft-Agents ändern.

 

 




