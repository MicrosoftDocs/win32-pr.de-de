---
title: Tunnel Modus
description: Im Tunnel Modus-IPSec-Richtlinien Szenario wird der IPSec-tunnelmodusschutz für den gesamten übereinstimmenden Datenverkehr zwischen zwei Tunnel Endpunkten angewendet.
ms.assetid: 170046c5-28ec-4341-89e2-93494bf9c6b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75fdecb7f959a2f95aae2649a6e3f8f94def9b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310692"
---
# <a name="tunnel-mode"></a>Tunnel Modus

Im Tunnel Modus-IPSec-Richtlinien Szenario wird der IPSec-tunnelmodusschutz für den gesamten übereinstimmenden Datenverkehr zwischen zwei Tunnel Endpunkten angewendet.

Dieses Richtlinien Szenario wird normalerweise verwendet, um den Datenverkehr zwischen mehreren Zweigstellen Subnetzen zu schützen, wenn dieser zwischen den entsprechenden Gateways im Internet weitergeleitet wird. Sie kann auch verwendet werden, um die End-to-End-Kommunikation zwischen zwei Host Computern zu sichern, auch als Punkt-zu-Punkt-Tunnel bezeichnet.

Um eine tunnelmodusrichtlinie mithilfe der Windows-Filter Plattform (WFP) zu implementieren, nennen Sie die [**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) -Funktion, die die entsprechenden Tunnel Modusfilter auf den entsprechenden Ebenen im Namen des Aufrufers instanziiert. Der Aufrufer muss den Hauptmodus, den Schnellmodus-Anbieter Kontext und die Filterbedingungen angeben, die den Datenverkehr beschreiben, der innerhalb des Tunnels gesichert werden soll.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beispielcode: Verwenden des Tunnel Modus](using-tunnel-mode.md)
</dt> <dt>

[**Filtern von ebenenbezeichgern**](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




