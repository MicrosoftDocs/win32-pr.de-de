---
description: TopoEdit-Module
ms.assetid: f3da2d13-a8ad-4db0-9d18-e94857f0abc7
title: TopoEdit-Module
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc95848a533ba67599c114917ebe502f42a4fe859df9c1ac6bf5acfc40bb393c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118057715"
---
# <a name="topoedit-modules"></a>TopoEdit-Module

Das TopoEdit-Tool wird mit dem Windows SDK für Windows Server 2008 und höher bereitgestellt. Das Tool erfordert Windows Vista oder höher.

Die TopoEdit-Module befinden sich im Ordner Bin des SDK. Diese Module sind:

-   TopoEdit.exe – Ausführbare Anwendung
-   TEDUTIL.dll – Erweiterungs-DLL

Die SDK-Installation registriert die DLL. Wenn dies jedoch fehlschlägt, führen Sie an einer Eingabeaufforderung Folgendes aus.


```C++
Regsvr32 <Install path>\Microsoft SDKs\Windows\v6.0\Bin\TEDUTIL.dll
```



Der Quellcode für TopoEdit wird auch als Beispiel im Windows SDK bereitgestellt. Sie befindet sich im folgenden Verzeichnis:

<samples root>\\Multimedia \\ Media Foundation \\ TopoEdit

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einführung in TopoEdit](introduction-to-topoedit.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



