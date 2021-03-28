---
description: Gerätegruppen ermöglichen die Angabe der Eigenschaften "Symbole", "Bezeichnung" und "Eigenschaften" für ein beliebiges Gerät, das einen Teil dieser Gruppe deklariert.
ms.assetid: 84433068-A869-479D-8ADA-E8221B38CCAE
title: Angeben eines Symbols, einer Bezeichnung oder eines Geräte Handlers für ein Gerät mithilfe einer Gerätegruppe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e534aa6fa1bc7dbfe1bae3a2825a14f18096176
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959688"
---
# <a name="how-to-specify-an-icon-label-or-device-handler-for-a-device-using-a-device-group"></a>Angeben eines Symbols, einer Bezeichnung oder eines Geräte Handlers für ein Gerät mithilfe einer Gerätegruppe

Gerätegruppen ermöglichen die Angabe der Eigenschaften "Symbole", "Bezeichnung" und "Eigenschaften" für ein beliebiges Gerät, das einen Teil dieser Gruppe deklariert. Wenn es sich bei der Gerätegruppe nicht um eine vom System bereitgestellte Gerätegruppe handelt, wird ein Schlüssel, der die Gerätegruppe definiert, unter dem Schlüssel " **autoplayhandlers** \\ **devicegroups** " hinzugefügt. Sie müssen nicht alle drei Eigenschaften für jede Gruppe festlegen. Sie können nur die Eigenschaften festlegen, die Sie anpassen möchten. Geräten und Geräte Handlern sollten jedoch immer Symbole und Bezeichnungen zugeordnet sein, um die Mindestanforderungen an die Nutzbarkeit zu erfüllen.

## <a name="instructions"></a>Instructions


Im folgenden Beispiel wird ein System mit mehreren angefügten ZIP-Laufwerken verwendet. Erstellen Sie eine Gerätegruppe mit dem Namen "zipdrive", und definieren Sie diese Werte darin, ohne die Symbole, die Bezeichnung und die Werte für den Geräte Bezeichner einzeln anzugeben. Die einzelnen ZIP-Laufwerke werden dann als Mitglied der Gruppe "zipdrive" deklariert.

Definieren Sie zunächst die Gerätegruppe, indem Sie den folgenden *zipdrive* -Schlüssel und seine Werte hinzufügen.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     DeviceGroups
                        ZipDrive
                           Icons [REG_MULTI_SZ] = %SystemRoot%\system32\mydll.dll,-103
                           NoMediaIcons [REG_MULTI_SZ] = %SystemRoot%\system32\mydll.dll,-104
                           Label [REG_SZ] = My Custom Device Label
                           DeviceHandlers [REG_SZ] = MyDeviceHandler
```

Jedes Zip-Laufwerk wird dann als Teil der Gruppe "zipdrive" deklariert und erbt die Eigenschaften der Gruppe. Fügen Sie unter dem Schlüssel **deviceparameters** der Geräte Instanz einen Wert mit dem Namen devicegroup als **Typ \_ REG SZ** hinzu. Der Dateneintrag für diesen Wert ist der Name der Gerätegruppe.

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Enum
            USB
               Vid_059b&Pid_0031
                  059B003112010E93
                     Device Parameters
                        DeviceGroup [REG_SZ] = ZipDrive
```

Sie können auch andere benutzerdefinierte Geräteeigenschaften als Symbole, Bezeichnung und Gerätegruppen unter dem Schlüssel der Gerätegruppe hinzufügen und diese dann auf alle Geräte anwenden, die zu dieser Gerätegruppe gehören.

> [!Note]  
> Eigenschaften, die auf der Geräte Instanzebene definiert werden, haben Vorrang vor den auf Gerätegruppen Ebene definierten Eigenschaften, die wiederum Vorrang vor den Eigenschaften haben, die auf Geräteklassen Ebene definiert sind.

 

 

 



