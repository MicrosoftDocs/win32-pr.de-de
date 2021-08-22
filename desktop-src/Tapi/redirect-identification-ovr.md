---
description: Wenn eine Anwendung eine Sitzung umleitet, behält TAPI Identifikationsinformationen über den Speicherort bei, von dem die Sitzung umgeleitet wurde, und den Speicherort, an den sie umgeleitet wurde.
ms.assetid: 08484b38-7c97-4acc-921e-0f566b2d3415
title: Umleitungsidentifikation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa7648167e6f60dc2e8593a576053df9a0ff54eb0fadc9a446a66127b435e5c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060448"
---
# <a name="redirect-identification"></a>Umleitungsidentifikation

Wenn eine Anwendung [eine Sitzung](redirect-ovr.md) umleitet, behält TAPI Identifikationsinformationen über den Speicherort bei, von dem die Sitzung umgeleitet wurde, und den Speicherort, an den sie umgeleitet wurde.

"Umleiten" bezieht sich auf den Speicherort, der den Umleitungsvorgang aufgerufen hat. "Redirection" identifiziert das neue Ziel für die Sitzung.

Nicht alle Dienstanbieter unterstützen die Verwendung dieser Informationen.

**TAPI 2.x: **[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwRedirectionIDSize**, **dwRedirectionIDOffset**, **dwRedirectionIDNameSize**, **dwRedirectionIDNameOffset**, **dwRedirectingIDSize**, **dwRedirectingIDOffset**, **dwRedirectingIDNameSize** und **dwRedirectingIDNameOffset-Elemente** von [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)

**TAPI 3.x: **[**ITCallInfo::get \_ CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring)wird mit dem **CIS \_ REDIRECTIONIDNAME-,** **CIS \_ REDIRECTIONIDNUMBER-,** **CIS \_ REDIRECTINGIDNAME-** oder **CIS \_ REDIRECTINGIDNUMBER-Element** von [**CALLINFO \_ STRING**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string) aufgerufen.

 

 
