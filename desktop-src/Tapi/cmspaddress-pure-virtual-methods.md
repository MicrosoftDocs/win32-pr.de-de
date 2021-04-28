---
description: 'REINE VIRTUELLE CMSPAddress-Methoden: Diese Methoden müssen von abgeleiteten Klassen überschrieben werden.'
ms.assetid: 68402cff-effd-4a2b-b9f9-f13f233b1555
title: CMSPAddress Pure Virtual Methods
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c9d9b9494e4ee42972d97433927fd587034af81
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084208"
---
# <a name="cmspaddress-pure-virtual-methods"></a>CMSPAddress Pure Virtual Methods

Diese Methoden müssen von abgeleiteten Klassen überschrieben werden.



| REINE VIRTUELLE CMSPAddress-Methoden                           | BESCHREIBUNG                                                                                                                                                                            |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MSPAddressAddRef**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressaddref)   | Private AddRef-Methode für die Adresse.                                                                                                                                                 |
| [**MSPAddressRelease**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressrelease) | Private Release-Methode für die Adresse.                                                                                                                                                |
| [**CreateMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)        | Wird von TAPI aufgerufen, um ein Aufrufobjekt zu erstellen. Die Implementierung in der abgeleiteten Klasse sollte einfach die [**CreateMSPCallHelper-Funktion**](/windows/desktop/api/Mspaddr/nf-mspaddr-createmspcallhelper) aufrufen.        |
| [**ShutdownMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-shutdownmspcall)    | Wird von TAPI aufgerufen, um ein Aufrufobjekt herunterfahren. Die Implementierung in der abgeleiteten Klasse sollte einfach die [**ShutdownMSPCallHelper-Funktion**](/windows/desktop/api/Mspaddr/nf-mspaddr-shutdownmspcallhelper) aufrufen. |
| [**GetCallMediaTypes**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getcallmediatypes) | Ruft vom MSP unterstützte Medientypen ab.                                                                                                                                                 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**CMSPAddress**](/windows/desktop/api/Mspaddr/nl-mspaddr-cmspaddress)
</dt> </dl>

 

 



