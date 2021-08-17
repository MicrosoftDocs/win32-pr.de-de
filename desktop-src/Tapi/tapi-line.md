---
description: Die Geräteklasse tapi/line besteht aus allen Liniengeräten. Sie greifen mithilfe der TAPI-Linienfunktionen auf diese Geräte zu.
ms.assetid: 2215b10b-e410-462c-8cf9-42f3e688e82e
title: tapi/line
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c56478f43d1055d7bf2a382bc84611360675da97e506812a1806df4beca0aeff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760732"
---
# <a name="tapiline"></a>tapi/line

Die Geräteklasse tapi/line besteht aus allen Liniengeräten. Sie greifen mithilfe der TAPI-Linienfunktionen auf diese Geräte zu.

Die [**lineGetID-Funktion**](/windows/desktop/api/Tapi/nf-tapi-linegetid) füllt eine [**VARSTRING-Struktur**](/windows/desktop/api/Tapi/ns-tapi-varstring) auf, setzt den **dwStringFormat-Member** auf den STRINGFORMAT BINARY-Wert und fügt \_ diesen zusätzlichen Member an.

``` syntax
DWORD dwDeviceI;  // line device identifier
```

Das **dwDeviceId-Member** ist der Bezeichner des Liniengeräts, das dem von lineGetID angegebenen [**Zeilenhandle zugeordnet ist.**](/windows/desktop/api/Tapi/nf-tapi-linegetid)

Die [**phoneGetID-Funktion**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) füllt auch eine [**VARSTRING-Struktur**](/windows/desktop/api/Tapi/ns-tapi-varstring) auf, setzt **dwStringFormat** auf STRINGFORMAT BINARY und fügt \_ diesen zusätzlichen Member an:

``` syntax
DWORD adwDeviceIds[];  // array of line device identifiers
```

Das **adwDeviceIds-Member** ist ein Array, das die Gerätebezeichner aller Gerätezeilen enthält, die dem Telefongerät zugeordnet sind. Wenn keine zugeordneten Zeilengeräte verfügbar sind, [**gibt phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) den Wert PHONEERR \_ INVALDEVICECLASS zurück.

 

 



