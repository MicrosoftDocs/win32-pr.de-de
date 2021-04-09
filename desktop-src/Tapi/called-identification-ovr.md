---
description: Die bezeichnete Identifikation identifiziert die ursprüngliche Zieladresse für eine Sitzung. In Situationen, in denen eine Sitzung umgeleitet, weitergeleitet oder übertragen wurde, unterscheidet sich dies von der verbundenen Identifikation.
ms.assetid: a03286eb-83a9-4170-b514-e8899fd04c74
title: Bezeichnete Identifikation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63f862d18fb3deb661cb8379c90a4b3e70caab1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866595"
---
# <a name="called-identification"></a>Bezeichnete Identifikation

Die bezeichnete Identifikation identifiziert die ursprüngliche Zieladresse für eine Sitzung. In Situationen, in denen eine Sitzung umgeleitet, weitergeleitet oder übertragen wurde, unterscheidet sich dies von der [verbundenen Identifikation](connected-identification-ovr.md).

Nicht alle Dienstanbieter unterstützen die Verwendung dieser Informationen.

**TAPI 2. x:** Weitere Informationen finden Sie unter [**linegetcallinfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwcalledidflags**, **dwcalledidsize**, **dwcalledidoffset**, **dwcalledidnamesize**, **dwcalledidnameoffset** und **dwcalledidadresstype** Members von *lpcallinfo*).

**TAPI 3. x:** Siehe [**itcallinfo:: get \_ callinfolong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**cil \_ calledidadresssstype** -Member von [**CallInfo \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)) [**, itcallinfo:: get \_ callinfostring**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIS \_ calledidname** und **CIS \_ calledidname** Members von [**CallInfo \_ String**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).

 

 
