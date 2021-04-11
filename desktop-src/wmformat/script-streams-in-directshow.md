---
title: Skripterstellung für Datenströme in DirectShow
description: Skripterstellung für Datenströme in DirectShow
ms.assetid: ad467897-1d25-4bb0-a0ec-84560fe7063b
keywords:
- Windows Media-Format-SDK, DirectShow
- Windows Media-Format-SDK, Skript Datenströme
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- Advanced Systems Format (ASF), Skript Datenströme
- ASF (Advanced Systems Format), Skript Datenströme
- DirectShow, Skript Datenströme
- Skript Datenströme, DirectShow
- Streams, Skript Datenströme in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09f08fab54dbdfe61dcc2ce78790cd471985cdeb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311159"
---
# <a name="script-streams-in-directshow"></a>Skripterstellung für Datenströme in DirectShow

Wenn der WM-ASF-Reader-Filter eine Datei erhält, die einen Datenstrom des Typs wmmediatype- \_ Skript enthält, erstellt er eine Ausgabepin für diese, die mit dem Editor für den Renderer des internen Skript Befehls von DirectShow verbunden werden kann. Beim Aufruf von **igraphbuilder:: RenderFile** wird dieser Filter automatisch dem Diagramm hinzugefügt und verbunden. Wenn der Renderer des internen Skript Befehls ein Beispiel mit einem Skript Befehl empfängt, löst es ein **EC- \_ OLE- \_ Ereignis** aus, dessen **LPARAM** das Skript enthält. Die Anwendung ist vollständig für die Behandlung dieses Ereignisses verantwortlich. Weitere Informationen zu **EC- \_ OLE- \_ Ereignissen** finden Sie in der DirectShow-SDK-Dokumentation.

 

 




