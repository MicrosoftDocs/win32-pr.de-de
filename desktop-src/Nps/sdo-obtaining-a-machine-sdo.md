---
title: Abrufen eines Computer-SDO
description: Der erste Schritt bei der Verwendung der SDO-API besteht im Erstellen eines SDO-Computerobjekts.
ms.assetid: bdb01437-08d0-4279-94f2-840cb786cc44
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9217333440235d5adac544e00420f8564513510908a89a1da7494cf7ba2772ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128600"
---
# <a name="obtaining-a-machine-sdo"></a>Abrufen eines Computer-SDO

Der erste Schritt bei der Verwendung der SDO-API besteht im Erstellen eines SDO-Computerobjekts.

Verwenden Sie [**die CLSIDFromProgID-Funktion,**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) um den Klassenbezeichner (CLSID) für das SDO-Computerobjekt zu erhalten. Der programmgesteuerte Bezeichner (ProgID), der für das Objekt verwendet werden soll, ist "IAS. SdoMachine".

Sobald Sie über die CLSID verfügen, rufen [**Sie CoCreateInstance mit**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) dieser CLSID auf. Geben [**Sie ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) als Schnittstelle an, für die ein Zeiger zurückgeben werden soll.

Beispielcode zum Abrufen eines [Computer-SDO](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) finden Sie unter Anfügen an einen SDO-Enabled-Computer.

 

 