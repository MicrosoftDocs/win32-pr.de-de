---
title: Abrufen eines Computers SDO
description: Der erste Schritt bei der Verwendung der SDO-API ist das Erstellen eines SDO-Computer Objekts.
ms.assetid: bdb01437-08d0-4279-94f2-840cb786cc44
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bf85f9712e76bbdadcffa3914a86cc56576aecd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039241"
---
# <a name="obtaining-a-machine-sdo"></a>Abrufen eines Computers SDO

Der erste Schritt bei der Verwendung der SDO-API ist das Erstellen eines SDO-Computer Objekts.

Verwenden Sie die [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) -Funktion, um den Klassen Bezeichner (CLSID) für das Objekt "SDO Machine" abzurufen. Der programmatische Bezeichner (ProgID), der für das-Objekt verwendet werden soll, ist "IAS. Sdomachine ".

Wenn Sie die CLSID haben, müssen Sie [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) mit dieser CLSID aufrufen. Geben Sie [**isdomachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) als Schnittstelle an, für die ein Zeiger zurückgegeben werden soll.

Beispielcode zum Abrufen eines Computers SDO finden [Sie unter Anfügen an einen SDO-Enabled Computer](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) .

 

 