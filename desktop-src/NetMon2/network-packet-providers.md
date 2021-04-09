---
description: Netzwerk Paketanbieter (NPPs) sind Netzwerkmonitor Systemkomponenten, die Netzwerk Datenverkehr (Frames) aus dem Netzwerk erfassen und an die Netzwerkmonitor-Benutzeroberfläche und NPP-Anwendungen weiterleiten.
ms.assetid: c966cd00-5cab-4fcf-ad8e-b6c4ffb0e977
title: Netzwerk Paketanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8257a62e4f8b0a8434143b2fecba04d9a66c9fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868824"
---
# <a name="network-packet-providers"></a>Netzwerk Paketanbieter

Netzwerk Paketanbieter (NPPs) sind Netzwerkmonitor Systemkomponenten, die Netzwerk Datenverkehr (Frames) aus dem Netzwerk erfassen und an die Netzwerkmonitor-Benutzeroberfläche und [*NPP-Anwendungen*](n.md)weiterleiten.

Die folgende Abbildung zeigt zwei NPPs: das von Netzwerkmonitor bereitgestellte NDIS NPP und ein benutzerdefiniertes NPP.

![NDIS NPP von Netzwerkmonitor und benutzerdefiniertem NPP bereitgestellt](images/npp.png)

Der von Netzwerkmonitor bereitgestellte NDIS-npp ist Ndisnpp.dll. Dieser NPP verwendet den Netzwerkmonitor System Treiber (Nmnt.sys), um die vom Netzwerk gesammelten Frames und verschiedene COM-Schnittstellen (als NPP-Schnittstellen bezeichnet) zu erhalten, um die Frames an die Netzwerkmonitor-Benutzeroberfläche und NPP-Anwendungen zu übergeben, in denen Sie angezeigt und analysiert werden können.

Ndisnpp.dll stellt eine Verbindung mit der [*NDIS*](n.md) -Schicht her, um den Netzwerk Datenverkehr abzurufen. (Benutzerdefinierte NPPs können die NDIS-Schicht umgehen und direkt mit der Netzwerkhardware kommunizieren.) Beachten Sie, dass NPPs unabhängig davon, ob NPP NDIS verwendet, eine Verbindung mit einer beliebigen Anzahl von Netzwerkkarten herstellen kann und dass alle NPPs die gleichen NPP-Schnittstellen unterstützen müssen.

Bevor eine Anwendung mit dem Erfassen von Daten beginnen kann, müssen Sie folgende Schritte ausführen:

-   Wählen Sie die Netzwerkschnittstellenkarte (NIC) aus, mit der der NPP mit dem Netzwerk verbunden wird.
-   Wählen Sie die NPP-Schnittstelle aus, die zum Erfassen der Netzwerk Rahmen verwendet werden soll.
-   Verwenden Sie die ausgewählte Schnittstelle, um eine Verbindung mit der NIC herzustellen.

Weitere Informationen zum Auflisten und Auswählen einer Netzwerkschnittstellenkarte finden Sie unter [Auswählen einer Netzwerkschnittstellenkarte](selecting-a-network-interface-card.md).

Weitere Informationen zu von NPPs verfügbar gemachten com-Schnittstellen finden Sie unter [Auswählen einer NPP-Schnittstelle](selecting-an-npp-interface.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Idelta-DC**](idelaydc.md)
</dt> <dt>

[**IESP**](iesp.md)
</dt> <dt>

[**"Iran"**](irtc.md)
</dt> <dt>

[**IStats**](istats.md)
</dt> </dl>

 

 



