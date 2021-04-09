---
description: Wenn Sie eine Sitzung löschen oder trennen, wird die Kommunikation beendet. Die Anwendung hat die Möglichkeit, Benutzer Benutzerinformationen zum Zeitpunkt der Trennung zu senden, wenn Sie vom Dienstanbieter unterstützt wird.
ms.assetid: dc348bb2-d564-40f8-afe3-5473c5769fa4
title: Verwerfen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a9bf3705d9b104b8816ce4b493ec6b188c5fe1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958816"
---
# <a name="drop"></a>Verwerfen

Wenn Sie eine Sitzung löschen oder trennen, wird die Kommunikation beendet. Die Anwendung hat die Möglichkeit, Benutzer Benutzerinformationen zum Zeitpunkt der Trennung zu senden, wenn Sie vom Dienstanbieter unterstützt wird.

Die üblichen Gründe für das Löschen einer Sitzung ist, dass ein Benutzer eine Trennung angefordert hat oder das andere Ende der Sitzung gelöscht wurde. Ein Drop-Vorgang kann auch aufgerufen werden, wenn TAPI eine Sitzung für die Anwendung anbietet. Wenn der Dienstanbieter dies unterstützt, hat dies den Effekt, dass die Anwendung den-Befehl ablehnt.

Beim Aufrufen eines Drop-Vorgangs können auch Verwandte Sitzungen beeinträchtigt werden. Beispielsweise können durch das Löschen eines Konferenz Aufrufes alle einzelnen Teilnehmer gelöscht werden. Zustands Änderungs Meldungen werden für alle Aufrufe, deren Status betroffen ist, an die Anwendung gesendet.

In verschiedenen überbrückenden oder parteigebundenen Konfigurationen wird der-Vorgang möglicherweise nicht durch einen Drop-Vorgang gelöscht, wenn mehrere Parteien den-Befehl aufzurufen. Beispielsweise kann der-Befehl in einer überbrückten Situation nicht gelöscht werden, da der Status anderer Stationen des Aufrufes steuern kann. Stattdessen kann der-Befehl einfach in den inaktiven Zustand geändert werden, während er an anderen Stationen verbunden bleibt.

Nach einem Drop-Vorgang können die Sitzungs-ID und die meisten Ressourcen, die der Sitzung zugeordnet sind, für die meisten Abfrage Vorgänge verwendet werden. Wenn eine Anwendung diese Ressourcen nicht mehr benötigt, muss Sie [die Sitzung beenden](terminate-a-session-ovr.md) , um Speicher Verluste zu vermeiden.

**TAPI 2. x:** Siehe [**linedrop**](/windows/win32/api/tapi/nf-tapi-linedrop).

**TAPI 3. x:** Weitere Informationen finden Sie unter [**itbasiccallcontrol::D isconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).

 

 
