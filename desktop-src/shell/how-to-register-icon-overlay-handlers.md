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
# <a name="how-to-register-icon-overlay-handlers"></a><span data-ttu-id="d5796-103">Registrieren von Symbol Überlagerungs Handlern</span><span class="sxs-lookup"><span data-stu-id="d5796-103">How to Register Icon Overlay Handlers</span></span>

<span data-ttu-id="d5796-104">Zusätzlich zur Registrierung des normalen Component Object Model (com) müssen die folgenden Schritte ausgeführt werden, um Symbol Überlagerungs Handler zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="d5796-104">In addition to normal Component Object Model (COM) registration, the following steps must be completed in order to register icon overlay handlers.</span></span>

## <a name="instructions"></a><span data-ttu-id="d5796-105">Instructions</span><span class="sxs-lookup"><span data-stu-id="d5796-105">Instructions</span></span>

### <a name="step-1-create-a-subkey-named-for-the-handler-under-this-key"></a><span data-ttu-id="d5796-106">Schritt 1: Erstellen Sie unter diesem Schlüssel einen Unterschlüssel mit dem Namen für den Handler.</span><span class="sxs-lookup"><span data-stu-id="d5796-106">Step 1: Create a subkey named for the handler under this key</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  ShellIconOverlayIdentifiers
```

### <a name="step-2-set-the-default-value-of-the-subkey-to-the-string-form-of-the-objects-class-identifier-clsidguid"></a><span data-ttu-id="d5796-107">Schritt 2: Legen Sie den Standardwert des unter Schlüssels auf die Zeichen folgen Form der Klassen Bezeichner-GUID (CLSID) des Objekts fest.</span><span class="sxs-lookup"><span data-stu-id="d5796-107">Step 2: Set the default value of the subkey to the string form of the object's class identifier (CLSID)GUID</span></span>

<span data-ttu-id="d5796-108">Im folgenden Beispiel wird veranschaulicht, wie ein Symbol Überlagerungs Handler mit dem Namen myoverlay registriert wird.</span><span class="sxs-lookup"><span data-stu-id="d5796-108">The following example illustrates how to register an icon overlay handler named MyOverlay.</span></span>

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

 

 



