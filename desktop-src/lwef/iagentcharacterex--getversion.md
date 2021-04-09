---
title: Iagentcharakteriex GetVersion
description: Iagentcharakteriex GetVersion
ms.assetid: 78f6d7b6-f72d-4af8-a014-3acd185926f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5c72d9304aa689cda83117d57f26c2da776c9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036775"
---
# <a name="iagentcharacterexgetversion"></a>Iagentcharakteriex:: GetVersion

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetVersion(
   short * psMajor,  // address of major version
   short * psMinor   // address of minor version
);
```

Ruft die Versionsnummer des Zeichen Standard-Animations Satzes ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="psMajor"></span><span id="psmajor"></span><span id="PSMAJOR"></span>*psmajor*
</dt> <dd>

Adresse einer Variablen, die die Hauptversion empfängt.

</dd> <dt>

<span id="psMinor"></span><span id="psminor"></span><span id="PSMINOR"></span>*psminor*
</dt> <dd>

Adresse einer Variablen, die die neben Version empfängt.

</dd> </dl>

Die standardmäßige Animations Satz-Versionsnummer wird automatisch festgelegt, wenn Sie Sie mit dem Microsoft-Agent-Zeichen-Editor erstellen.

 

 




