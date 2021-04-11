---
description: Msitool. MAK ist ein Makefile, das Sie zum Erstellen von Tools und benutzerdefinierten Aktionen verwenden können.
ms.assetid: c05da933-7e0e-4fbb-a936-517902a363c4
title: Msitool. MAK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c3dad9fd65aaa880e9fdb38369843907104dea4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131308"
---
# <a name="msitoolmak"></a>Msitool. MAK

Msitool. MAK ist ein Makefile, das Sie zum Erstellen von Tools und benutzerdefinierten Aktionen verwenden können. Sie kann mit Visual C++ Version 4,0 oder höher verwendet werden. Weitere Informationen finden Sie in der Header Datei. Vor dem einschließen dieser Datei muss ein Satz von Werten definiert werden. In der Regel platzieren Entwickler diese am Anfang der CPP-Datei, die durch den C-Compiler übersprungen werden soll. Ebenso werden Ressourcen am Ende der CPP-Datei hinzugefügt. Weitere Informationen finden Sie in den Beispielen.

Vcbin kann für das Verzeichnis definiert werden, in dem die Visual C++ Tools gefunden werden, oder das Makefile verwendet msvcdir und msdevdir. Wenn diese nicht definiert sind, wird kein Speicherort angegeben, es wird davon ausgegangen, dass sich die Tools auf dem Pfad befinden. Ein Problem mit den Umgebungsvariablen in Visual C++ Version 5,0 besteht darin, dass der Linker keine Msdis100.dll finden kann, wenn sich beide nicht auf Ihrem Pfad befinden. Wenn Sie diese aus msdevdir in msvcdir kopieren, funktioniert Sie. Die andere Möglichkeit besteht darin, Msdis100.dll und Rc.exe und Rcdll.dll in msvcdir zu kopieren und vcbin auf diese festzulegen.

Dieses Tool ist nur in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)verfügbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwicklungs Tools für Windows Installer](windows-installer-development-tools.md)
</dt> <dt>

[Veröffentlichte Versionen, Tools und verteilbare Dateien](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



