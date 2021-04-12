---
description: Die TAPI/Phone-Geräteklasse besteht aus allen Telefongeräten. Sie greifen auf diese Geräte mithilfe der TAPI-Telefonfunktionen zu.
ms.assetid: c2e52fdf-e07a-4897-8af5-0a101d6c237a
title: TAPI/Telefon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c704a6999982fb0c23a8b02439a3d0e61b3af8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960230"
---
# <a name="tapiphone"></a>TAPI/Telefon

Die TAPI/Phone-Geräteklasse besteht aus allen Telefongeräten. Sie greifen auf diese Geräte mithilfe der TAPI-Telefonfunktionen zu.

Die [**phonegetid**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) -Funktion füllt eine [**varstring**](/windows/desktop/api/Tapi/ns-tapi-varstring) -Struktur aus, legt den **dwstringformat** -Member auf den "StringFormat" \_ -Binärwert fest und fügt diesen zusätzlichen Member an:

``` syntax
DWORD dwDeviceI;  // phone device identifier
```

Der **dwenviceid** -Member ist der Bezeichner des Telefon Geräts, das dem durch [**phonegetid**](/windows/desktop/api/Tapi/nf-tapi-phonegetid)angegebenen Telefon Handle zugeordnet ist.

Die [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) -Funktion füllt auch eine [**varstring**](/windows/desktop/api/Tapi/ns-tapi-varstring) -Struktur, wobei **dwstringformat** auf die Binärdatei StringFormat festgelegt \_ und dieses zusätzliche Mitglied angehängt wird:

``` syntax
DWORD adwDeviceIds[];  // array of phone device identifiers
```

Der **adwenviceids** -Member ist ein Array mit den Geräte bezeichdern aller Telefongeräte, die mit dem angegebenen liniengerät verknüpft sind. Wenn keine zugeordneten Telefongeräte vorhanden sind, gibt [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) den lineerr- \_ Wert "invalendviceclass" zurück.

 

 



