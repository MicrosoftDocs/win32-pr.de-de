---
description: Veranschaulicht den Prozess zum Hinzufügen eines Geräte Handlers zu einem Gerät.
title: Zuweisen eines Geräte Handlers zu einem Gerät
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16db6a39406e3d8ba7cd8b497e12883685b80d93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979616"
---
# <a name="how-to-assign-a-device-handler-to-a-device"></a><span data-ttu-id="b762c-103">Zuweisen eines Geräte Handlers zu einem Gerät</span><span class="sxs-lookup"><span data-stu-id="b762c-103">How to Assign a Device Handler to a Device</span></span>

<span data-ttu-id="b762c-104">Veranschaulicht den Prozess zum Hinzufügen eines Geräte Handlers zu einem Gerät.</span><span class="sxs-lookup"><span data-stu-id="b762c-104">Illustrates the process for adding a device handler to a device.</span></span>

## <a name="instructions"></a><span data-ttu-id="b762c-105">Instructions</span><span class="sxs-lookup"><span data-stu-id="b762c-105">Instructions</span></span>


<span data-ttu-id="b762c-106">Fügen Sie zum Zuweisen eines Geräte Handlers zu einem Gerät unter dem Unterschlüssel **Geräteparameter** der Geräte Instanz einen Wert vom Typ **reg \_ SZ** namens **devicehandlers** hinzu.</span><span class="sxs-lookup"><span data-stu-id="b762c-106">To assign a device handler to a device, under the **Device Parameters** subkey of the device instance, add a value of type **REG\_SZ** named **DeviceHandlers**.</span></span> <span data-ttu-id="b762c-107">Der Dateneintrag für diesen Wert ist der Name des Geräte Handlers.</span><span class="sxs-lookup"><span data-stu-id="b762c-107">The data entry for this value is the name of the device handler.</span></span>

<span data-ttu-id="b762c-108">Im folgenden finden Sie einen Beispiel Eintrag für ein fiktives vid \_ 059&PID-Wert- \_ Gerät.</span><span class="sxs-lookup"><span data-stu-id="b762c-108">The following is an example entry for a fictitious Vid\_059&Pid\_0031 device.</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Enum
            USB
               Vid_059b&Pid_0031
                  059B003112010E93
                     Device Parameters
                        DeviceHandlers = MyDeviceHandler
```

<span data-ttu-id="b762c-109">Geräte Handler können auch mithilfe von [Gerätegruppen](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-group.md) -oder [Geräteklassen](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-class.md) Einstellungen zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="b762c-109">Device handlers can also be assigned by using [device group](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-group.md) or [device class](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-class.md) settings.</span></span>

 

 



