---
title: Verwenden der Zwischenablage mit AVI-Dateien
description: Verwenden der Zwischenablage mit AVI-Dateien
ms.assetid: 76ef7cc9-9afd-462a-b9fe-2b62f8113a9a
keywords:
- AVIPutFileOnClipboard-Funktion
- AVIGetFromClipboard-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 579f7eeed3b5b7397e248bb1c9090bc086cb715c591ec436af5de7d885551c14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687840"
---
# <a name="using-the-clipboard-with-avi-files"></a>Verwenden der Zwischenablage mit AVI-Dateien

Die Zwischenablage bietet praktischen temporären Speicher, den eine Anwendung zum Kopieren oder Übertragen von AVI-Dateien verwenden kann. AVIFile enthält Zwischenablagefunktionen, die Sie mit Datenträger- oder Arbeitsspeicherdateien verwenden können.

Sie können eine Datei mithilfe der [**FUNKTION AVIPutFileOnClipboard**](/windows/desktop/api/Vfw/nf-vfw-aviputfileonclipboard) in die Zwischenablage kopieren. Verwenden Sie die [**FUNKTION AVIGetFromClipboard,**](/windows/desktop/api/Vfw/nf-vfw-avigetfromclipboard) um eine Datei in der Zwischenablage in den Arbeitsspeicher oder datenträger zu schreiben.

Sie können eine Datei mithilfe der [**AVIClearClipboard-Funktion**](/windows/desktop/api/Vfw/nf-vfw-aviclearclipboard) aus der Zwischenablage löschen. Diese Funktion löscht keine anderen Informationstypen, z. B. Text, aus der Zwischenablage. Wenn Sie in Ihrer Anwendung Zwischenablagefunktionen verwenden, löschen Sie die Zwischenablage mit **AVIClearClipboard,** bevor Sie die Anwendung schließen oder die Datei in der Zwischenablage schließen. Sie können **AVIClearClipboard** in Ihrer Anwendung unabhängig davon aufrufen, ob **AVIPutFileOnClipboard** verwendet wurde oder nicht.

> [!Note]  
> Wenn Ihre Anwendung eine Datei in die Zwischenablage kopiert und die Datei Datenstromdaten enthält, die sich möglicherweise ändern, können Sie mithilfe der [**AVIMakeFileFromStreams-Funktion**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) eine Speicherdatei geklonter Datenströme erstellen. Sie können die Datei dann in der Zwischenablage platzieren und dann die ursprüngliche Datei freigeben, ohne sie für ungültig zu erklären.

 

 

 




