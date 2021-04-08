---
title: Bestimmen der Bits-Version auf einem Computer
description: Überprüfen Sie die Version von QMgr.dll, um die Bits-Version auf dem Client Computer zu ermitteln.
ms.assetid: b6057ae4-3bf0-4304-ae50-5da5e82a0bed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c94e151608511ec59e52befdef6e4f63e44476e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707860"
---
# <a name="determining-the-version-of-bits-on-a-computer"></a>Bestimmen der Bits-Version auf einem Computer

Überprüfen Sie die Version von QMgr.dll, um die Bits-Version auf dem Client Computer zu ermitteln. So ermitteln Sie die Versionsnummer der dll:

-   Suchen Sie in% windir% \\ system32 nach QMgr.dll.
-   Klicken Sie mit der rechten Maustaste auf QMgr.dll und dann auf **Eigenschaften**
-   Klicken Sie auf die Registerkarte **Version** .
-   Beachten Sie die Versionsnummer.

Sie können auch den folgenden PowerShell-Code verwenden, um die Version der DLL-Datei auf Ihrem System zu ermitteln:

`get-item "C:\Windows\System32\qmgr.dll" | Select-Object -ExpandProperty VersionInfo`

Wenn die dll auch in% windir% \\ system32 \\ Bits vorhanden ist, wiederholen Sie die vorherigen Schritte. Bits verwendet die DLL mit der höheren Versionsnummer.

In der folgenden Tabelle sind die Versionen von Bits und ihre entsprechenden QMgr.dll Dateiversionsnummern aufgeführt.



| BITS-Version | Versionsnummer der QMgr.dll Datei |
|--------------|------------------------------|
| Bits 10,1    | 7.8. xxxx. xxxx                |
| Bits 5,0     | 7.7. xxxx. xxxx                |
| Bits 4,0     | 7.5. xxxx. xxxx                |
| Bits 3,0     | 7.0. xxxx. xxxx                |
| BITS 2.5     | 6.7. xxxx. xxxx                |
| BITS 2,0     | 6.6. xxxx. xxxx                |
| Bits 1,5     | 6.5. xxxx. xxxx                |
| Bits 1,2     | 6.2. xxxx. xxxx                |
| Bits 1,0     | 6.0. xxxx. xxxx                |



 

Mit den symbolischen Klassen Bezeichners können Sie auch die Version von Bits ermitteln, die auf dem Computer registriert ist. In der folgenden Tabelle werden die Versionen von Bits und ihre entsprechenden symbolischen Klassen Bezeichner aufgelistet. Die **cokreateinstance** -Funktion gibt **RegDB \_ E \_ classnotreg** zurück, wenn die Klasse nicht registriert ist.



| BITS-Version  | Symbolischer Klassen Bezeichner         |
|---------------|-----------------------------------|
| Bits 10,1     | CLSID \_ BackgroundCopyManager10 \_ 1 |
| Bits 5,0      | CLSID \_ BackgroundCopyManager5 \_ 0  |
| Bits 4,0      | CLSID \_ BackgroundCopyManager4 \_ 0  |
| Bits 3,0      | CLSID \_ BackgroundCopyManager3 \_ 0  |
| BITS 2.5      | CLSID \_ BackgroundCopyManager2 \_ 5  |
| BITS 2,0      | CLSID \_ BackgroundCopyManager2 \_ 0  |
| Bits 1,5      | CLSID \_ BackgroundCopyManager1 \_ 5  |
| Bits 1,2, 1,0 | CLSID- \_ backgroundcopymanager      |



 

 

 




