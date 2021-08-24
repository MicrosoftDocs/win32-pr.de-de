---
title: Vom System aufgerufene Funktionen
description: Vom System aufgerufene Funktionen
ms.assetid: 006ac524-d456-44e9-957b-42a85dc92519
keywords:
- Multimediaaudio, ACM-Funktionen
- Audio,ACM-Funktionen
- Audiokomprimierungs-Manager (ACM), Funktionen
- ACM (Audiokomprimierungs-Manager), Funktionen
- ACM-Funktionen
- Rückruffunktionen
- Audiokomprimierungs-Manager (ACM), Rückruffunktionen
- ACM (Audiokomprimierungs-Manager), Rückruffunktionen
- Hookverfahren
- Treiberverfahren
- Audiokomprimierungs-Manager (ACM), Hookverfahren
- ACM (Audiokomprimierungs-Manager), Hookverfahren
- Audiokomprimierungs-Manager (ACM), Treiberverfahren
- ACM (Audiokomprimierungs-Manager), Treiberverfahren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11b8a8c3615ae0124d4701f8d37d332e652d8390ef165cec8dc57d881cd328fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678619"
---
# <a name="functions-called-by-the-system"></a>Vom System aufgerufene Funktionen

Das System ruft drei verschiedene Arten von anwendungsdefinierten Funktionen auf. Rückruffunktionen sind Funktionen in Ihrer Anwendung, die das System als Reaktion auf eine anforderung einer Anwendung aufruft. Hookverfahren helfen einer Anwendung bei der Anpassung von Dialogfeldern. Eine Treiberprozedur ist die Implementierung eines eigenen Codecs, Konverters oder Filters einer Anwendung.

Die Rückruffunktionen haben die folgenden Namen:

-   [**acmDriverEnumCallback**](/windows/win32/api/msacm/nc-msacm-acmdriverenumcb)
-   [**acmFilterEnumCallback**](/windows/desktop/api/Msacm/nc-msacm-acmfilterenumcb)
-   [**acmFilterTagEnumCallback**](/windows/desktop/api/Msacm/nc-msacm-acmfiltertagenumcb)
-   [**acmFormatEnumCallback**](/windows/desktop/api/Msacm/nc-msacm-acmformatenumcb)
-   [**acmFormatTagEnumCallback**](/windows/desktop/api/Msacm/nc-msacm-acmformattagenumcb)
-   [**acmStreamConvertCallback**](/previous-versions//dd742925(v=vs.85))

Die meisten Enumerationsfunktionen im ACM verwenden Rückruffunktionen. Wenn Sie beispielsweise eine Enumerationsfunktion aufrufen, werden die Elemente vom ACM durch wiederholtes Aufrufen der Anwendung über die Rückruffunktion aufgelistet.

Einige Funktionen können nicht innerhalb dieser Rückruffunktionen aufgerufen werden. Funktionen, die nicht aufgerufen werden können, bearbeiten interne ACM-Strukturen, die von den Enumerationsfunktionen verwendet werden. Die folgenden Funktionen sollten nicht innerhalb einer Rückruffunktion aufgerufen werden:

-   [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd)
-   [**acmDriverPriority**](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority)
-   [**acmDriverRemove**](/windows/desktop/api/Msacm/nf-msacm-acmdriverremove)

Das System ruft die folgenden Funktionen auf, um eine Anwendung bei der Anpassung von Dialogfeldern zu unterstützen:

-   [**acmFilterChooseHookProc**](/windows/desktop/api/Msacm/nc-msacm-acmfilterchoosehookproc)
-   [**acmFormatChooseHookProc**](/windows/desktop/api/Msacm/nc-msacm-acmformatchoosehookproc)

Die folgende Funktion wird als Prototyp angegeben, der es einer Anwendung ermöglicht, einen benutzerdefinierten Codec, Konverter oder Filter zu verwenden. Eine Funktion, die diesem Prototyp entspricht, kann als Argument an die [**acmDriverAdd-Funktion übergeben**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) werden.

-   [**acmDriverProc**](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc)

 

 