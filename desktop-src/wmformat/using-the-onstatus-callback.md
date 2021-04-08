---
title: Verwenden des OnStatus-Rückrufs
description: Verwenden des OnStatus-Rückrufs
ms.assetid: 598e2d13-709b-42a3-ae06-b8c7d208ca9e
keywords:
- Windows Media-Format-SDK, OnStatus-Rückruf Methode
- Windows Media-Format-SDK, iwmstatus Callback-Schnittstelle
- OnStatus-Rückruf Methode, Informationen zu
- Iwmstatus Callback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e96b8d7fd75fd8a1d97a56c8b09304c51d0238
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103948412"
---
# <a name="using-the-onstatus-callback"></a>Verwenden des OnStatus-Rückrufs

Die [**iwmstatuscallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) -Rückruf Methode wird von mehreren Objekten im Windows Media-Format-SDK aufgerufen. **OnStatus** empfängt Nachrichten, die Änderungen am Status von SDK-Vorgängen darstellen.

Um die **OnStatus** -Rückruf Methode verwenden zu können, müssen Sie eine Klasse in der Anwendung implementieren, die von der [**iwmstatuscallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) -Schnittstelle erbt. Fügen Sie Code für Ihre Version von **OnStatus** in der-Klasse ein. Einige Beispiele für **OnStatus** -Implementierungen finden Sie in den Beispielen, die in diesem SDK enthalten sind. Weitere Informationen zu den Beispielen finden Sie unter [Beispielanwendungen](sample-applications.md).

Sie müssen die Implementierung des Status Rückrufs verschiedenen Objekten des Windows Media Format SDK zuordnen. Jedes-Objekt verfügt über eine andere Möglichkeit, diese Zuordnung vorzunehmen. Eine Liste der Methoden, die bestimmte Objekte zuordnen, finden Sie auf der Referenzseite zu **iwmstatus Callback** .

Die Statusmeldungen, die von **OnStatus** empfangen werden können, werden im [**WMT- \_ statusenumerationstyp**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) definiert.

Sie können auswählen, welche Nachrichten abgefangen und welche ignoriert werden sollen. Allerdings ist die Reaktion auf einige Statusmeldungen für bestimmte Features erforderlich. Bei Verwendung des asynchronen Readers öffnet die [**iwmreader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) -Methode z. b. eine Datei asynchron. Die einzige Möglichkeit, um zu erkennen, wann die Datei geöffnet wurde, ist das Abfangen der geöffneten MWT- \_ Nachricht. In der Regel sind die Nachrichten, auf die Sie Antworten, eine Benachrichtigung über den Abschluss von asynchronen Tasks.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden der Rückruf Methoden**](using-the-callback-methods.md)
</dt> </dl>

 

 




