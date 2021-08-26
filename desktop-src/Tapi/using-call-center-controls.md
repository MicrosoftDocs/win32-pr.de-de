---
description: Callcentersteuerungen erweitern das TAPI 3-Objektmodell, um die Anforderungen von ACD-Systemen (Automatic Call Distribution) zu unterstützen.
ms.assetid: cb7a4231-6249-4ab9-9de7-243768a18775
title: Verwenden von Callcenter-Steuerelementen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04f166658cce86faa0003b762ec697286a434a06b36b18ae92a861d1f6757fa6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991540"
---
# <a name="using-call-center-controls"></a>Verwenden von Callcenter-Steuerelementen

Callcentersteuerungen erweitern das TAPI 3-Objektmodell, um die Anforderungen von ACD-Systemen (Automatic Call Distribution) zu unterstützen. Ein Callcenter ist ein Standort mit Agenten oder Betreibern an Telefone, die entweder ausgehende Telefonanrufe tätigen oder eingehende Telefonanrufe tätigen. Beispielsweise verwendet ein Bank- oder Kreditkartenunternehmen ein Callcenter, um Kontoanfragen zu verarbeiten.

Callcenteranwendungen sind in drei grundlegende Typen unterteilt:

-   [ACD-Proxy:](acd-proxy.md)Verarbeitet eingehende oder ausgehende Sitzungen auf dem Server, die von einem proprietären Telefonschalter bis hin zu einem Internetgateway alles sein können.
-   [ACD-Agent-Client:](acd-agent-client.md)Wartet einen einzelnen Agent, der Aufrufe empfängt oder aufruft.
-   ACD Supervisor-Client: Bietet eine allgemeine Ansicht der Agent- und ACD-Vorgänge.

> [!Note]  
> Für Windows 2000 ist die Proxyfunktionalität mit TAPI 2.2 verfügbar, und Supervisorfunktionen werden nicht implementiert.

 

Der Abschnitt samples des Windows SDK enthält ACD-Codebeispiele unter Netds \\ Tapi \\ Tapi2 \\ Acd und Netds \\ Tapi \\ Tapi3 \\ Acd.

 

 



