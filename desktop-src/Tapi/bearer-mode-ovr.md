---
description: Der bearermodus entspricht der Qualität der vom Netzwerk angeforderten Übertragung zum Einrichten eines Aufrufes.
ms.assetid: 5276e1e7-7a91-4b74-b8c2-c0c7cebb203f
title: Bearermodus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1780bee44254e6da754584f838785452ee728f18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215357"
---
# <a name="bearer-mode"></a>Bearermodus

Der [**bearermodus**](./linebearermode--constants.md) entspricht der Qualität der vom Netzwerk angeforderten Übertragung zum Einrichten eines Aufrufes. Es ist wichtig, das Konzept des bearermodus vom [**Medientyp**](tapimediatype--constants.md)getrennt zu halten. Beispielsweise bietet das analoge Telefon Netzwerk (PSTN) nur einen 3,1 kHz-Funktionsträger Modus, aber Aufrufe, die ihn verwenden, können Medientypen wie z. b. sprach-, Fax-oder Datenmodem unterstützen.

Der bearermodus eines Aufrufes wird beim Einrichten des Aufrufes angegeben, oder er wird bereitgestellt, wenn der-Befehl angeboten wird. Wenn Linien Geräte channelpools darstellen können, kann ein Dienstanbieter zulassen, dass Aufrufe mit größerer Bandbreite hergestellt werden.

Nicht alle Dienstanbieter unterstützen die Verwendung dieser Informationen.

**TAPI 2. x:** Weitere Informationen finden Sie unter [**linesetcallparser**](/windows/win32/api/tapi/nf-tapi-linesetcallparams), [**linegetcallinfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwbearermode** -Member von [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo).

**TAPI 3. x:** Siehe [**itcallinfo:: get \_ callinfolong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**itcallinfo::p UT \_ callinfolong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong), **cil \_ bearermode** Member von [**CallInfo \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).

**TSPI:** Siehe [**Zeilen \_ Aufruf Info**](/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)) -Meldung, wobei *dwParam1* auf linecallinfostate \_ bearermode festgelegt ist.

 

 
