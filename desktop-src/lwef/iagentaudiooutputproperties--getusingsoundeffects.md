---
title: IAgentAudioOutputProperties GetUsingSoundEffects
description: IAgentAudioOutputProperties GetUsingSoundEffects
ms.assetid: 3ccf90b1-a2aa-482a-9f96-85d735532c11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6750dbfee36039337025a03b9f77573a2134f85d15a56d77b2d512482c7bb0e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118751454"
---
# <a name="iagentaudiooutputpropertiesgetusingsoundeffects"></a>IAgentAudioOutputProperties::GetUsingSoundEffects

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT GetUsingSoundEffects(
long * pbUsingSoundEffects  // address of variable sound effects output 
);                          // setting 
```

Ruft einen Wert ab, der angibt, ob die Ausgabe von Soundeffekten aktiviert ist.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbUsingSoundEffects"></span><span id="pbusingsoundeffects"></span><span id="PBUSINGSOUNDEFFECTS"></span>*pbUsingSoundEffects*
</dt> <dd>

Adresse einer Variablen, die **True** empfängt, wenn die Ausgabe von Soundeffekten derzeit aktiviert ist, und **False** , wenn diese deaktiviert ist.

</dd> </dl>

Soundeffekte für die Animation eines Zeichens werden im Zeichen-Editor des Microsoft-Agents zugewiesen. Da sich diese Einstellung auf die Ausgabe von Soundeffekten für alle Zeichen auswirkt, kann nur der Benutzer diese Eigenschaft im Eigenschaftenblatt des Microsoft-Agents ändern.

 

 




