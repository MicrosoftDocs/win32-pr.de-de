---
title: Verwenden des OnStatus-Rückrufs
description: Verwenden des OnStatus-Rückrufs
ms.assetid: 598e2d13-709b-42a3-ae06-b8c7d208ca9e
keywords:
- Windows Media Format SDK, OnStatus-Rückrufmethode
- Windows Medienformat-SDK, IWMStatusCallback-Schnittstelle
- OnStatus-Rückrufmethode,About
- IWMStatusCallback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8eb1f2ae8ef64204435d7837b75258b77ec12f516103caeb936e82f979049ab4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027118"
---
# <a name="using-the-onstatus-callback"></a>Verwenden des OnStatus-Rückrufs

Die [**IWMStatusCallback::OnStatus-Rückrufmethode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) wird von mehreren Objekten im Windows Media Format SDK aufgerufen. **OnStatus** empfängt Nachrichten, die Änderungen am Status von SDK-Vorgängen darstellen.

Um die **OnStatus-Rückrufmethode** zu verwenden, müssen Sie eine Klasse in Ihrer Anwendung implementieren, die von der [**IWMStatusCallback-Schnittstelle erbt.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) Fügen Sie Code für Ihre **OnStatus-Version** in die -Klasse ein. Einige Beispiele für **OnStatus-Implementierungen** finden Sie in den Beispielen, die in diesem SDK enthalten sind. Weitere Informationen zu den Beispielen finden Sie unter [Beispielanwendungen](sample-applications.md).

Sie müssen Ihre Implementierung des Statusrückrufs verschiedenen Objekten des Windows Medienformat-SDK zuordnen. Jedes -Objekt hat eine andere Möglichkeit, diese Zuordnung zu erstellen. Eine Liste der Methoden, die bestimmte Objekte zuordnen, finden Sie auf der **Referenzseite zu IWMStatusCallback.**

Die Statusmeldungen, die von **OnStatus empfangen werden können,** werden im [**WMT \_ STATUS-Enumerationstyp**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) definiert.

Sie können auswählen, welche Nachrichten abfangen und welche ignoriert werden sollen. Für bestimmte Features ist jedoch eine Reaktion auf einige Statusmeldungen erforderlich. Wenn Sie beispielsweise den asynchronen Reader verwenden, öffnet [**die IWMReader::Open-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) eine Datei asynchron. Die einzige Möglichkeit, zu erkennen, wann die Datei geöffnet wurde, besteht im Abfangen der MELDUNG BEIM \_ ÖFFNEN. In der Regel sind die Meldungen, auf die Sie reagieren, Benachrichtigungen über den Abschluss asynchroner Aufgaben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden der Rückrufmethoden**](using-the-callback-methods.md)
</dt> </dl>

 

 




