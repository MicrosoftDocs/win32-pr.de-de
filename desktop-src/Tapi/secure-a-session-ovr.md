---
description: Wenn eine Anwendung keine Störungen durch externe Ereignisse für eine Sitzung von TAPI oder dem Dienstanbieter wünscht, sollte Sie den-Befehl sichern.
ms.assetid: 0a3be209-e3ff-4177-abb2-ad0facbdf569
title: Sichern einer Sitzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00b1567303efb61f28f9c6b3e92c24287d23d4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369112"
---
# <a name="secure-a-session"></a>Sichern einer Sitzung

Wenn eine Anwendung keine Störungen durch externe Ereignisse für eine Sitzung von TAPI oder dem Dienstanbieter wünscht, sollte Sie den-Befehl sichern. Beispielsweise können in einer analogen Umgebung aufrufende Töne eine Fax-oder Modem Sitzung für den ursprünglichen-Befehl zerstören.

Eine Anwendung kann einen Aufruf zu dem Zeitpunkt sichern, an dem der Aufruf erfolgt ist, oder nachdem der Aufruf bereits vorhanden ist.

Nicht alle Dienstanbieter unterstützen die Verwendung dieses Vorgangs.

**TAPI 2. x:** Weitere Informationen finden Sie unter [**linesecurecall**](/windows/win32/api/tapi/nf-tapi-linesecurecall).

**TAPI 3. x:** Siehe [**itaddress:: Forward**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward).

 

 
