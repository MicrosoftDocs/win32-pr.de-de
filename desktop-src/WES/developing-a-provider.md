---
title: Entwickeln eines Anbieters
description: Zum Schreiben der Ereignisse, die Sie in Ihrem Manifest definieren, verwenden Sie die Funktionen, die in der ETW-API (Ereignisablaufverfolgung) enthalten sind. Weitere Informationen zum Schreiben eines Anbieters finden Sie unter Bereitstellen von Ereignissen.
ms.assetid: 23de19c4-5f8d-4faa-acd9-fe6208ca17a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bdcbf17113eb926aba245f270b84e7ab50bf3072e15a9a7752b8828296a00a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117937185"
---
# <a name="developing-a-provider"></a>Entwickeln eines Anbieters

Zum Schreiben der Ereignisse, die Sie in Ihrem Manifest definieren, verwenden Sie die Funktionen, die in der ETW-API [(Ereignisablaufverfolgung)](/windows/desktop/ETW/event-tracing-portal) enthalten sind. Weitere Informationen zum Schreiben eines Anbieters finden Sie unter [Bereitstellen von Ereignissen.](/windows/desktop/ETW/providing-events)

Verwenden Sie nach dem Schreiben des Anbieters das WevtUtil.exe, um den Anbieter und das Schema zu registrieren. Weitere Informationen zur Verwendung von WevtUtil finden Sie unter [Windows Event Log Tools](windows-event-log-tools.md). Im Folgenden wird gezeigt, wie Sie WevtUtil verwenden, um einen Anbieter zu registrieren und die Registrierung zu entfernen.


```cmd
wevtutil im provider.man

wevtutil um provider.man
```