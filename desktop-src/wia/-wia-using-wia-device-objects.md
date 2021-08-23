---
description: Ein Bildverarbeitungsgerät wird in Windows Image Acquisition (WIA) als hierarchische Struktur von WIA-Elementobjekten (IWiaItem-Schnittstellen) dargestellt.
ms.assetid: 5f3e56aa-8616-4574-882c-619caf54ca04
title: Verwenden von WIA-Geräteobjekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4f9ec9fd4a3fc4746b1908863ae6afcdcc60b54aa7f9f8f73c769d52ad08688
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813480"
---
# <a name="using-wia-device-objects"></a>Verwenden von WIA-Geräteobjekten

Ein Bildverarbeitungsgerät wird in Windows Image Acquisition (WIA) als hierarchische Struktur von WIA-Elementobjekten [**(IWiaItem-Schnittstellen)**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) dargestellt. In der Regel stellt der Stamm dieser Elementstruktur das Gerät selbst dar, während die anderen Elemente in der Struktur Bilder für eine Kamera oder Scanregionen für einen Scanner darstellen.

Anwendungen verwenden den WIA-Geräte-Manager zum Erstellen und Aufzählen von WIA-Geräten. In den folgenden Abschnitten wird erläutert, wie WIA-Geräte erstellt und verwendet werden:

-   [Auswählen eines Geräts](-wia-selecting-a-device.md)
-   [WIA-Kamerageräte](-wia-wia-camera-devices.md)
-   [WIA-Scannergeräte](-wia-wia-scanner-devices.md)

 

 



