---
title: Iagentnotifysink-Lesezeichen
description: Iagentnotifysink-Lesezeichen
ms.assetid: 172042af-a524-4ea4-955d-4e3dee079344
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1febedfc962904544a49b8621812d0518026b459
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709311"
---
# <a name="iagentnotifysinkbookmark"></a>Iagentnotifysink:: Bookmark

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT Bookmark(
   long dwBookMarkID  // bookmark ID
);                          
```

Benachrichtigt eine Client Anwendung, wenn Ihr Lesezeichen abgeschlossen ist.

-   Kein Rückgabewert.

<dl> <dt>

<span id="dwBookMarkID"></span><span id="dwbookmarkid"></span><span id="DWBOOKMARKID"></span>*dwbookmarkid*
</dt> <dd>

Der Bezeichner des Lesezeichens, das zum Auslösen des Ereignisses geführt hat.

</dd> </dl>

Wenn Sie Lesezeichen Tags in eine [**Sprech**](speak-method.md) Methode einbeziehen, können Sie nachverfolgen, wann Sie mit diesem Ereignis auftreten.

## <a name="see-also"></a>Weitere Informationen

[**Iagentcharacter::**](iagentcharacter--speak.md)Speech, [Microsoft Agent Speech Output-Tags](microsoft-agent-speech-output-tags.md)


 

 




