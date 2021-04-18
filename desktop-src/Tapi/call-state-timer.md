---
description: Derzeit werden alle Aufrufe von-Aufrufen an Anwendungen übergegangen.
ms.assetid: 9eb98b48-4bee-4f6d-b818-2f81b36591da
title: Timer für den CallState
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5d273d7f8439ebfee9d6668565745ed2c209f70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357386"
---
# <a name="call-state-timer"></a>Timer für den CallState

Derzeit werden alle Aufrufe von-Aufrufen an Anwendungen übergegangen. Dies kann sehr aufwändiger sein, wenn die Anwendung eine große Anzahl von Aufrufen überwacht, und wenn mehrere Anwendungen vorhanden sind, möglicherweise auf mehreren Servern, kann es erforderlich sein, dass alle Timer bei denselben aufrufen gewartet werden. Daher ist es sinnvoller, die zeitliche Steuerung des Ansichts Zustands vom Server zu verarbeiten.

Das **tstateentrytime** -Element in [**linecallstatus**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) ermöglicht die zeitliche Steuerung von Aufrufen in Zuständen, die gemeldet werden sollen. Der Member (des Typs **SysTime**) gibt den Zeitpunkt an, zu dem der aktuelle Status eingegeben wurde.

 

 



