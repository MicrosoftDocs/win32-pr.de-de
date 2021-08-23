---
description: Zusätzlich zur normalen Registrierung Component Object Model (COM) müssen die folgenden Schritte abgeschlossen werden, um Symbolüberlagerungshandler zu registrieren.
ms.assetid: 73EE5E69-969B-409E-9E8F-5837720EA0B3
title: Registrieren von Symbolüberlagerungshandlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a0e62d95b224b131f03c2bd976ddf7c01d7cb3de7ad6995f21568dc7e990d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714910"
---
# <a name="how-to-register-icon-overlay-handlers"></a>Registrieren von Symbolüberlagerungshandlern

Zusätzlich zur normalen Registrierung Component Object Model (COM) müssen die folgenden Schritte abgeschlossen werden, um Symbolüberlagerungshandler zu registrieren.

## <a name="instructions"></a>Anweisungen

### <a name="step-1-create-a-subkey-named-for-the-handler-under-this-key"></a>Schritt 1: Erstellen eines Unterschlüssels mit dem Namen für den Handler unter diesem Schlüssel

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  ShellIconOverlayIdentifiers
```

### <a name="step-2-set-the-default-value-of-the-subkey-to-the-string-form-of-the-objects-class-identifier-clsidguid"></a>Schritt 2: Festlegen des Standardwerts des Unterschlüssels auf die Zeichenfolgenform des Klassenbezeichners (CLSID)GUID des Objekts

Im folgenden Beispiel wird veranschaulicht, wie sie einen Symbolüberlagerungshandler namens MyOverlay registrieren.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  ShellIconOverlayIdentifiers
                     MyOverlay
                        (Default) = {MyOverlay CLSID GUID}
```

 

 



