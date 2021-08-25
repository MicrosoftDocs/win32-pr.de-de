---
title: Aufzählen von Senken
description: Aufzählen von Senken
ms.assetid: 1b635cd8-6bdd-4592-bfb5-bcdcf7818e18
keywords:
- Advanced Systems Format (ASF), Aufzählen von Senken
- ASF (Advanced Systems Format), Aufzählen von Senken
- Advanced Systems Format (ASF),sinks
- ASF (Advanced Systems Format), sinks
- sinks,enumerating
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b51b46f3efdf95902b1ca5b359227da845292c4b0f23dbf0bd52039fba151cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118029071"
---
# <a name="enumerating-sinks"></a>Aufzählen von Senken

Dem Writer können viele Senken zugeordnet sein. Sie können die Senken aufzählen, die dem Writer hinzugefügt wurden, indem Sie [**IWMWriterAdvanced::GetSinkCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsinkcount) und [**IWMWriterAdvanced::GetSink verwenden.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsink)

Der Beispielcode in Getting Error Messages from a Sink (Abrufen von Fehlermeldungen aus einer [Senke)](getting-error-messages-from-a-sink.md) veranschaulicht die Senkenenumeration.

> [!Note]  
> Beim Aufzählen von Senken wird die Standarddateisenke, die als Reaktion auf einen Aufruf von [**IWMWriter::SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) erstellt wurde, zusammen mit allen anderen hinzugefügten Senken aufzählt. Wenn Sie nur die Standarddateisenke verwenden, können Sie darauf zugreifen, indem Sie **GetSink für** senkenden Index 0 aufrufen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWMWriterAdvanced-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**Arbeiten mit Writer-Senken**](working-with-writer-sinks.md)
</dt> </dl>

 

 




