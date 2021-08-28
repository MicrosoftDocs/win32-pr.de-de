---
description: MFTrace ist ein Tool zum Generieren von Ablaufverfolgungsprotokollen für Media Foundation Anwendungen.
ms.assetid: 55b421c8-e87c-4dd2-8649-93832c93f999
title: Mftrace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 542ac9325b33fc8f1a76394d203dbf1d27919bd6
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885231"
---
# <a name="mftrace"></a>Mftrace

MFTrace ist ein Tool zum Generieren von Ablaufverfolgungsprotokollen für Media Foundation Anwendungen.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Verwenden von MFTrace](using-mftrace.md)
-   [MFTrace-Schlüsselwörter](mftrace-keywords.md)
-   [MFTrace-Konfigurationsdatei](mftrace-configuration-file.md)

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------------|---------------------------------------------------------------------------------------|
| Mindestversion des SDK      | Microsoft Windows Software Development Kit (SDK) für Windows 7 und .NET Framework 4.0 |
| Mindestbetriebssystem | Windows Vista                                                                         |



 

MFTrace erfordert die folgenden DLLs, die auch im SDK bereitgestellt werden.

-   detoured.dll
-   mfdetours.dll

Das SDK stellt sowohl 32-Bit- als auch 64-Bit-Versionen von MFTrace bereit. MFTrace unterstützt WOW64 nicht. Verwenden Sie die 32-Bit-Version von MFTrace, um einen 32-Bit-Prozess zu verfolgen, der auf 64-Bit-Windows ausgeführt wird.

sdk-root auf 32-Bit-Systemen: \Programme\Windows Kits\10 sdk-root auf 64-Bit-System: \Programme (x86)\Windows Kits\10 Sie finden mftrace unter &lt; sdk-root &gt; \bin \<sdk-version> \<architecture>\mftrace.exe

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation Tools](media-foundation-tools.md)
</dt> </dl>

 

 



