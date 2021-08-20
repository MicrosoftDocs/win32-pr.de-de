---
description: Die Aufruf-ID unterscheidet sich von der Sitzungs-ID auf zwei primäre Weisen, die der Dienstanbieter zuweist, und ist für jede Anwendung, die die Sitzung verarbeitet, identisch.
ms.assetid: c9d0d43b-3053-4e3e-b442-57942f3448df
title: Anruf-ID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb32a8cd00e3c8f77bcabb14de79170a259fba0e40ddb354afeab022528369c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118870149"
---
# <a name="call-id"></a>Anruf-ID

Die Aufruf-ID unterscheidet sich von der [Sitzungs-ID](session-identifier-ovr.md) auf zwei primäre Arten: Der Dienstanbieter weist sie zu und ist für jede Anwendung, die die Sitzung verarbeitet, identisch. Sie kann nicht für die normale Kommunikation mit TAPI in Bezug auf Sitzungsvorgänge verwendet werden, da sie nicht mit einer bestimmten Anwendung übereinstimmt.

Die Anruf-ID wird in Vorgängen verwendet, z. B. bei der Bestimmung, ob eine Gruppe von Sitzungs-IDs tatsächlich auf einen Anruf verweist, wie dies bei einer Konferenz der Fall ist, oder für die Kommunikation mit einer anderen Anwendung.

Nicht alle Dienstanbieter unterstützen die Verwendung dieser Informationen.

**TAPI 2.x:** Siehe [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCallID-Member** von [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)).

**TAPI 3.x:** Siehe [**ITCallInfo::get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL \_ CALLID** member of [**CALLINFO \_ LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).

 

 
