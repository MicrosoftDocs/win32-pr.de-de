---
title: Auflisten von senken
description: Auflisten von senken
ms.assetid: 1b635cd8-6bdd-4592-bfb5-bcdcf7818e18
keywords:
- Advanced Systems Format (ASF), Aufzählen von senken
- ASF (Advanced Systems Format), Enumerieren von senken
- Advanced Systems Format (ASF), senken
- ASF (Advanced Systems Format), senken
- senken, auflisten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff35124a8c88108082544b270aa4d9813ff67ea9
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/21/2020
ms.locfileid: "103724030"
---
# <a name="enumerating-sinks"></a>Auflisten von senken

Dem Writer können viele senken zugeordnet werden. Sie können die senken, die dem Writer hinzugefügt wurden, mithilfe von [**iwmschreiteradvanced:: getsink count**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsinkcount) und [**iwmschreiteradvanced:: getsink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsink)auflisten.

Der Beispielcode in den [Fehlermeldungen aus einer Senke](getting-error-messages-from-a-sink.md) veranschaulicht die Senke-Enumeration.

> [!Note]  
> Beim Auflisten von senken wird die standardmäßige Datei Senke, die als Reaktion auf einen [**callmwriter:: setoutputfilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) erstellt wurde, zusammen mit allen anderen senken aufgelistet, die Sie hinzugefügt haben. Wenn Sie nur die standardmäßige Datei Senke verwenden, können Sie darauf zugreifen, indem Sie **getsink** für Senke-Index 0 aufrufen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwmschreiteradvanced-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**Arbeiten mit Writer-senken**](working-with-writer-sinks.md)
</dt> </dl>

 

 




