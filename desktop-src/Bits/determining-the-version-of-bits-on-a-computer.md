---
title: Bestimmen der Bits-Version auf einem Computer
description: Um die Version von BITS auf dem Clientcomputer zu bestimmen, überprüfen Sie die Version QMgr.dll.
ms.assetid: b6057ae4-3bf0-4304-ae50-5da5e82a0bed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8caa2c501fd5f37d44becf11679debb1390aeeb9ee47bee02b43a97788493cd7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005310"
---
# <a name="determining-the-version-of-bits-on-a-computer"></a>Bestimmen der Bits-Version auf einem Computer

Um die Version von BITS auf dem Clientcomputer zu bestimmen, überprüfen Sie die Version QMgr.dll. So suchen Sie die Versionsnummer der DLL:

-   Suchen QMgr.dll in %windir% \\ System32.
-   Klicken Sie mit der rechten Maustaste QMgr.dll, und klicken Sie **auf Eigenschaften.**
-   Klicken Sie auf **die Registerkarte** Version.
-   Beachten Sie die Versionsnummer.

Sie können auch den folgenden PowerShell-Code verwenden, um die Version des .dll auf Ihrem System zu bestimmen:

`get-item "C:\Windows\System32\qmgr.dll" | Select-Object -ExpandProperty VersionInfo`

Wenn die DLL auch in %windir% \\ System32 Bits vorhanden \\ ist, wiederholen Sie die vorherigen Schritte. BITS verwendet die DLL mit der höheren Versionsnummer.

In der folgenden Tabelle sind die Versionen von BITS und die entsprechenden QMgr.dll dateiversionsnummern aufgeführt.



| BITS-Version | QMgr.dll der Dateiversionsnummer |
|--------------|------------------------------|
| BITS 10.1    | 7.8.xxxx.xxxx                |
| BITS 5.0     | 7.7.xxxx.xxxx                |
| BITS 4.0     | 7.5.xxxx.xxxx                |
| BITS 3.0     | 7.0.xxxx.xxxx                |
| BITS 2.5     | 6.7.xxxx.xxxx                |
| BITS 2.0     | 6.6.xxxx.xxxx                |
| BITS 1.5     | 6.5.xxxx.xxxx                |
| BITS 1.2     | 6.2.xxxx.xxxx                |
| BITS 1.0     | 6.0.xxxx.xxxx                |



 

Sie können auch die symbolischen Klassenbezeichner verwenden, um die Version von BITS zu bestimmen, die auf dem Computer registriert ist. In der folgenden Tabelle sind die Versionen von BITS und die entsprechenden symbolischen Klassenbezeichner aufgeführt. Die **CoCreateInstance-Funktion** gibt **REGDB \_ E \_ CLASSNOTREG** zurück, wenn die Klasse nicht registriert ist.



| BITS-Version  | Symbolischer Klassenbezeichner         |
|---------------|-----------------------------------|
| BITS 10.1     | CLSID \_ BackgroundCopyManager10 \_ 1 |
| BITS 5.0      | CLSID \_ BackgroundCopyManager5 \_ 0  |
| BITS 4.0      | CLSID \_ BackgroundCopyManager4 \_ 0  |
| BITS 3.0      | CLSID \_ BackgroundCopyManager3 \_ 0  |
| BITS 2.5      | CLSID \_ BackgroundCopyManager2 \_ 5  |
| BITS 2.0      | CLSID \_ BackgroundCopyManager2 \_ 0  |
| BITS 1.5      | CLSID \_ BackgroundCopyManager1 \_ 5  |
| BITS 1.2, 1.0 | CLSID \_ BackgroundCopyManager      |



 

 

 




