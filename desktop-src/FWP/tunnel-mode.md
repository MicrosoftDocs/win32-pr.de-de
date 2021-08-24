---
title: Tunnel Modus
description: Das Tunnel IPsec-Richtlinienszenario im IPsec-Modus wird verwendet, um den IPsec-Tunnelmodusschutz für den abgleichenden Datenverkehr zwischen zwei Tunnelendpunkten anzuwenden.
ms.assetid: 170046c5-28ec-4341-89e2-93494bf9c6b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbac16de0dc01bc37e0e4f4b997d00d19339de021ffce66a0d3cf6957addbe90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639070"
---
# <a name="tunnel-mode"></a>Tunnel Modus

Das Tunnel IPsec-Richtlinienszenario im IPsec-Modus wird verwendet, um den IPsec-Tunnelmodusschutz für den abgleichenden Datenverkehr zwischen zwei Tunnelendpunkten anzuwenden.

Dieses Richtlinienszenario wird in der Regel zum Schutz des Datenverkehrs zwischen mehreren Subnetzen der Filiale verwendet, wenn er zwischen den entsprechenden Gateways im Internet weitergeleitet wird. Sie kann auch verwendet werden, um die End-to-End-Kommunikation zwischen zwei Hostcomputern zu schützen, die auch als Punkt-zu-Punkt-Tunnel bezeichnet werden.

Um die Tunnel Mode-Richtlinie mithilfe der Windows Filtering Platform (WFP) zu implementieren, rufen Sie die [**FwpmIPsecTunnelAdd0-Funktion**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) auf, die die entsprechenden Tunnelmodusfilter auf den entsprechenden Ebenen im Namen des Aufrufers instanziiert. Der Aufrufer muss den Hauptmodus, die Anbieterkontexte im Schnellmodus und die Filterbedingungen angeben, die den Datenverkehr beschreiben, der innerhalb des Tunnels geschützt werden soll.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beispielcode: Verwenden des Tunnel Modus](using-tunnel-mode.md)
</dt> <dt>

[**Filtern von Ebenenbezeichnern**](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




