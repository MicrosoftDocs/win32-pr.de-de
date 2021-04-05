---
title: Verwenden der Zwischenablage mit AVI-Dateien
description: Verwenden der Zwischenablage mit AVI-Dateien
ms.assetid: 76ef7cc9-9afd-462a-b9fe-2b62f8113a9a
keywords:
- Aviputfleonclipboard-Funktion
- Avigetfromclipboard-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe46f463f22aa2d015d4ffd8496eb95c37053a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710620"
---
# <a name="using-the-clipboard-with-avi-files"></a>Verwenden der Zwischenablage mit AVI-Dateien

Die Zwischenablage bietet einen bequemen temporären Speicher, der von einer Anwendung zum Kopieren oder übertragen von AVI-Dateien verwendet werden kann. Avifile umfasst Zwischenablage Funktionen, die Sie mit Datenträger-oder Arbeitsspeicher Dateien verwenden können.

Mithilfe der [**aviputfleonclipboard**](/windows/desktop/api/Vfw/nf-vfw-aviputfileonclipboard) -Funktion können Sie eine Datei in die Zwischenablage kopieren. Um eine Datei in der Zwischenablage in den Arbeitsspeicher oder Datenträger zu schreiben, verwenden Sie die [**avigetfromclipboard**](/windows/desktop/api/Vfw/nf-vfw-avigetfromclipboard) -Funktion.

Mithilfe der [**aviclearclipboard**](/windows/desktop/api/Vfw/nf-vfw-aviclearclipboard) -Funktion können Sie eine Datei aus der Zwischenablage löschen. Diese Funktion löscht keine anderen Arten von Informationen, z. b. Text, aus der Zwischenablage. Wenn Sie in der Anwendung Zwischenablage Funktionen verwenden, löschen Sie die Zwischenablage mit **aviclearclipboard** , bevor Sie die Anwendung schließen oder die Datei in der Zwischenablage schließen. Sie können **aviclearclipboard** in Ihrer Anwendung aufrufen, unabhängig davon, ob **aviputfleonclipboard** verwendet wurde.

> [!Note]  
> Wenn Ihre Anwendung eine Datei in die Zwischenablage kopiert und die Datei Streamdaten enthält, die sich möglicherweise ändern, können Sie mithilfe der [**avimakefilefromstreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) -Funktion eine Speicherdatei mit geklonten Streams erstellen. Anschließend können Sie die Datei in der Zwischenablage platzieren und die ursprüngliche Datei freigeben, ohne sie ungültig zu machen.

 

 

 




