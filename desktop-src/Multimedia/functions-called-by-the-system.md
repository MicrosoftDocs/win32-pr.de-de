---
title: Vom System aufgerufene Funktionen
description: Vom System aufgerufene Funktionen
ms.assetid: 006ac524-d456-44e9-957b-42a85dc92519
keywords:
- Multimedia-Audiofunktionen, ACM-Funktionen
- Audiofunktionen, ACM-Funktionen
- Audiokomprimierungs-Manager (ACM), Funktionen
- ACM (Audiokomprimierungs-Manager), Funktionen
- ACM-Funktionen
- Rückruffunktionen
- Audiokomprimierungs-Manager (ACM), Rückruf Funktionen
- ACM (Audiokomprimierungs-Manager), Rückruf Funktionen
- Hook-Verfahren
- Treiber Prozeduren
- Audiokomprimierungs-Manager (ACM), Hook-Prozeduren
- ACM (Audiokomprimierungs-Manager), Hook-Prozeduren
- Audiokomprimierungs-Manager (ACM), Treiber Prozeduren
- ACM (Audiokomprimierungs-Manager), Treiber Prozeduren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1324ea168892d54f21754658607476c35075910
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106337841"
---
# <a name="functions-called-by-the-system"></a>Vom System aufgerufene Funktionen

Das System ruft drei verschiedene Arten von Anwendungs definierten Funktionen auf. Rückruf Funktionen sind Funktionen in der Anwendung, die vom System als Antwort auf eine Anforderung einer Anwendung aufgerufen werden. Mithilfe von Hook-Prozeduren wird die Anpassung von Dialogfeldern von der Anwendung behandelt. Eine Treiber Prozedur ist die Implementierung eines eigenen Codecs, Konverters oder Filters einer Anwendung.

Die Rückruf Funktionen haben die folgenden Namen:

-   [**acmdriverenumcallback**](/windows/win32/api/msacm/nc-msacm-acmdriverenumcb)
-   [**acmfilterenumcallback**](/windows/desktop/api/Msacm/nc-msacm-acmfilterenumcb)
-   [**acmfiltertagenumschlag**](/windows/desktop/api/Msacm/nc-msacm-acmfiltertagenumcb)
-   [**acmformatenumcallback**](/windows/desktop/api/Msacm/nc-msacm-acmformatenumcb)
-   [**acmformattagenumschlag**](/windows/desktop/api/Msacm/nc-msacm-acmformattagenumcb)
-   [**acmstreamconvertcallback**](/previous-versions//dd742925(v=vs.85))

Die meisten Enumerationsfunktionen im ACM verwenden Rückruf Funktionen. Wenn Sie z. b. eine Enumerationsfunktion aufrufen, listet das ACM die Elemente auf, indem die Anwendung wiederholt über die Rückruffunktion aufgerufen wird.

Einige Funktionen können nicht in diesen Rückruf Funktionen aufgerufen werden. Funktionen, die nicht aufgerufen werden können, bearbeiten interne ACM-Strukturen, die von den-Enumerationsfunktionen verwendet werden. Die folgenden Funktionen sollten nicht innerhalb einer Rückruffunktion aufgerufen werden:

-   [**acmdriveradd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd)
-   [**acmdriverpriority**](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority)
-   [**acmdriverremove**](/windows/desktop/api/Msacm/nf-msacm-acmdriverremove)

Das System ruft die folgenden Funktionen auf, um einer Anwendung zu helfen, die Anpassung von Dialogfeldern zu handhaben:

-   [**acmfilterchooabhuokproc**](/windows/desktop/api/Msacm/nc-msacm-acmfilterchoosehookproc)
-   [**acmformatchooabhuokproc**](/windows/desktop/api/Msacm/nc-msacm-acmformatchoosehookproc)

Die folgende Funktion wird als Prototyp angegeben, der es einer Anwendung ermöglicht, einen angepassten Codec, Konverter oder Filter zu verwenden. Eine Funktion, die diesem Prototyp entspricht, kann als Argument an die [**acmdriveradd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) -Funktion übermittelt werden.

-   [**acmdriverproc**](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc)

 

 