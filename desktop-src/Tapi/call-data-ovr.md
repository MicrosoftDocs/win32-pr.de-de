---
description: Beim Abrufen von Daten handelt es sich um einen Puffer mit variabler Größe, der zum Sammeln von Informationen über eine Kommunikationssitzung verwendet werden kann. Diese Informationen sind für alle Anwendungen verfügbar, die die Sitzung besitzen oder überwachen.
ms.assetid: 8b7a674f-ba78-4830-bb20-7fa74e202a1a
title: Daten abrufen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dedfd44a46518a58f3a3aeaec59326648669cb49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344759"
---
# <a name="call-data"></a>Daten abrufen

Beim Abrufen von Daten handelt es sich um einen Puffer mit variabler Größe, der zum Sammeln von Informationen über eine Kommunikationssitzung verwendet werden kann. Diese Informationen sind für alle Anwendungen verfügbar, die die Sitzung besitzen oder überwachen.

Beispielsweise könnte der anfängliche Handler einer eingehenden Sitzung Client Kontoinformationen in einen calldatenpuffer anfordern und eingeben. Anschließend müssten nachfolgende Handler die Anforderung nicht wiederholen.

Nicht alle Dienstanbieter unterstützen die Verwendung dieser Informationen.

**TAPI 2. x:** Weitere Informationen finden Sie unter [**linegetcallinfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), [**linesetcalldata**](/windows/win32/api/tapi/nf-tapi-linesetcalldata) (**dwcalldatasize** und **dwcalldataoffset** Members von [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)), [**line \_ CallInfo**](./line-callinfo.md) Message (*dwParam1* Set to linecallinfostate \_ calldata).

**TAPI 3. x:** Siehe [**itcallinfo::p UT \_ callinfobuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfobuffer) (**CIB \_ calldatabuffer** -Member des [**CallInfo- \_ Puffers**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)); [**Itcallinfochangeevent:: get \_ Ursache**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfochangeevent-get_cause) gibt den **CIC \_ calldata** -Member der [**callinfochange- \_ Ursache**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfochange_cause)zurück.

 

 
