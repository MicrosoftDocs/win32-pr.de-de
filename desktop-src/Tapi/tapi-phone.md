---
description: Die Geräteklasse tapi/phone besteht aus allen Telefongeräten. Sie greifen auf diese Geräte mithilfe der TAPI-Telefonfunktionen zu.
ms.assetid: c2e52fdf-e07a-4897-8af5-0a101d6c237a
title: tapi/phone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96b3238fb2e83d4f6e5e565f40b3ab3b124236ae2c89f879cb284d4a5997f662
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002718"
---
# <a name="tapiphone"></a>tapi/phone

Die Geräteklasse tapi/phone besteht aus allen Telefongeräten. Sie greifen auf diese Geräte mithilfe der TAPI-Telefonfunktionen zu.

Die [**phoneGetID-Funktion**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) füllt eine [**VARSTRING-Struktur**](/windows/desktop/api/Tapi/ns-tapi-varstring) auf, setzt den **dwStringFormat-Member** auf den STRINGFORMAT BINARY-Wert und fügt diesen \_ zusätzlichen Member an:

``` syntax
DWORD dwDeviceI;  // phone device identifier
```

Das **dwDeviceId-Mitglied** ist der Bezeichner des Telefongeräts, das dem von phoneGetID angegebenen [**Telefonhandle zugeordnet ist.**](/windows/desktop/api/Tapi/nf-tapi-phonegetid)

Die [**lineGetID-Funktion**](/windows/desktop/api/Tapi/nf-tapi-linegetid) füllt auch eine [**VARSTRING-Struktur**](/windows/desktop/api/Tapi/ns-tapi-varstring) auf, indem **dwStringFormat** auf STRINGFORMAT BINARY und dieses \_ zusätzliche Member angefügt wird:

``` syntax
DWORD adwDeviceIds[];  // array of phone device identifiers
```

Das **AdwDeviceIds-Member** ist ein Array, das die Gerätebezeichner aller Telefongeräte enthält, die dem angegebenen Zeilengerät zugeordnet sind. Wenn keine zugeordneten Telefongeräte verfügbar sind, [**gibt lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) den LINEERR \_ INVALDEVICECLASS-Wert zurück.

 

 



