---
title: IAgentCharacterEx GetVersion
description: IAgentCharacterEx GetVersion
ms.assetid: 78f6d7b6-f72d-4af8-a014-3acd185926f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 864bd0cf53e9dd94a547a459bb17cd477189401d544aebca047ead2f049c1c6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750473"
---
# <a name="iagentcharacterexgetversion"></a>IAgentCharacterEx::GetVersion

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT GetVersion(
   short * psMajor,  // address of major version
   short * psMinor   // address of minor version
);
```

Ruft die Versionsnummer des Zeichenstandard-Animationssets ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="psMajor"></span><span id="psmajor"></span><span id="PSMAJOR"></span>*psMajor*
</dt> <dd>

Adresse einer Variablen, die die Hauptversion empfängt.

</dd> <dt>

<span id="psMinor"></span><span id="psminor"></span><span id="PSMINOR"></span>*psMinor*
</dt> <dd>

Adresse einer Variablen, die die Nebenversion empfängt.

</dd> </dl>

Die Standardversionsnummer des Animationssets wird automatisch festgelegt, wenn Sie sie mit dem Microsoft Agent-Zeichen-Editor erstellen.

 

 




