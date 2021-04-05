---
title: Iagentaudiooutputproperties getusingsoundebug
description: Iagentaudiooutputproperties getusingsoundebug
ms.assetid: 3ccf90b1-a2aa-482a-9f96-85d735532c11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e83314acfc67ce8bea4a0f0d305f6d5d490a92e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710638"
---
# <a name="iagentaudiooutputpropertiesgetusingsoundeffects"></a>Iagentaudiooutputproperties:: getusingsoundebug

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetUsingSoundEffects(
long * pbUsingSoundEffects  // address of variable sound effects output 
);                          // setting 
```

Ruft einen Wert ab, der angibt, ob die Ausgabe der Soundeffekte aktiviert ist.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbUsingSoundEffects"></span><span id="pbusingsoundeffects"></span><span id="PBUSINGSOUNDEFFECTS"></span>*pbusingsounentffects*
</dt> <dd>

Adresse einer Variablen, die **true** empfängt, wenn die Ausgabe der Soundeffekte derzeit aktiviert ist, und **false** , wenn Sie deaktiviert ist.

</dd> </dl>

Sound Effekte für die Animation eines Zeichens werden im Microsoft-Agent-Zeichen-Editor zugewiesen. Da sich diese Einstellung auf die Ausgabe der Soundeffekte für alle Zeichen auswirkt, kann nur der Benutzer diese Eigenschaft auf der Eigenschaften Seite des Microsoft-Agents ändern.

 

 




