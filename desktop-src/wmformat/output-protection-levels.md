---
title: Ausgabeschutzebenen
description: Ausgabeschutzebenen
ms.assetid: 89a9fc13-5ade-4a33-8304-05a2ec999fc1
keywords:
- Windows Medienformat-SDK, Ausgabeschutzebenen (OPL)
- Digital Rights Management (DRM), Ausgabeschutzebenen (OPL)
- DRM (Digital Rights Management), Ausgabeschutzebenen (OPL)
- Ausgabeschutzebenen (Output Protection Levels, OPL)
- OPL (Ausgabeschutzebenen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f76804b70df5db085484cb769e4c60f046aedadd9cd177480de90b8a3eb5ad6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707460"
---
# <a name="output-protection-levels"></a>Ausgabeschutzebenen

Ausgabeschutzebenen (Output Protection Levels, OPLs) sind numerische Bewertungen, die verschiedenen Technologien zugeordnet sind, die digitale Medieninhalte empfangen. Welche Ebene eine Technologie unterstützt, hängt davon ab, wie sicher sie ist. Das opl-System, das in Windows Media DRM 10 eingeführt wurde, ermöglicht die Erstellung von Lizenzen mit mehr Flexibilität als in früheren Versionen. Sie können die minimalen OPLs angeben, die für die Wiedergabe und das Kopieren erforderlich sind. Darüber hinaus können Sie Ausnahmen für die minimale OPL angeben, um eine Technologie zuzulassen, die nicht hoch genug bewertet wird, oder um eine Technologie mit einer OPL, die den Mindestwert überschreitet, nicht zuzulassen.

Durch die Angabe von Einschränkungen für Lizenzen mit opls muss ein Inhaltsbesitzer nur zwei Aktionen verwenden (Kopieren und Wiedergeben), wobei in früheren Versionen separate Aktionen für die verschiedenen Arten von Geräten definiert wurden, die zum Kopieren unterstützt werden (SDMI, Nicht-SDMI und Red Book-Audio-CD).

**Hinweis** DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Digital Rights Management Features**](digital-rights-management-features.md)
</dt> <dt>

[**Arbeiten mit Ausgabeschutzebenen**](working-with-output-protection-levels.md)
</dt> </dl>

 

 




