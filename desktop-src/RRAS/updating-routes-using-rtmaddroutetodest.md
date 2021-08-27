---
title: Aktualisieren von Routen mit rtmAddRouteToDest
description: Wenn der Client beim Hinzufügen einer Route keine Effizienz erfordert, sollte er die folgende Methode zum Aktualisieren von Routen verwenden.
ms.assetid: bfa914ea-5d54-4ce9-a97c-903c497d135b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb3212a74637fa4de51f3b05f80f84bace1c0c57ba570e5025adb796da933b24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025330"
---
# <a name="updating-routes-using-rtmaddroutetodest"></a>Aktualisieren von Routen mit rtmAddRouteToDest

Wenn der Client beim Hinzufügen einer Route keine Effizienz erfordert, sollte er die folgende Methode zum Aktualisieren von Routen verwenden. Diese Methode ist weniger effizient, da sie erfordert, ein Handle für die Route zu erhalten und die [**RTM \_ ROUTE \_ INFO-Struktur**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) an und vom Routingtabellen-Manager zu übergeben. Diese Methode dauert auch mehr Zeit. Da [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) die Routingtabelle nicht direkt bearbeitet, wird die Effizienz mit dieser Methode der Einfachheit halber geeint.

Beispielcode, der die Verwendung dieser Funktionen veranschaulicht, finden Sie unter Hinzufügen und Aktualisieren von Routen [mit rtmAddRouteToDest.](add-and-update-routes-using-rtmaddroutetodest.md)

 

 




