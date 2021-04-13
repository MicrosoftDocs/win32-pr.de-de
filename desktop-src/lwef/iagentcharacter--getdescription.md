---
title: Iagentcharacter GetDescription
description: Iagentcharacter GetDescription
ms.assetid: 729f54ac-1c60-4a7b-b993-5682a6ea2b3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423cd1f5c799cc1f0177f6d3d7922d5d14de1dbe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388814"
---
# <a name="iagentcharactergetdescription"></a>Iagentcharacter:: GetDescription

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetDescription(
   BSTR * pbszDescription   // address of buffer for character description
); 
```

Ruft die Beschreibung des Zeichens ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbszDescription"></span><span id="pbszdescription"></span><span id="PBSZDESCRIPTION"></span>*pbszdescription*
</dt> <dd>

Die Adresse eines BSTR-Werts, der den Wert der Beschreibung für das Zeichen empfängt. Die Beschreibung eines Zeichens wird bei der Kompilierung mit dem Microsoft-Agent-Zeichen-Editor definiert. Die Beschreibungs Einstellung ist optional und kann nicht für alle Zeichen angegeben werden.

</dd> </dl>

 

 




