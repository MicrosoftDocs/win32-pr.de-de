---
description: Veranschaulicht den Prozess zum Hinzufügen eines Gerätehandlers zu einem Gerät.
title: Zuweisen eines Gerätehandlers zu einem Gerät
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de091a7206e8fe2d9ea2781e2c5b3475cb71446bae2effa9e017795ced8b9bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092974"
---
# <a name="how-to-assign-a-device-handler-to-a-device"></a>Zuweisen eines Gerätehandlers zu einem Gerät

Veranschaulicht den Prozess zum Hinzufügen eines Gerätehandlers zu einem Gerät.

## <a name="instructions"></a>Anweisungen


Um einem Gerät einen Gerätehandler zuzuweisen, fügen Sie unter dem Unterschlüssel **Geräteparameter** der Geräteinstanz einen Wert vom Typ **REG \_ SZ** mit dem Namen **DeviceHandlers hinzu.** Der Dateneintrag für diesen Wert ist der Name des Gerätehandlers.

Im Folgenden finden Sie einen Beispieleintrag für ein fiktives Vid \_ 059&Pid \_ 0031-Gerät.

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

Gerätehandler können auch mithilfe von [Gerätegruppen-](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-group.md) oder [Geräteklasseneinstellungen](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-class.md) zugewiesen werden.

 

 



