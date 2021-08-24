---
title: Protokoll
description: Gibt an, dass diese OLE 2-Klasse in OLE 1-Containern eingefügt werden kann.
ms.assetid: 320dff51-ac27-42f3-8c0f-353b29e289d9
keywords:
- Protokollregistrierungsschlüssel-COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7721e4f90a122fcbc519163d80c1e8e549f2b6aa05526d33d9693783abd1276a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130022"
---
# <a name="protocol"></a>Protokoll

Gibt an, dass diese OLE 2-Klasse in OLE 1-Containern eingefügt werden kann.

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

## <a name="remarks"></a>Hinweise

Der **Eintrag StdFileEditing** gibt OLE 1-Kompatibilitätsinformationen an. Sie sollte nur vorhanden sein, wenn Objekte dieser Klasse in OLE 1-Containern eingefügt werden können.

**Server** gibt den vollständigen Pfad zur OLE 2-Serveranwendung und **Verb** die Verben an. Verb 0 ist das primäre Verb, und zusätzliche Verben müssen nacheinander nummeriert werden.

 

 




