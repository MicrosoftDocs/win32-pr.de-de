---
title: Statusrückruffunktionen
description: Statusrückruffunktionen
ms.assetid: fe89fb97-0b56-4956-a1a6-f4ad2d06befa
keywords:
- AVICap-Rückruffunktionen,Status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f07539b016ea344f2a38d54a7274d01006532ed040ea3fa96990bff09e22d470
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037160"
---
# <a name="status-callback-functions"></a>Statusrückruffunktionen

Ein Erfassungsfenster kann Nachrichten an die Statusrückruffunktion senden, während Videos auf dem Datenträger erfasst werden, oder während anderer längerer Vorgänge, um Ihre Anwendung über den Fortschritt eines Vorgangs zu benachrichtigen. Die Statusinformationen enthalten einen Meldungsbezeichner und eine formatierte Textzeichenfolge, die zur Anzeige bereit sind. Ihre Anwendung kann den Nachrichtenbezeichner verwenden, um die Benachrichtigungen zu filtern und die Nachrichten so zu beschränken, dass sie dem Benutzer angezeigt werden. Bei Erfassungsvorgängen ist die erste Nachricht, die an die Rückruffunktion gesendet wird, immer IDS CAP BEGIN, und die letzte ist \_ \_ immer IDS CAP \_ \_ END. Der Meldungsbezeichner 0 (null) gibt an, dass ein neuer Vorgang gestartet wird und die Rückruffunktion den aktuellen Status löschen sollte.

 

 




