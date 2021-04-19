---
description: Die Beendigung der Sitzung kann eine Benutzer Anforderung, eine Remote Trennung durch die andere Partei oder anwendungsspezifische Gründe haben.
ms.assetid: 69ed2e2c-f1c7-4f69-86a0-3cfdd80e423d
title: Beenden einer Sitzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac433f1c8104ec41a3c42dc44c32a2b110d79469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366333"
---
# <a name="terminate-a-session"></a>Beenden einer Sitzung

Die Beendigung der Sitzung kann eine Benutzer Anforderung, eine Remote Trennung durch die andere Partei oder anwendungsspezifische Gründe haben. Wenn eine Sitzung beendet wird, bleibt die [Sitzungs](session-identifier-ovr.md) -ID gültig, bis Sie explizit freigegeben wird, und kann zum Erfassen von Daten nach der Verbindung verwendet werden.

Die Beendigung der Sitzung wird durch Aufheben der Zuordnung und Freigabe der der Sitzung zugeordneten Ressourcen abgeschlossen. Wenn eine Sitzung lediglich gelöscht oder getrennt wird, aber keine Ressourcen freigegeben werden, ist das Ergebnis ein Speicher Abfall in der Anwendung und möglicherweise auch im Dienstanbieter.

**TAPI 2. x:** Weitere Informationen finden Sie unter [**linedrop**](/windows/win32/api/tapi/nf-tapi-linedrop), [**linedezugewiesene eCall**](/windows/win32/api/tapi/nf-tapi-linedeallocatecall).

**TAPI 3. x:** Weitere Informationen finden Sie unter [**itbasiccallcontrol::D isconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect), Ausführen einer Standard-com-Version auf dem callobjektzeiger.

 

 
