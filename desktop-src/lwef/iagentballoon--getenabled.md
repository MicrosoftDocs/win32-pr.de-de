---
title: Iagentballoon GetEnabled
description: Iagentballoon GetEnabled
ms.assetid: 1a5ea6c0-6150-459f-95eb-a9c7598c1d94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfd78245534b942e7972066ec90179172f7b556c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311381"
---
# <a name="iagentballoongetenabled"></a>Iagentballoon:: GetEnabled

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetEnabled(
  long * pbEnabled  // address of variable for Enabled setting 
);                  // for word balloon
```

Ruft den Wert der [**aktivierten**](enabled-property.md) Eigenschaft für eine Wort Sprechblase ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbenabled*
</dt> <dd>

Die Adresse einer Variablen, die **true** empfängt, wenn die Wort Sprechblase aktiviert ist, und **false** , wenn Sie deaktiviert wird.

</dd> </dl>

Der Microsoft-Agent-Server zeigt automatisch die Word-Sprechblase für eine gesprochene Ausgabe an, sofern diese nicht deaktiviert ist. Die Word-Sprechblase kann für ein Zeichen im Microsoft-Agent-Zeichen-Editor oder (vom Benutzer) für alle Zeichen im Microsoft-Agent-Eigenschaften Blatt deaktiviert werden. Wenn der Benutzer die Wort Sprechblase deaktiviert, kann er vom Client nicht wieder hergestellt werden.

 

 




