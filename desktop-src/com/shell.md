---
title: Shell (com)
description: Bietet Informationen zum Drucken von Windows 3,1-Shell und zum Öffnen von Dateien.
ms.assetid: 15e329f2-ed64-4940-aa00-63edbd283b07
keywords:
- Shell-Registrierungsschlüssel com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1acf4a62d72892d1cd25a5f2276e71d52ab7f700
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739345"
---
# <a name="shell-com"></a>Shell (com)

Bietet Informationen zum Drucken von Windows 3,1-Shell und zum **Öffnen von Dateien** .

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   {ProgID}
      Shell
         Open
            command = path %1
         Print
            command = path %1
```

## <a name="remarks"></a>Bemerkungen

Diese Einträge sollten den Pfad und den Dateinamen der Anwendung angeben.

 

 




