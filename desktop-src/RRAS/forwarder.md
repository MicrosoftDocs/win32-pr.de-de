---
title: Weiterleitung
description: Bei der Weiterleitung handelt es sich um die Kernelmoduskomponente des Routers, die für die Weiterleitung von Daten von einer Routerschnittstelle an andere zuständig ist.
ms.assetid: 69cdbefa-9137-48cb-940a-badfb3f4f231
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52885000a9f1fcc117cd1fefc207531b9b524e74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037010"
---
# <a name="forwarder"></a>Weiterleitung

Bei der Weiterleitung handelt es sich um die Kernelmoduskomponente des Routers, die für die Weiterleitung von Daten von einer Routerschnittstelle an andere zuständig ist. Die Weiterleitung entscheidet auch, ob ein Paket für die lokale Übermittlung bestimmt ist, ob es für die Weiterleitung aus einer anderen Schnittstelle oder beides bestimmt ist.

Es gibt zwei Weiterleitungen im kernelmodusmodus: Unicast und Multicast.

Der routermanager erhält die besten Routen für alle Ziele aus dem Routing Tabellen-Manager. Diese Routen werden an die Unicastweiterleitung übergeben. Die Unicastweiterleitung verwendet diese Routen, um die tatsächliche Weiterleitung von Unicastdaten auszuführen. Auf diese Weise behält die Unicastweiterleitung einen Cache der besten Routen in der unicastansicht der Routing Tabelle bei.

Der Multicast-Gruppen-Manager verwendet Informationen aus der Multicast Ansicht der Routing Tabelle, um Multicast Weiterleitungs Einträge zur Multicast Weiterleitung hinzuzufügen.

 

 




