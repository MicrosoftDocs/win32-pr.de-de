---
title: Aktualisieren von Routen mithilfe von rtmaddroutededest
description: Wenn der Client beim Hinzufügen einer Route keine Effizienz benötigt, sollte er die folgenden Methoden zum Aktualisieren von Routen verwenden.
ms.assetid: bfa914ea-5d54-4ce9-a97c-903c497d135b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99c7972b2d5ec0996cafc1dd32a8a4056a6aeb0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947995"
---
# <a name="updating-routes-using-rtmaddroutetodest"></a>Aktualisieren von Routen mithilfe von rtmaddroutededest

Wenn der Client beim Hinzufügen einer Route keine Effizienz benötigt, sollte er die folgenden Methoden zum Aktualisieren von Routen verwenden. Diese Methode ist weniger effizient, da Sie das Abrufen eines Handles für die Route und das übergeben der [**RTM- \_ Routen \_ Informations**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) Struktur an den Routing Tabellen-Manager erfordert. Diese Methode benötigt auch mehr Zeit. Da [**rtmaddroutededest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) die Routing Tabelle nicht direkt bearbeitet, funktioniert die Verwendung dieser Methode zur Vereinfachung.

Beispielcode, der die Verwendung dieser Funktionen veranschaulicht, finden [Sie unter Hinzufügen und Aktualisieren von Routen mithilfe von rtmaddroutededest](add-and-update-routes-using-rtmaddroutetodest.md).

 

 




