---
description: ASF-Skript Datenströme in DirectShow
ms.assetid: afef1b8b-4be2-48a1-b72a-b2e6342a5e84
title: ASF-Skript Datenströme in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da279c654a581bdb9eba23371882c5cbefbf5849
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103958017"
---
# <a name="asf-script-streams-in-directshow"></a>ASF-Skript Datenströme in DirectShow

Wenn der [WM-ASF-Reader](wm-asf-reader-filter.md) -Filter eine Datei erhält, die einen Datenstrom des Typs wmmediatype- \_ Skript enthält, wird eine entsprechende Ausgabe-PIN erstellt, die mit dem [internen rendererfilter des Skript Befehls](internal-script-command-renderer-filter.md) verbunden werden kann. Beim Aufruf von [**igraphbuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile)wird dieser Filter automatisch dem Diagramm hinzugefügt und verbunden. Wenn der Renderer des internen Skript Befehls ein Beispiel mit einem Skript Befehl empfängt, löst es ein [**EC- \_ OLE- \_ Ereignis**](ec-ole-event.md) Ereignis aus, dessen *LPARAM* das Skript enthält. Die Anwendung ist vollständig für die Behandlung dieses Ereignisses verantwortlich.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Lesen von ASF-Dateien in DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



