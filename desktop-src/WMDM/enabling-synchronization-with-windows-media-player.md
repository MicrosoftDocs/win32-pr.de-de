---
title: Aktivieren der Synchronisierung mit Windows Media Player
description: Aktivieren der Synchronisierung mit Windows Media Player
ms.assetid: a312dfef-ac48-4c58-a59a-b277f5386419
keywords:
- Windows Medien Geräte-Manager,Synchronisierung mit Windows Media Player
- Geräte-Manager,Synchronisierung mit Windows Media Player
- Programmierhandbuch,Synchronisierung mit Windows Media Player
- Dienstanbieter,Synchronisierung mit Windows Media Player
- Erstellen von Dienstanbietern,Synchronisierung mit Windows Media Player
- Synchronisierung mit Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef06dd0e32e0ea95674f54b94336ecb6882e8215775c857ee0780a58b71af75c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585008"
---
# <a name="enabling-synchronization-with-windows-media-player"></a>Aktivieren der Synchronisierung mit Windows Media Player

Sie können es einem Gerät ermöglichen, an der automatischen Synchronisierung mit Windows Media Player. Die automatische Synchronisierung bedeutet, dass beim Verbinden eines vom Benutzer festgelegten synchronisierten Geräts mit dem Computer Windows Media Player Automatisch Dateien vom Gerät herunterladt, aktualisiert oder löscht, ohne dass zusätzliche Benutzereingaben erforderlich sind.

Standardmäßig werden die folgenden Geräte mit Windows Media Player:

-   MTP-Geräte
-   Massenspeichergeräte
-   Windows CE (Windows Media Player 10 Mobile und höher)

Damit jedes andere Gerät mit dem Windows Media Player synchronisiert werden kann, müssen die folgenden Anforderungen erfüllt sein:

-   Das Gerät muss eine PAP-Geräteschnittstelle mit dem Namen {F33FDC04-D1AC-4E8E-9A30-19BBD4B108AE} ankäuten.
-   Die vom Dienstanbieter zurückgegebenen Geräteobjekte müssen die **IMDSPDevice3-Schnittstelle** unterstützen.
-   Der Geräteparameter UseExtendedWmdm muss auf den **DWORD-Wert** 1 festgelegt werden. Weitere [Informationen finden Sie](device-parameters.md) unter Geräteparameter.
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

 

 




