---
description: Callcenter-Steuerelemente erweitern das TAPI 3-Objektmodell, um die Anforderungen von ACD-Systemen (Automatic calldistribution) zu unterstützen.
ms.assetid: cb7a4231-6249-4ab9-9de7-243768a18775
title: Verwenden von callcentersteuerelementen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdc01cac4b068c5ec17ff5794e2e7ffff46dbf95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357422"
---
# <a name="using-call-center-controls"></a>Verwenden von callcentersteuerelementen

Callcenter-Steuerelemente erweitern das TAPI 3-Objektmodell, um die Anforderungen von ACD-Systemen (Automatic calldistribution) zu unterstützen. Ein Callcenter ist ein Ort, an dem Agents oder Operatoren an Telefon Telefonen entweder ausgehende Telefonanrufe tätigen oder eingehende Anrufe tätigen. Beispielsweise verwendet eine Bank oder ein Kreditkartenunternehmen ein Callcenter, um Konto Anfragen zu verarbeiten.

Callcenteranwendungen sind in drei grundlegende Typen unterteilt:

-   [ACD-Proxy](acd-proxy.md): verarbeitet eingehende oder ausgehende Sitzungen auf dem Server, die von einem proprietären Telefon Switch zu einem Internet Gateway verwendet werden können.
-   [ACD-Agent-Client](acd-agent-client.md): dient zum Bereitstellen eines einzelnen Agents, der einen einzelnen Agent empfängt oder aufruft.
-   ACD Supervisor Client: bietet eine allgemeine Ansicht der Agent-und ACD-Vorgänge.

> [!Note]  
> Für Windows 2000 ist die Proxy Funktionalität mithilfe von TAPI 2,2 verfügbar, und Supervisor-Funktionen sind nicht implementiert.

 

Der Abschnitt "Beispiele" der Windows SDK enthält ACD-Codebeispiele unter netds \\ TAPI \\ Tapi2 \\ ACD und netds \\ TAPI \\ Tapi3 \\ ACD.

 

 



