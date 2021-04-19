---
description: Die ID des Aufrufes unterscheidet sich von der Sitzungs-ID in zwei primären Methoden, die vom Dienstanbieter zugewiesen werden, und ist für jede Anwendung, die die Sitzung verarbeitet, identisch.
ms.assetid: c9d0d43b-3053-4e3e-b442-57942f3448df
title: Telefonnummer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef571b55f653cb9c7bc1d61cdc8a3f71e91ba8f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350250"
---
# <a name="call-id"></a>Telefonnummer

Die ID des Aufrufes unterscheidet sich von der [Sitzungs](session-identifier-ovr.md) -ID in zweierlei Hinsicht: der Dienstanbieter weist Sie zu und ist für jede Anwendung, die die Sitzung verarbeitet, identisch. Sie kann nicht für die normale Kommunikation mit TAPI für Sitzungs Vorgänge verwendet werden, da Sie nicht mit einer bestimmten Anwendung identisch ist.

Die ID des Aufrufes wird in Vorgängen verwendet, z. b. die Bestimmung, ob eine Gruppe von Sitzungs-IDs tatsächlich auf einen-Befehl verweist, wie dies bei einer Konferenz der Fall ist oder für die Kommunikation mit einer anderen Anwendung

Nicht alle Dienstanbieter unterstützen die Verwendung dieser Informationen.

**TAPI 2. x:** Weitere Informationen finden Sie unter [**linegetcallinfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwcallid** -Member von [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)).

**TAPI 3. x:** Siehe [**itcallinfo:: get \_ callinfolong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**cil \_ callid** -Member von [**CallInfo \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).

 

 
