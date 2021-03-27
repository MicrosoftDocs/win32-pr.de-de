---
description: Geräteklassen ermöglichen die Angabe der Eigenschaften "Symbole", "Bezeichnung" und "devicehandlers" für jedes Gerät dieser Klasse.
ms.assetid: E32C1BA6-B520-4809-A9E9-48813C7EBAA4
title: Angeben eines Symbols, einer Bezeichnung oder eines Geräte Handlers für ein Gerät mithilfe einer Geräteklasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46f81ee6fa469a6bec13abbc1d8a088f5fb334ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994654"
---
# <a name="how-to-specify-an-icon-label-or-device-handler-for-a-device-using-a-device-class"></a>Angeben eines Symbols, einer Bezeichnung oder eines Geräte Handlers für ein Gerät mithilfe einer Geräteklasse

Geräteklassen ermöglichen die Angabe der Eigenschaften "Symbole", "Bezeichnung" und "devicehandlers" für jedes Gerät dieser Klasse. Dies ähnelt der Verwendung von Gerätegruppen, aber Geräteklassen und ihre Mitgliedschaften werden von der Hardware bestimmt, anstatt erstellt oder zugewiesen zu werden. Jeder Klassen Schlüssel Name, der die GUID der Plug & Play Geräteschnittstelle ist, befindet sich unter dem **deviceclasses** -Schlüssel. Weisen Sie unter dem Schlüssel der einzelnen Klasse die Werte für Symbole, Bezeichnung und devicehandlers zu.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Schritt 1:

Das folgende Beispiel zeigt die Werte Class Key und devicehandlers für die Volume-Schnittstelle.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     DeviceClasses
                        {53f5630d-b6bf-11d0-94f2-00a0c91efb8b}
                           DeviceHandlers [REG_SZ] = GenericVolumeHandler
```

Sie können auch benutzerdefinierte Geräteeigenschaften unter dem Geräteklassen Schlüssel hinzufügen. Die benutzerdefinierten Geräteeigenschaften gelten dann für alle Geräte in dieser Klasse. Geräten und Geräte Handlern sollten immer Symbole und Bezeichnungen zugeordnet sein, um die Mindestanforderungen an die Nutzbarkeit zu erfüllen.

> [!Note]  
> Eigenschaften, die auf der Geräte Instanzebene definiert werden, haben Vorrang vor den auf Gerätegruppen Ebene definierten Eigenschaften, die wiederum Vorrang vor den Eigenschaften haben, die auf Geräteklassen Ebene definiert sind.

 

 

 



