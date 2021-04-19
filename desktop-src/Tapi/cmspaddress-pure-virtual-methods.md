---
description: Diese Methoden müssen von abgeleiteten Klassen überschrieben werden.
ms.assetid: 68402cff-effd-4a2b-b9f9-f13f233b1555
title: Reine virtuelle cmspaddress-Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a93c9b2a995554dd2f7412c8fa5bf153ea8871e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348635"
---
# <a name="cmspaddress-pure-virtual-methods"></a>Reine virtuelle cmspaddress-Methoden

Diese Methoden müssen von abgeleiteten Klassen überschrieben werden.



| Reine virtuelle cmspaddress-Methoden                           | BESCHREIBUNG                                                                                                                                                                            |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Mspaddressadressf**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressaddref)   | Private adressf-Methode für die Adresse.                                                                                                                                                 |
| [**Mspaddressrelease**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressrelease) | Private releasemethode für die Adresse.                                                                                                                                                |
| [**"" Für ""**](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)        | Wird von TAPI aufgerufen, um ein Aufruf Objekt zu erstellen. Die Implementierung in der abgeleiteten Klasse sollte einfach die Funktion " [**deatemspcallhelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-createmspcallhelper) " aufrufen.        |
| [**Shutdownmspcallcenter**](/windows/desktop/api/msp/nf-msp-itmspaddress-shutdownmspcall)    | Wird von TAPI aufgerufen, um ein Aufruf Objekt zu schließen. Die Implementierung in der abgeleiteten Klasse sollte einfach die [**shutdownmspcallhelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-shutdownmspcallhelper) -Funktion aufrufen. |
| [**Getcallmediatypes**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getcallmediatypes) | Ruft die vom MSP unterstützten Medientypen ab.                                                                                                                                                 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Cmspaddress**](/windows/desktop/api/Mspaddr/nl-mspaddr-cmspaddress)
</dt> </dl>

 

 



