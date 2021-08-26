---
title: RAS-Schnittstellen
description: Eine Schnittstelle stellt ein Netzwerk dar, das über einen LAN- oder WAN-Adapter erreicht werden kann.
ms.assetid: 26eec1af-43b4-4719-bec9-bc3f9b0341e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef716e0db05fe37a0a7d326fbf5f8da878a0628d1deec9e996fcc49d917cc051
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030140"
---
# <a name="ras-interfaces"></a>RAS-Schnittstellen

Eine Schnittstelle stellt ein Netzwerk dar, das über einen LAN- oder WAN-Adapter erreicht werden kann. Jede Schnittstelle verfügt über einen eindeutigen Bezeichner auf dem Router. Schnittstellen, die aktiv sind, verfügen über einen Adapter, der Konnektivität mit dem Netzwerk bietet, das sie darstellen. Schnittstellen, die inaktiv sind, verfügen nicht über einen Adapter, der Konnektivität bietet, es sei denn, ein Administrator hat die Schnittstelle deaktiviert, nachdem sie bereits über einen Adapter verfügen.

Das Weiterleiten eines Pakets an ein Netzwerk, das durch eine Schnittstelle dargestellt wird, verursacht, dass der Router einen Adapter für diese Schnittstelle zuteilen und eine WAN-Verbindung mit dem Remotenetzwerk herstellen kann. Das Zuordnen eines Adapters zu einer Schnittstelle wird als Bindung *bezeichnet.*

Schnittstellen sind verwaltbare Objekte. Jede Schnittstelle wird als Zeile in der Schnittstellentabelle des entsprechenden SNMP-MIB angezeigt.