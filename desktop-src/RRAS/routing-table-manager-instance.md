---
title: Routing-Tabellen-Manager-Instanz
description: Eine Instanz ist eine separate Tabelle, die der Routing Tabellen-Manager verwendet, um Routing Informationen über eine Teilmenge der Schnittstellen beizubehalten.
ms.assetid: a17233fc-2c40-4d00-8a6b-86f08fef5690
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d209f254bb9111c786bde6635b43895604785d5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036864"
---
# <a name="routing-table-manager-instance"></a>Routing-Tabellen-Manager-Instanz

Eine Instanz ist eine separate Tabelle, die der Routing Tabellen-Manager verwendet, um Routing Informationen über eine Teilmenge der Schnittstellen beizubehalten. Instanzen werden in der Regel verwendet, um einen physischen Router als Satz virtueller Router zu fungieren – einen virtuellen Router pro logischem Netzwerk.

Derzeit unterstützt der Routing Tabellen-Manager nur eine Instanz (als 0 (null), Standardeinstellung). Der Client kann sich bei anderen Instanzen registrieren, aber es wird kein virtueller Router, außer dem Standardwert, erkannt oder vom Router-Manager verwendet.

 

 




