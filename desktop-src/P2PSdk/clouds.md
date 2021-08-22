---
description: Clouds werden von den Peergruppen- und Graphinfrastrukturen verwendet.
ms.assetid: 01327211-0461-4922-925e-67bebe3e6158
title: Clouds
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c5ecbeee1f5b69d120c5f351f8a5bb200b6e3e5f60e4bacca5a4f5484f402dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932692"
---
# <a name="clouds"></a>Clouds

Clouds werden von den [Peergruppen- und](grouping-api.md) [Graphinfrastrukturen](graphing-api.md) verwendet. Das [Peer Name Resolution Protocol (PNRP)](pnrp-namespace-provider-api.md) identifiziert eine Cloud als eine Gruppe von Peers, die innerhalb desselben IPv6-Bereichs kommunizieren können. Clouds sind eng mit den IPv6-Geltungsbereichen verknüpft. In der folgenden Liste sind einige der einzigartigen Cloudfeatures aufgeführt:

-   Eine Cloud wird anhand eines Namens identifiziert, und verfügbare Clouds können mithilfe von [**WSALookupServiceBegin aufzählt werden.**](pnrp-and-wsalookupservicebegin.md)
-   Wenn ein Computer mit dem Internet verbunden ist, ist er Teil einer globalen Cloud, die durch die Zeichenfolge "Global" identifiziert \_ wird.
-   Wenn ein Computer mit mindestens einem LAN (Local Area Networks) verbunden ist, sind für jeden Link einzelne Clouds verfügbar.
-   Ein Computer kann mit vielen Netzwerken verbunden werden, indem mehrere Netzwerkadapter oder ein virtuelles privates Netzwerk (VPN) verwendet werden. Dies bedeutet, dass ein Computer mit einer Schnittstelle in vielen Clouds sichtbar sein kann.
-   Sie können PNRP verwenden, um Peernamen in einer bestimmten Cloud zu registrieren und aufzulösen.

 

 



