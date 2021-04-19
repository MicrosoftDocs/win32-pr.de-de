---
description: Die Rate oder Bandbreite eines Aufrufes gibt die Geschwindigkeit der Datenübertragung an. Drei Datenpunkte identifizieren die Rate der aktuellen Rate der maximalen Rate für einen angegebenen bearermodus und den minimalen Satz für den bearermodus.
ms.assetid: bc373ac5-a986-483f-a136-60cdc2e2c6b0
title: Rate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40747c26a98d8eb69e8161fb04302c5187121dff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356951"
---
# <a name="rate"></a>Rate

Die Rate (oder Bandbreite) eines Aufrufes gibt die Geschwindigkeit der Datenübertragung an. Rate von drei Datenpunkten: die aktuelle Rate, die maximale Rate für einen angegebenen bearermodus und die minimale Rate für den bearermodus.

Nicht alle Dienstanbieter unterstützen die Verwendung dieser Informationen.

* * TAPI 2. x: * *[**linesetcallparser**](/windows/win32/api/tapi/nf-tapi-linesetcallparams), [**linegetcallinfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwminrate** oder **dwmaxrate** Member von [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)

* * TAPI 3. x: * *[**itcallinfo:: get \_ callinfolong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**itcallinfo::p UT \_ callinfolong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong), **cil \_ maxrate**, **cil \_ minrate** oder **cil \_ Rate** Member von [**CallInfo \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)

* * TSPI: * *[**Zeile \_ CallInfo**](/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)) -Meldung mit *dwParam1* auf linecallinfostate- \_ Rate festgelegt

 

 
