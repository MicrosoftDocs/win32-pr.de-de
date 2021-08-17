---
description: Die möglichen Gründe für eine eingehende Sitzung, z. B. die Übertragung, sind in den \_ LINECALLREASON-Konstanten aufgeführt.
ms.assetid: 94cc1a79-7ce4-47ec-bdd8-ee7f0d9f48ed
title: Grund
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4be431b5d3918714a11fb95411a8d5503a47f9e6d4cd462f9a208f00dfb96c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139953"
---
# <a name="reason"></a>`Reason`

Die möglichen Gründe für eine eingehende Sitzung, z. B. die Übertragung, sind in den [LINECALLREASON-Konstanten \_ ](./linecallreason--constants.md)aufgeführt.

Nicht alle Dienstanbieter unterstützen die Verwendung dieser Informationen.

**TAPI 2.x: **[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (** dwReason-Member** von *lpCallInfo*)

**TAPI 3.x: **[**ITCallInfo::get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (** CIL \_ REASON** member of [**CALLINFO \_ LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long))

 

 
