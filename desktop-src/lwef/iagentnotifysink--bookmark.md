---
title: IAgentNotifySink-Lesezeichen
description: IAgentNotifySink-Lesezeichen
ms.assetid: 172042af-a524-4ea4-955d-4e3dee079344
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02562b7cbf42c3445a25edc5071476da1b2d8dc53d80923ad875fddf09e5d31b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477096"
---
# <a name="iagentnotifysinkbookmark"></a>IAgentNotifySink::Bookmark

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT Bookmark(
   long dwBookMarkID  // bookmark ID
);                          
```

Benachrichtigt eine Clientanwendung, wenn das Lesezeichen abgeschlossen ist.

-   Kein Rückgabewert.

<dl> <dt>

<span id="dwBookMarkID"></span><span id="dwbookmarkid"></span><span id="DWBOOKMARKID"></span>*dwBookMarkID*
</dt> <dd>

Bezeichner des Lesezeichens, das zum Auslösen des Ereignisses führte.

</dd> </dl>

Wenn Sie Lesezeichentags in eine [**Speak-Methode**](speak-method.md) einfügen, können Sie nachverfolgen, wann sie mit diesem Ereignis auftreten.

## <a name="see-also"></a>Weitere Informationen

[**IAgentCharacter::Speak**](iagentcharacter--speak.md), [Microsoft Agent Speech-Ausgabetags](microsoft-agent-speech-output-tags.md)


 

 




