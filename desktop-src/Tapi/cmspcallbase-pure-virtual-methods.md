---
description: Diese Methoden müssen von abgeleiteten Klassen überschrieben werden.
ms.assetid: 2ea9d35a-c87e-44f4-8dc6-618251c81fe4
title: Reine virtuelle cmspcallbase-Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d8dea4c1a240e362a4dc3a19b3c09a37a318947
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865379"
---
# <a name="cmspcallbase-pure-virtual-methods"></a>Reine virtuelle cmspcallbase-Methoden

Diese Methoden müssen von abgeleiteten Klassen überschrieben werden.



| Reine virtuelle cmspcallbase-Methoden                                 | BESCHREIBUNG                                                                                                                             |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**Mspcalladressf**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcalladdref)               | Private adressf-Methode für das calltobjekt.                                                                                              |
| [**Mspcallrelease**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcallrelease)             | Private releasemethode für das-Objekt des-Objekts.                                                                                             |
| [**Init**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-init)                                 | Wird vom MSP-Adress Objekt (in [**der Methode "**](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)" "" "" "" "" "" "" "" "" "" "" " |
| [**Abschlusses**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-shutdown)                         | Wird vom MSP-Adress Objekt aufgerufen, um den Aufruf zu beenden.                                                                                |
| [**Internalkreatestream**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) | Wird von " [**kreatestream**](/windows/win32/api/tapi3if/nf-tapi3if-itstreamcontrol-createstream) " aufgerufen, um ein Streamobjekt zu erstellen.                                               |
| [**"Kreatestreamobject"**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-createstreamobject)     | Wird von [**internalkreatestream**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) aufgerufen, um ein Stream-Objekt zu erstellen.                                  |
| [**Removestream**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-removestream)                 | Wird von der Anwendung aufgerufen, um einen Stream aus dem Aufruf zu entfernen.                                                                              |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Cmspcallbase**](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallbase)
</dt> </dl>

 

 
