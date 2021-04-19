---
title: Protokoll
description: Gibt an, dass diese OLE 2-Klasse in OLE 1-Containern einfügbar ist.
ms.assetid: 320dff51-ac27-42f3-8c0f-353b29e289d9
keywords:
- COM-Registrierungsschlüssel com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 176cb3fce826a6416270fc35a902621521341e6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338006"
---
# <a name="protocol"></a>Protokoll

Gibt an, dass diese OLE 2-Klasse in OLE 1-Containern einfügbar ist.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   {ProgID}
      Protocol
         StdFileEditing
            Server = path
            Verb
               0 = verb1
               1 = verb2
               ...
```

## <a name="remarks"></a>Bemerkungen

Der Eintrag **stdfileediting** gibt OLE 1-Kompatibilitätsinformationen an. Sie sollte nur vorhanden sein, wenn Objekte dieser Klasse in OLE 1-Containern eingefügt werden können.

Der **Server** gibt den vollständigen Pfad zur OLE 2-Serveranwendung an, und das **Verb** gibt die Verben an. Verb 0 ist das primäre Verb, und zusätzliche Verben müssen nacheinander nummeriert werden.

 

 




