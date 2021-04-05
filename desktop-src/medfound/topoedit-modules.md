---
description: Topoedit-Module
ms.assetid: f3da2d13-a8ad-4db0-9d18-e94857f0abc7
title: Topoedit-Module
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728f39edace5974d390746173308361b595c3b40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042043"
---
# <a name="topoedit-modules"></a>Topoedit-Module

Das Tool topoedit wird mit dem Windows SDK für Windows Server 2008 und höher bereitgestellt. Das Tool erfordert Windows Vista oder höher.

Die topoedit-Module befinden sich im Ordner "bin" des SDK. Diese Module sind:

-   TopoEdit.exe – ausführbare Datei der Anwendung
-   TEDUTIL.dll –-Erweiterungs-DLL

Die SDK-Installation registriert die dll. Wenn dies jedoch nicht möglich ist, führen Sie an einer Eingabeaufforderung Folgendes aus.


```C++
Regsvr32 <Install path>\Microsoft SDKs\Windows\v6.0\Bin\TEDUTIL.dll
```



Quellcode für topoedit wird auch als Beispiel in der Windows SDK bereitgestellt. Sie befindet sich im folgenden Verzeichnis:

<samples root>\\Multimedia- \\ Media Foundation \\ topoedit

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einführung in topoedit](introduction-to-topoedit.md)
</dt> <dt>

[Topoedit](topoedit.md)
</dt> </dl>

 

 



