---
description: WIA stellt ein Kamera Gerät als hierarchische Struktur von iwiaitem-Objekten dar.
ms.assetid: fbb2821c-7f13-4fdd-a2ea-582be303855a
title: WIA-Kamerageräte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 002a14d8e047019b1af2d2f86c1fd4a2e00d7808
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214643"
---
# <a name="wia-camera-devices"></a>WIA-Kamerageräte

WIA stellt ein Kamera Gerät als hierarchische Struktur von [**iwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) -Objekten dar. Das Stamm Element, das von einem Aufrufen der Windows-Abbild Erfassungs Methode (WIA) Device Manager [**iwiadevmgr::**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) up-Device-Methode zurückgegeben wird, wird zum Abrufen und Festlegen von Geräteinformationen, zum Steuern des Geräts und zum Starten der Geräte Element-Enumeration verwendet.

> [!Note]  
> WIA unterstützt keine Kameras in Windows Vista oder höher. Verwenden Sie für diese Windows-Versionen die im Windows-Treiber Development Kit (DDK) beschriebene Windows-API für portable Geräte, um Images von Kameras abzurufen.

 

Das folgende Diagramm veranschaulicht eine Beispiel Kamera Implementierung. Das Stamm Element der Kamera enthält drei untergeordnete Elemente, zwei Bilder und einen Ordner. Der Ordner enthält zwei untergeordnete Elemente, beide Bilder.

![Beispiel für eine Kamera Implementierung](images/wihierar.gif)

 

 



