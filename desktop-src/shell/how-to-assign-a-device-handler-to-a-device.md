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
# <a name="how-to-assign-a-device-handler-to-a-device"></a>Zuweisen eines Geräte Handlers zu einem Gerät

Veranschaulicht den Prozess zum Hinzufügen eines Geräte Handlers zu einem Gerät.

## <a name="instructions"></a>Instructions


Fügen Sie zum Zuweisen eines Geräte Handlers zu einem Gerät unter dem Unterschlüssel **Geräteparameter** der Geräte Instanz einen Wert vom Typ **reg \_ SZ** namens **devicehandlers** hinzu. Der Dateneintrag für diesen Wert ist der Name des Geräte Handlers.

Im folgenden finden Sie einen Beispiel Eintrag für ein fiktives vid \_ 059&PID-Wert- \_ Gerät.

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

Geräte Handler können auch mithilfe von [Gerätegruppen](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-group.md) -oder [Geräteklassen](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-class.md) Einstellungen zugewiesen werden.

 

 



