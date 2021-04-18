---
title: Aktivieren der Synchronisierung mit Windows Media Player
description: Aktivieren der Synchronisierung mit Windows Media Player
ms.assetid: a312dfef-ac48-4c58-a59a-b277f5386419
keywords:
- Windows Media Device Manager, Synchronisierung mit Windows Media Player
- Device Manager, Synchronisierung mit Windows Media Player
- Programmier Handbuch, Synchronisierung mit Windows Media Player
- Dienstanbieter, Synchronisierung mit Windows-Media Player
- Erstellen von Dienstanbietern, Synchronisierung mit Windows Media Player
- Synchronisierung mit Windows-Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b621be3b17d42368bc859081f47bc29bb2cfc667
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340658"
---
# <a name="enabling-synchronization-with-windows-media-player"></a>Aktivieren der Synchronisierung mit Windows Media Player

Sie können ein Gerät für die Teilnahme an der automatischen Synchronisierung mit Windows Media Player aktivieren. Automatische Synchronisierung bedeutet Folgendes: Wenn ein Benutzer bestimmtes synchronisiertes Gerät eine Verbindung mit dem Computer herstellt, werden von Windows Media Player automatisch Dateien vom Gerät heruntergeladen, aktualisiert oder gelöscht, ohne dass zusätzliche Benutzereingaben erforderlich sind.

Standardmäßig werden die folgenden Geräte mit Windows Media Player synchronisiert:

-   MTP-Geräte
-   Massenspeichergeräte
-   Windows CE Geräte (Windows Media Player 10 Mobile und höher)

Damit alle anderen Geräte mit Windows Media Player synchronisiert werden können, müssen die folgenden Anforderungen erfüllt sein:

-   Vom Gerät muss eine PAP-Geräteschnittstelle mit {F33FDC04-D1AC-4E8E-9A30-19BBD4B108AE} angekündigt werden.
-   Die vom Dienstanbieter zurückgegebenen Geräte Objekte müssen die **IMDSPDevice3** -Schnittstelle unterstützen.
-   Der Geräteparameter useextendedwmdm muss auf den **DWORD** -Wert 1 festgelegt werden. Weitere Informationen finden Sie unter [Geräteparameter](device-parameters.md) .
-   Der Dienstanbieter sollte die folgenden Schnittstellen implementieren:

    [**IMDSPDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice3)

    [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2)

    [**IMDSPStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage4)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen eines Dienstanbieters**](creating-a-service-provider.md)
</dt> <dt>

[**Geräteparameter**](device-parameters.md)
</dt> </dl>

 

 




