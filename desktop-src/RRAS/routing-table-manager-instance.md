---
title: Routingtabellen-Manager-Instanz
description: Eine -Instanz ist eine separate Tabelle, die der Routingtabellen-Manager verwendet, um Routinginformationen zu einer Teilmenge von Schnittstellen zu verwalten.
ms.assetid: a17233fc-2c40-4d00-8a6b-86f08fef5690
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3215baf7a3cf093ecf47e8cf9965a71e75dea17a0527949e68b2c5f929d336ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073920"
---
# <a name="routing-table-manager-instance"></a>Routingtabellen-Manager-Instanz

Eine -Instanz ist eine separate Tabelle, die der Routingtabellen-Manager verwendet, um Routinginformationen zu einer Teilmenge von Schnittstellen zu verwalten. Instanzen werden in der Regel verwendet, damit ein physischer Router als Gruppe von virtuellen Routern fungieren kann – ein virtueller Router pro logischem Netzwerk.

Derzeit unterstützt der Routingtabellen-Manager nur eine -Instanz (als 0 (null, Standardeinstellung) identifiziert). Der Client kann sich bei anderen Instanzen registrieren, aber kein virtueller Router außer dem Standardrouter wird vom Router-Manager erkannt oder verwendet.

 

 




