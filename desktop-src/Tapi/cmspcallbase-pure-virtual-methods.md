---
description: 'CMSPCallBase Pure Virtual Methods : Diese Methoden müssen von abgeleiteten Klassen überschrieben werden.'
ms.assetid: 2ea9d35a-c87e-44f4-8dc6-618251c81fe4
title: CMSPCallBase – reine virtuelle Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8da8530ab3dae737bf1407f00d5d4a415a1437e3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094458"
---
# <a name="cmspcallbase-pure-virtual-methods"></a>CMSPCallBase – reine virtuelle Methoden

Diese Methoden müssen von abgeleiteten Klassen überschrieben werden.



| REINE VIRTUELLE CMSPCallBase-Methoden                                 | BESCHREIBUNG                                                                                                                             |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**MSPCallAddRef**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcalladdref)               | Private AddRef-Methode für das Aufrufobjekt.                                                                                              |
| [**MSPCallRelease**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcallrelease)             | Private Release-Methode für das Aufrufobjekt.                                                                                             |
| [**Init**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-init)                                 | Wird vom MSP-Adressobjekt (in der [**Methode CreateMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)) aufgerufen, um das MSP-Aufrufobjekt zu initialisieren. |
| [**Herunterfahren**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-shutdown)                         | Wird vom MSP-Adressobjekt aufgerufen, um den Aufruf herunterzufahren.                                                                                |
| [**InternalCreateStream**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) | Wird von [**CreateStream**](/windows/win32/api/tapi3if/nf-tapi3if-itstreamcontrol-createstream) aufgerufen, um ein Streamobjekt zu erstellen.                                               |
| [**CreateStreamObject**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-createstreamobject)     | Wird von [**InternalCreateStream**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) aufgerufen, um ein Streamobjekt zu erstellen.                                  |
| [**RemoveStream**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-removestream)                 | Wird von der Anwendung aufgerufen, um einen Stream aus dem Aufruf zu entfernen.                                                                              |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**CMSPCallBase**](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallbase)
</dt> </dl>

 

 
