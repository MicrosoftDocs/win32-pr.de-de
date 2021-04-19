---
description: MF Trace ist ein Tool zum Erstellen von Ablauf Verfolgungs Protokollen für Media Foundation Anwendungen.
ms.assetid: 55b421c8-e87c-4dd2-8649-93832c93f999
title: MF-Ablauf Verfolgung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4a216f225141ceccf3f1357025dd069afa494d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367569"
---
# <a name="mftrace"></a>MF-Ablauf Verfolgung

MF Trace ist ein Tool zum Erstellen von Ablauf Verfolgungs Protokollen für Media Foundation Anwendungen.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Verwenden von MF Trace](using-mftrace.md)
-   [MF Trace-Schlüsselwörter](mftrace-keywords.md)
-   [MF-Ablauf Verfolgungs Konfigurationsdatei](mftrace-configuration-file.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------------|---------------------------------------------------------------------------------------|
| Mindestversion des SDK      | Microsoft Windows Software Development Kit (SDK) für Windows 7 und .NET Framework 4,0 |
| Mindestens Betriebssystem | Windows Vista                                                                         |



 

MF-Ablauf Verfolgung erfordert die folgenden DLLs, die ebenfalls im SDK bereitgestellt werden.

-   detoured.dll
-   mfdetours.dll

Das SDK bietet sowohl 32-Bit-als auch 64-Bit-Versionen von MF Trace. MF unterstützt nicht WOW64; Verwenden Sie zum Nachverfolgen eines 32-Bit-Prozesses, der unter 64-Bit-Windows ausgeführt wird, die 32-Bit-Version von mftrace.

SDK-Root auf 32-Bit-Systemen: \Program Files\Windows kits\10 SDK-Root auf 64 Bit System: \Programme (x86) \Windows kits\10 Sie finden mftrace unter <SDK-Root> \bin \<sdk-version> \<architecture>\mftrace.exe

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation Tools](media-foundation-tools.md)
</dt> </dl>

 

 



