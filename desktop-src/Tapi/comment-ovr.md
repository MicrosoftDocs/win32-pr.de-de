---
description: Eine Anwendung kann während der Initiierung einer Sitzung einen Kommentar festlegen. Kommentare werden häufig zu Protokollierungszwecken verwendet.
ms.assetid: 46201166-de07-47b8-8d9a-c8edb7fb6926
title: Kommentar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 757570651315e0d4e9b313af9e926daf12cd25f3a6415037aaf92079bff5b824
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118868078"
---
# <a name="comment"></a>Kommentar

Eine Anwendung kann während der Initiierung einer Sitzung einen Kommentar festlegen. Kommentare werden häufig zu Protokollierungszwecken verwendet.

Nicht alle Dienstanbieter unterstützen die Verwendung dieser Informationen.

**TAPI 2.x:** Siehe [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCommentSize-** und **dwCommentOffset-Member** von *lpCallInfo*).

**TAPI 3.x:** Siehe [**ITCallInfo::get \_ CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIL \_ COMMENT** member of [**CALLINFO \_ STRING**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).

 

 
