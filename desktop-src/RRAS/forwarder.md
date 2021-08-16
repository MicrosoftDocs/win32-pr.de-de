---
title: Weiterleitung
description: Die Weiterleitung ist die Kernelmoduskomponente des Routers, die für die Weiterleitung von Daten von einer Routerschnittstelle an die anderen zuständig ist.
ms.assetid: 69cdbefa-9137-48cb-940a-badfb3f4f231
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5011d340b444c9d0be5b26ee5449f041bb7419fd4a52f8a983ce2b85d9b106f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674020"
---
# <a name="forwarder"></a>Weiterleitung

Die Weiterleitung ist die Kernelmoduskomponente des Routers, die für die Weiterleitung von Daten von einer Routerschnittstelle an die anderen zuständig ist. Die Weiterleitung entscheidet auch, ob ein Paket für die lokale Übermittlung bestimmt ist, ob es von einer anderen Schnittstelle weitergeleitet werden soll oder beides.

Es gibt zwei Kernelmodus-Weiterleitungen: Unicast und Multicast.

Der Router-Manager ruft die besten Routen zu allen Zielen vom Routingtabellen-Manager ab. Diese Routen werden an die Unicast-Weiterleitung übergeben. Die Unicastweiterleitung verwendet diese Routen, um die tatsächliche Weiterleitung von Unicastdaten durchzuführen. Auf diese Weise verwaltet die Unicastweiterleitung einen Cache der besten Routen in der Unicastansicht der Routingtabelle.

Der Multicastgruppen-Manager verwendet Informationen aus der Multicastansicht der Routingtabelle, um der Multicastweiterleitung Multicastweiterleitungseinträge hinzuzufügen.

 

 




