---
description: Die Rate oder Bandbreite eines Aufrufs gibt die Geschwindigkeit der Datenübertragung an. Drei Datenpunkte identifizieren die aktuelle Rate, die maximale Rate für einen angegebenen Bearermodus und die Mindestrate für den Bearermodus.
ms.assetid: bc373ac5-a986-483f-a136-60cdc2e2c6b0
title: Rate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce0af0b2dd6dfe34759753f52773bafe0bdf2bf8f4472ed863dcc6c8b0f10a0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060558"
---
# <a name="rate"></a>Rate

Die Rate (oder Bandbreite) eines Aufrufs gibt die Geschwindigkeit der Datenübertragung an. Drei Datenpunkte identifizieren die Rate: die aktuelle Rate, die maximale Rate für einen angegebenen Bearermodus und die Mindestrate für den Bearermodus.

Nicht alle Dienstanbieter unterstützen die Verwendung dieser Informationen.

**TAPI 2.x: **[**lineSetCallParams**](/windows/win32/api/tapi/nf-tapi-linesetcallparams), [**lineGetCallInfo,**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) **dwMinRate** oder **dwMaxRate-Element** von [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)

**TAPI 3.x: **[**ITCallInfo::get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**ITCallInfo::p ut \_ CallInfoLong,**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong) **CIL \_ MAXRATE,** **CIL \_ MINRATE** oder **CIL \_ RATE Member** von [**CALLINFO \_ LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)

**TSPI: **[**LINE \_ CALLINFO-Nachricht,**](/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)) *bei der dwParam1* auf LINECALLINFOSTATE RATE festgelegt \_ ist

 

 
