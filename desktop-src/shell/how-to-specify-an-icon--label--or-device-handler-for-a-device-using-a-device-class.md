---
description: Geräteklassen ermöglichen die Angabe der Eigenschaften Symbole, Bezeichnung und DeviceHandlers für jedes Gerät dieser Klasse.
ms.assetid: E32C1BA6-B520-4809-A9E9-48813C7EBAA4
title: Angeben eines Symbols, einer Bezeichnung oder eines Gerätehandlers für ein Gerät mithilfe einer Geräteklasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26ef06228d9b533f2793384c0053017f06aca72d05bd64c5333aa2aadca48dcf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111770"
---
# <a name="how-to-specify-an-icon-label-or-device-handler-for-a-device-using-a-device-class"></a>Angeben eines Symbols, einer Bezeichnung oder eines Gerätehandlers für ein Gerät mithilfe einer Geräteklasse

Geräteklassen ermöglichen die Angabe der Eigenschaften Symbole, Bezeichnung und DeviceHandlers für jedes Gerät dieser Klasse. Dies ähnelt der Verwendung von Gerätegruppen, aber Geräteklassen und ihre Mitgliedschaften werden durch die Hardware bestimmt, anstatt erstellt oder zugewiesen zu werden. Each class key name, which is the Plug and Play device interface GUID, is found under the **DeviceClasses** key. Weisen Sie unter dem einzelnen Klassenschlüssel die Werte für Symbole, Bezeichnungen und DeviceHandler zu.

## <a name="instructions"></a>Anweisungen

### <a name="step-1"></a>Schritt 1:

Das folgende Beispiel zeigt die Werte für den Klassenschlüssel und deviceHandlers für die Volumeschnittstelle.

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

Sie können auch benutzerdefinierte Geräteeigenschaften unter dem Geräteklassenschlüssel hinzufügen. Die benutzerdefinierten Geräteeigenschaften gelten dann für alle Geräte in dieser Klasse. Geräte und Gerätehandler sollten immer über zugeordnete Symbole und Bezeichnungen verfügen, um mindestanforderungen an die Benutzerfreundlichkeit zu erfüllen.

> [!Note]  
> Eigenschaften, die auf Geräteinstanzebene definiert werden, haben Vorrang vor Eigenschaften, die auf Gerätegruppenebene definiert sind, die wiederum Vorrang vor Eigenschaften haben, die auf Geräteklassenebene definiert sind.

 

 

 



