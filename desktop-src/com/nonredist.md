---
title: NONREDIST
description: Fügt der Liste der Dateien Namen hinzu, die nicht exportiert werden sollen, wenn COM+-Anwendungen für die Installation auf anderen Computern gepackt werden. Beachten Sie, dass dies ein Unterschlüssel und kein Wert ist.
ms.assetid: c50e20e4-1a25-4978-ab84-8f7b4b2f6069
keywords:
- NONREDIST-Registrierungswert COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b303c145ea48a51f72d6ee21078b5f29a6b6d4fabc7184d4a37e980a2bbb2e4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678460"
---
# <a name="nonredist"></a>NONREDIST

Fügt der Liste der Dateien Namen hinzu, die nicht exportiert werden sollen, wenn COM+-Anwendungen für die Installation auf anderen Computern gepackt werden. Beachten Sie, dass dies ein Unterschlüssel und kein Wert ist.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   NONREDIST
      name1
      name2
```

## <a name="remarks"></a>Hinweise

Die Dateien, die Sie der Liste hinzufügen, werden durch Name-Wert-Paare dargestellt, die unter diesem Schlüssel gespeichert sind. In jedem Name-Wert-Paar ist der Name der Dateiname, und der Wert ist reserviert.

 

 




