---
title: NONREDIST
description: Fügt der Liste der Dateien Namen hinzu, die nicht exportiert werden sollen, wenn com+-Anwendungen zur Installation auf anderen Computern verpackt werden. Beachten Sie, dass dies ein Unterschlüssel und kein Wert ist.
ms.assetid: c50e20e4-1a25-4978-ab84-8f7b4b2f6069
keywords:
- Nicht Redist-Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d537208ecaf98cec46591966e4ae7d9c205850a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037653"
---
# <a name="nonredist"></a>NONREDIST

Fügt der Liste der Dateien Namen hinzu, die nicht exportiert werden sollen, wenn com+-Anwendungen zur Installation auf anderen Computern verpackt werden. Beachten Sie, dass dies ein Unterschlüssel und kein Wert ist.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   NONREDIST
      name1
      name2
```

## <a name="remarks"></a>Bemerkungen

Die Dateien, die Sie der Liste hinzufügen, werden durch die Name-Wert-Paare dargestellt, die unter diesem Schlüssel gespeichert sind. In jedem Name-Wert-Paar ist der Name der Dateiname, und der Wert ist reserviert.

 

 




