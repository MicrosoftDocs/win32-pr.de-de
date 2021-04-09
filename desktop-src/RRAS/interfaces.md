---
title: RAS-Schnittstellen
description: Eine Schnittstelle stellt ein Netzwerk dar, das über ein LAN oder einen WAN-Adapter erreicht werden kann.
ms.assetid: 26eec1af-43b4-4719-bec9-bc3f9b0341e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dea285a625377709a4eca3bc8b9947106c2f5cfd
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "103857835"
---
# <a name="ras-interfaces"></a>RAS-Schnittstellen

Eine Schnittstelle stellt ein Netzwerk dar, das über ein LAN oder einen WAN-Adapter erreicht werden kann. Jede Schnittstelle verfügt über einen eindeutigen Bezeichner auf dem Router. Aktive Schnittstellen verfügen über einen Adapter, der Konnektivität mit dem Netzwerk bereitstellt, das Sie darstellen. Inaktive Schnittstellen verfügen über keinen Adapter, der Konnektivität bereitstellt, es sei denn, ein Administrator hat die Schnittstelle deaktiviert, nachdem Sie bereits einen Adapter besaß.

Das Routing eines Pakets an ein Netzwerk, das durch eine Schnittstelle dargestellt wird, weist den Router an, einen Adapter für diese Schnittstelle zuzuweisen und eine WAN-Verbindung mit dem Remote Netzwerk herzustellen. Das Zuordnen eines Adapters zu einer Schnittstelle wird als *Bindung* bezeichnet.

Schnittstellen sind verwaltbare Objekte. Jede Schnittstelle wird als Zeile in der Schnittstellen Tabelle der entsprechenden SNMP-MIB angezeigt.