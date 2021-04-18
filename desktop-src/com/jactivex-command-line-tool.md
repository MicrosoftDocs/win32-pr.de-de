---
title: JActiveX-Command-Line Tool
description: Die Befehlszeilen Anwendung "JActiveX" ist eine Komponente von Visual J++ 6,0.
ms.assetid: b356eb85-5dd4-475b-8d53-8c13a84aa976
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9975e060a3967f927440111719045378aa812f16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337185"
---
# <a name="jactivex-command-line-tool"></a>JActiveX-Command-Line Tool

Die Befehlszeilen Anwendung "JActiveX" ist eine Komponente von Visual J++ 6,0. Die Typbibliothek eines Microsoft ActiveX-Steuer Elements wird gelesen, und die entsprechenden Java-Quelldateien werden generiert. Anschließend können Sie diese Quelldateien kompilieren und in Ihre Java-Anwendung importieren.

Führen Sie zum Generieren von Java-Quelldateien für ein COM-Objekt an der Eingabeaufforderung Folgendes aus:

**JActiveX** - *Dateiname*

wobei *filename* der Name der Datei ist, die die Typbibliothek enthält. Diese Datei kann eine der folgenden Dateinamen Erweiterungen aufweisen: ". tlb", ". olb", ". ocx", ". dll" oder ". exe".

Weitere Informationen zu den optionalen Parametern, die Sie in JActiveX festlegen können, finden Sie in der Visual J++-Dokumentation, oder geben Sie die folgende Befehlszeile ein:

**JActiveX/?**

> [!WARNING]
> Verwenden Sie Visual J++-Compiler nicht vor Version 1.02.3920, um die von JActiveX.exe generierten Dateien zu kompilieren. Dies liegt daran, dass die generierten Quelldateien mit einem Compiler kompiliert werden müssen @com-aware . Nur Visual J++-Compiler, die später als Version 1.02.3920 sind, sind @com-aware .

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersetzen in Java](translating-to-java.md)
</dt> </dl>

 

 




