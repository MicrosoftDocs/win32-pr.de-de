---
description: Netzwerkpaketanbieter (Network Packet Providers, NPPs) sind Netzwerkmonitor Systemkomponenten, die Netzwerkdatenverkehr (Frames) aus dem Netzwerk erfassen und an die Netzwerkmonitor-Benutzeroberfläche und NPP-Anwendungen übergeben.
ms.assetid: c966cd00-5cab-4fcf-ad8e-b6c4ffb0e977
title: Netzwerkpaketanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c580610224a5d6cb3f461b1c039862e49b29358c4952549cefefe3c7434aa084
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799535"
---
# <a name="network-packet-providers"></a>Netzwerkpaketanbieter

Netzwerkpaketanbieter (Network Packet Providers, NPPs) sind Netzwerkmonitor Systemkomponenten, die Netzwerkdatenverkehr (Frames) aus dem Netzwerk erfassen und an die Netzwerkmonitor-Benutzeroberfläche und [*NPP-Anwendungen*](n.md)übergeben.

Die folgende Abbildung zeigt zwei NPPs: das von Netzwerkmonitor bereitgestellte NDIS-NPP und ein benutzerdefiniertes NPP.

![Vom Netzwerkmonitor bereitgestellte ndis npp und ein benutzerdefiniertes npp](images/npp.png)

Das von Netzwerkmonitor bereitgestellte NDIS-NPP ist Ndisnpp.dll. Dieses NPP verwendet den Netzwerkmonitor Systemtreiber (Nmnt.sys), um die vom Netzwerk gesammelten Frames und mehrere COM-Schnittstellen (als NPP-Schnittstellen bezeichnet) abzurufen, um die Frames an die Netzwerkmonitor-Benutzeroberfläche und NPP-Anwendungen zu übergeben, wo sie angezeigt und analysiert werden können.

Ndisnpp.dll stellt eine Verbindung mit der [*NDIS-Schicht*](n.md) her, um den Netzwerkdatenverkehr zu erhalten. (Benutzerdefinierte NPPs können die NDIS-Ebene umgehen und direkt mit der Netzwerkhardware kommunizieren.) Beachten Sie, dass NPPs unabhängig davon, ob ein NPP NDIS verwendet, eine Verbindung mit einer beliebigen Anzahl von Netzwerkkarten herstellen können und dass alle NPPs die gleichen NPP-Schnittstellen unterstützen müssen.

Bevor eine Anwendung mit der Erfassung von Daten beginnen kann, muss Sie:

-   Wählen Sie die Netzwerkschnittstellenkarte (Network Interface Card, NIC) aus, die das NPP mit dem Netzwerk verbindet.
-   Wählen Sie die NPP-Schnittstelle aus, die zum Erfassen der Netzwerkframes verwendet wird.
-   Verwenden Sie die ausgewählte Schnittstelle, um eine Verbindung mit der NIC herzustellen.

Weitere Informationen zum Aufzählen und Auswählen einer Netzwerkschnittstellenkarte finden Sie unter [Auswählen einer Netzwerkschnittstellenkarte.](selecting-a-network-interface-card.md)

Weitere Informationen zu COM-Schnittstellen, die von NPPs verfügbar gemacht werden, finden Sie unter [Auswählen einer NPP-Schnittstelle.](selecting-an-npp-interface.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IDelaydC**](idelaydc.md)
</dt> <dt>

[**IESP**](iesp.md)
</dt> <dt>

[**IRTC**](irtc.md)
</dt> <dt>

[**IStats**](istats.md)
</dt> </dl>

 

 



