---
title: Abrufen von MCI-Systeminformationen
description: Abrufen von MCI-Systeminformationen
ms.assetid: 06175d6e-6d09-4c95-93e9-03af870a2d3f
keywords:
- MCI_SYSINFO Befehl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fa6cc0757bc09aa16216f2f20385bf31b44bb88e27ea64e091ff3909d8d57e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893220"
---
# <a name="obtaining-mci-system-information"></a>Abrufen von MCI-Systeminformationen

Der [Befehl sysinfo](sysinfo.md) ([**MCI \_ SYSINFO**](mci-sysinfo.md)) erhält Systeminformationen zu MCI-Geräten. MCI verarbeitet diesen Befehl, ohne ihn an ein MCI-Gerät weiter zu übertragen. Für die Befehlsmeldungsschnittstelle gibt MCI die Systeminformationen in der [**MCI \_ SYSINFO \_ PARMS-Struktur**](mci-sysinfo-parms.md) zurück.

Sie können den **Sysinfo-Befehl** (MCI SYSINFO) verwenden, um Informationen wie die Anzahl der MCI-Geräte auf einem System, die Anzahl der MCI-Geräte eines bestimmten Typs, die Anzahl der geöffneten MCI-Geräte und die Namen der Geräte \_ abzurufen. Dieser Befehl wird häufig mehr als einmal aufgerufen, um eine bestimmte Information abzurufen. Beispielsweise können Sie die Anzahl der Geräte eines bestimmten Typs im ersten Aufruf abrufen und dann im nächsten Aufruf die Namen der Geräte aufzählen.

 

 




