---
description: Der Kompatibilitäts Puffer ist spezifisch für den ISDN Q. 931-Standard. Informationen zur Bedeutung und Verwendung dieser Daten finden Sie in der Dokumentation Ihres Dienstanbietern.
ms.assetid: c4c87ca8-fbae-4275-9b69-7b32daf4c18f
title: Kompatibilitäts Puffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8669e32cd47978c10e2f5abdbe076bcf08ba1862
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372884"
---
# <a name="compatibility-buffer"></a>Kompatibilitäts Puffer

Der Kompatibilitäts Puffer ist spezifisch für den ISDN Q. 931-Standard. Informationen zur Bedeutung und Verwendung dieser Daten finden Sie in der Dokumentation Ihres Dienstanbieters.

Nicht alle Dienstanbieter unterstützen die Verwendung dieser Informationen.

**TAPI 2. x:** Weitere Informationen finden Sie unter [**linegetcallinfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwhighlevelcompsize**, **dwhighlevelcompoffset**, **dwlowlevelcompsize** und **dwlowlevelcompoffset** Members von *lpcallinfo*).

**TAPI 3. x:** Siehe [**itcallinfo:: get \_ callinfobuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfobuffer) (**CIB \_ highlevelcompatibilitybuffer** und **CIB \_ lowlevelcompatibilitybuffer** Member des [**CallInfo- \_ Puffers**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)).

 

 
