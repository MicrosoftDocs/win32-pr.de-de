---
title: Iagentspeechinputproperties GetEnabled
description: Iagentspeechinputproperties GetEnabled
ms.assetid: 5731f9ad-eb2e-4a79-a724-b3c263235c8c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c95613398bf79b2446d2bc572864f69ad1ad92ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707007"
---
# <a name="iagentspeechinputpropertiesgetenabled"></a>Iagentspeechinputproperties:: GetEnabled

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetEnabled(
   long * pbEnabled  // address of variable for speech recognition engine 
);                   // Enabled setting
```

Ruft einen Wert ab, der angibt, ob die installierte Spracherkennungs-Engine aktiviert ist.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbenabled*
</dt> <dd>

Adresse einer Variablen, die **true** empfängt, wenn die Sprach-Engine aktuell aktiviert ist, und **false** , wenn Sie deaktiviert ist.

</dd> </dl>

 

 




