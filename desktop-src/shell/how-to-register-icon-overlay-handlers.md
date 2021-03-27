---
description: Zusätzlich zur Registrierung des normalen Component Object Model (com) müssen die folgenden Schritte ausgeführt werden, um Symbol Überlagerungs Handler zu registrieren.
ms.assetid: 73EE5E69-969B-409E-9E8F-5837720EA0B3
title: Registrieren von Symbol Überlagerungs Handlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cb58747adc9b754481f43fec825a4588e1606ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994655"
---
# <a name="how-to-register-icon-overlay-handlers"></a>Registrieren von Symbol Überlagerungs Handlern

Zusätzlich zur Registrierung des normalen Component Object Model (com) müssen die folgenden Schritte ausgeführt werden, um Symbol Überlagerungs Handler zu registrieren.

## <a name="instructions"></a>Instructions

### <a name="step-1-create-a-subkey-named-for-the-handler-under-this-key"></a>Schritt 1: Erstellen Sie unter diesem Schlüssel einen Unterschlüssel mit dem Namen für den Handler.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  ShellIconOverlayIdentifiers
```

### <a name="step-2-set-the-default-value-of-the-subkey-to-the-string-form-of-the-objects-class-identifier-clsidguid"></a>Schritt 2: Legen Sie den Standardwert des unter Schlüssels auf die Zeichen folgen Form der Klassen Bezeichner-GUID (CLSID) des Objekts fest.

Im folgenden Beispiel wird veranschaulicht, wie ein Symbol Überlagerungs Handler mit dem Namen myoverlay registriert wird.

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

 

 



