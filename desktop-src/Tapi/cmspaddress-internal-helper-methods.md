---
description: In der folgenden Liste sind die internen CMSP-Adress Methoden enthalten.
ms.assetid: 2016a776-1464-46b5-96b9-b045834f9e38
title: Interne cmspaddress-Hilfsmethoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17064d161e2a073addb2e8eef6d9d290b41278b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363850"
---
# <a name="cmspaddress-internal-helper-methods"></a>Interne cmspaddress-Hilfsmethoden



| Interne cmspaddress-Hilfsmethoden                                        | BESCHREIBUNG                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Getstaticterminals**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getstaticterminals)               | Wird von [**get \_ staticterminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_staticterminals) und [**enumeratestaticterminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratestaticterminals) aufgerufen, um ein Array von statischen Terminals zu erhalten, das für diese Adresse verwendet werden kann.                                     |
| [**Getdynamicterminalclasses**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getdynamicterminalclasses) | Wird von [**get \_ dynamicterminalclasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_dynamicterminalclasses) und [**enumeratedynamicterminalclasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratedynamicterminalclasses) aufgerufen, um ein Array dynamischer Terminal Klassen zu erhalten, das für diese Adresse verwendet werden kann. |
| [**Updateterminallist**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-updateterminallist)               | Füllt die Liste der statischen Terminals des MSP auf.                                                                                                                                                                                                                                |
| [**Receivetspaddressdata**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-receivetspaddressdata)         | Wird aufgerufen, wenn eine TSP-Daten Nachricht von der Adresse anstelle eines bestimmten Aufrufs verarbeitet werden soll.                                                                                                                                                                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Cmspaddress**](/windows/desktop/api/Mspaddr/nl-mspaddr-cmspaddress)
</dt> </dl>

 

 
