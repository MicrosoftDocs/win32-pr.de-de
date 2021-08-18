---
title: JActiveX Command-Line Tool
description: Die JActiveX-Befehlszeilenanwendung ist eine Komponente von Visual J++ 6.0.
ms.assetid: b356eb85-5dd4-475b-8d53-8c13a84aa976
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae611e56c44b78398817cd0c78804d343fa97754f80fb3b036ea2705c801070f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992650"
---
# <a name="jactivex-command-line-tool"></a>JActiveX Command-Line Tool

Die JActiveX-Befehlszeilenanwendung ist eine Komponente von Visual J++ 6.0. Es liest die Typbibliothek eines Microsoft ActiveX-Steuerelements und generiert die entsprechenden Java-Quelldateien. Anschließend können Sie diese Quelldateien kompilieren und in Ihre Java-Anwendung importieren.

Führen Sie an der Eingabeaufforderung Aus, um Java-Quelldateien für ein COM-Objekt zu generieren:

**jactivex-Dateiname** 

dabei *ist filename* der Name der Datei, die die Typbibliothek enthält. Diese Datei kann eine der folgenden Dateierweiterungen haben: .tlb, .olb, .ocx, .dll oder .exe.

Weitere Informationen zu den optionalen Parametern, die Sie in JActiveX festlegen können, finden Sie in der Visual J++-Dokumentation, oder geben Sie die folgende Befehlszeile ein:

**jactivex /?**

> [!WARNING]
> Verwenden Sie keine Visual J++-Compiler vor Version 1.02.3920, um die dateien zu kompilieren, die von JActiveX.exe. Dies liegt daran, dass die generierten Quelldateien mit einem Compiler kompiliert werden @com-aware müssen. Nur Visual J++-Compiler, die höher als Version 1.02.3920 sind, sind @com-aware .

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersetzen in Java](translating-to-java.md)
</dt> </dl>

 

 




