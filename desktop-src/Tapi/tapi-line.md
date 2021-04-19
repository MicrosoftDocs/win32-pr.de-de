---
description: Die TAPI/Line-Geräteklasse besteht aus allen Linien Geräten. Sie greifen auf diese Geräte mithilfe der TAPI-Linienfunktionen zu.
ms.assetid: 2215b10b-e410-462c-8cf9-42f3e688e82e
title: TAPI/Linie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 928cfa6144e9a701d6462519d2aa9d590a54a511
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373218"
---
# <a name="tapiline"></a>TAPI/Linie

Die TAPI/Line-Geräteklasse besteht aus allen Linien Geräten. Sie greifen auf diese Geräte mithilfe der TAPI-Linienfunktionen zu.

Die [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) -Funktion füllt eine [**varstring**](/windows/desktop/api/Tapi/ns-tapi-varstring) -Struktur aus, legt den **dwstringformat** -Member auf den "StringFormat" \_ -Binärwert fest und fügt diesen zusätzlichen Member an.

``` syntax
DWORD dwDeviceI;  // line device identifier
```

Der **dwenviceid** -Member ist der Bezeichner des Linien Geräts, das dem von [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid)angegebenen Zeilen Handle zugeordnet ist.

Die [**phonegetid**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) -Funktion füllt auch eine [**varstring**](/windows/desktop/api/Tapi/ns-tapi-varstring) -Struktur, wobei **dwstringformat** auf die Binärdatei StringFormat festgelegt \_ und dieses zusätzliche Mitglied angehängt wird:

``` syntax
DWORD adwDeviceIds[];  // array of line device identifiers
```

Der **adwenviceids** -Member ist ein Array, das die Geräte Bezeichner aller Linien Geräte enthält, die dem Telefongerät zugeordnet sind. Wenn keine zugeordneten Zeilen Geräte vorhanden sind, gibt [**phonegetid**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) den Wert phoneerr \_ invalendviceclass zurück.

 

 



