---
description: WIA stellt ein Kameragerät als hierarchische Struktur von IWiaItem-Objekten dar.
ms.assetid: fbb2821c-7f13-4fdd-a2ea-582be303855a
title: WIA-Kamerageräte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cb2023af90df6f868dfcace6f088bfe7ffeb6b549e0e20661231497f3fdf014
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592724"
---
# <a name="wia-camera-devices"></a>WIA-Kamerageräte

WIA stellt ein Kameragerät als hierarchische Struktur von [**IWiaItem-Objekten**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) dar. Das Stammelement, das von einem Aufruf der [**IWiaDevMgr::CreateDevice-Methode**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) des WIA-Geräte-Managers (Windows Image Acquisition) zurückgegeben wird, wird zum Abruf und Festlegen von Geräteinformationen, zum Steuern des Geräts und zum Starten der Geräteelementenumeration verwendet.

> [!Note]  
> WIA unterstützt keine Kameras in Windows Vista oder höher. Verwenden Sie für diese Versionen des Windows die Windows Portable Device (WPD)-API, die im Windows Driver Development Kit (DDK) beschrieben ist, um Bilder von Kameras zu erhalten.

 

Das folgende Diagramm veranschaulicht eine Beispielkameraimplementierung. Das Kamerastammelement enthält drei untergeordnete Elemente, zwei Bilder und einen Ordner. Der Ordner verfügt über zwei untergeordnete Elemente, beide Bilder.

![Beispiel für eine Kameraimplementierung](images/wihierar.gif)

 

 



