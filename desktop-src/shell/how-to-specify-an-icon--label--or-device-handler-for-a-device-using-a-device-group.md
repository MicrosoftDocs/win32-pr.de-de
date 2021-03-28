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
# <a name="how-to-specify-an-icon-label-or-device-handler-for-a-device-using-a-device-group"></a><span data-ttu-id="c1f13-103">Angeben eines Symbols, einer Bezeichnung oder eines Geräte Handlers für ein Gerät mithilfe einer Gerätegruppe</span><span class="sxs-lookup"><span data-stu-id="c1f13-103">How to Specify an Icon, Label, or Device Handler for a Device Using a Device Group</span></span>

<span data-ttu-id="c1f13-104">Gerätegruppen ermöglichen die Angabe der Eigenschaften "Symbole", "Bezeichnung" und "Eigenschaften" für ein beliebiges Gerät, das einen Teil dieser Gruppe deklariert.</span><span class="sxs-lookup"><span data-stu-id="c1f13-104">Device groups allow the specification of the Icons, Label, or DeviceHandlers properties for any device that declares itself part of that group.</span></span> <span data-ttu-id="c1f13-105">Wenn es sich bei der Gerätegruppe nicht um eine vom System bereitgestellte Gerätegruppe handelt, wird ein Schlüssel, der die Gerätegruppe definiert, unter dem Schlüssel " **autoplayhandlers** \\ **devicegroups** " hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c1f13-105">If the device group is not a system-provided device group, a key that defines the device group will be added under the **AutoplayHandlers**\\**DeviceGroups** key.</span></span> <span data-ttu-id="c1f13-106">Sie müssen nicht alle drei Eigenschaften für jede Gruppe festlegen. Sie können nur die Eigenschaften festlegen, die Sie anpassen möchten.</span><span class="sxs-lookup"><span data-stu-id="c1f13-106">You do not need to set all three properties for each group; you can set only those properties that you want to customize.</span></span> <span data-ttu-id="c1f13-107">Geräten und Geräte Handlern sollten jedoch immer Symbole und Bezeichnungen zugeordnet sein, um die Mindestanforderungen an die Nutzbarkeit zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="c1f13-107">However, devices and device handlers should always have associated icons and labels to meet minimum usability requirements.</span></span>

## <a name="instructions"></a><span data-ttu-id="c1f13-108">Instructions</span><span class="sxs-lookup"><span data-stu-id="c1f13-108">Instructions</span></span>


<span data-ttu-id="c1f13-109">Im folgenden Beispiel wird ein System mit mehreren angefügten ZIP-Laufwerken verwendet.</span><span class="sxs-lookup"><span data-stu-id="c1f13-109">The following example uses a system with several attached Zip drives.</span></span> <span data-ttu-id="c1f13-110">Erstellen Sie eine Gerätegruppe mit dem Namen "zipdrive", und definieren Sie diese Werte darin, ohne die Symbole, die Bezeichnung und die Werte für den Geräte Bezeichner einzeln anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c1f13-110">Without specifying the Icons, Label, and DeviceHandlers values for each drive individually, you create a device group called ZipDrive and define those values within it.</span></span> <span data-ttu-id="c1f13-111">Die einzelnen ZIP-Laufwerke werden dann als Mitglied der Gruppe "zipdrive" deklariert.</span><span class="sxs-lookup"><span data-stu-id="c1f13-111">Each Zip drive is then declared a member of the ZipDrive group.</span></span>

<span data-ttu-id="c1f13-112">Definieren Sie zunächst die Gerätegruppe, indem Sie den folgenden *zipdrive* -Schlüssel und seine Werte hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c1f13-112">First, define the device group by adding the following *ZipDrive* key and its values.</span></span>

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

<span data-ttu-id="c1f13-113">Jedes Zip-Laufwerk wird dann als Teil der Gruppe "zipdrive" deklariert und erbt die Eigenschaften der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="c1f13-113">Each Zip drive device is then declared as part of the ZipDrive group, inheriting the properties of that group.</span></span> <span data-ttu-id="c1f13-114">Fügen Sie unter dem Schlüssel **deviceparameters** der Geräte Instanz einen Wert mit dem Namen devicegroup als **Typ \_ REG SZ** hinzu.</span><span class="sxs-lookup"><span data-stu-id="c1f13-114">Under the **DeviceParameters** key of the device instance, add a value named DeviceGroup as type **REG\_SZ**.</span></span> <span data-ttu-id="c1f13-115">Der Dateneintrag für diesen Wert ist der Name der Gerätegruppe.</span><span class="sxs-lookup"><span data-stu-id="c1f13-115">The data entry for this value is the name of the device group.</span></span>

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

<span data-ttu-id="c1f13-116">Sie können auch andere benutzerdefinierte Geräteeigenschaften als Symbole, Bezeichnung und Gerätegruppen unter dem Schlüssel der Gerätegruppe hinzufügen und diese dann auf alle Geräte anwenden, die zu dieser Gerätegruppe gehören.</span><span class="sxs-lookup"><span data-stu-id="c1f13-116">You can also add custom device properties other than Icons, Label, and DeviceHandlers under the device group's key and then apply them to all devices that belong to that device group.</span></span>

> [!Note]  
> <span data-ttu-id="c1f13-117">Eigenschaften, die auf der Geräte Instanzebene definiert werden, haben Vorrang vor den auf Gerätegruppen Ebene definierten Eigenschaften, die wiederum Vorrang vor den Eigenschaften haben, die auf Geräteklassen Ebene definiert sind.</span><span class="sxs-lookup"><span data-stu-id="c1f13-117">Properties that are defined at the device instance level take precedence over properties defined at the device group level, which in turn take precedence over properties defined at the device class level.</span></span>

 

 

 



