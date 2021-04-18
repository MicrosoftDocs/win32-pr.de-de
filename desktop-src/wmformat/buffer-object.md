---
title: Buffer-Objekt
description: Buffer-Objekt
ms.assetid: 0812261c-698c-4071-929c-4363a16dd5a8
keywords:
- Windows Media-Format-SDK, Puffer Objekte
- Advanced Systems Format (ASF), Buffer Objects
- ASF (Advanced Systems Format), Buffer Objects
- Objekte, Puffer Objekte
- Puffer Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8a9a3c6acfa0b0780b07f2853f60fdd68d0eaf
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/21/2020
ms.locfileid: "106339051"
---
# <a name="buffer-object"></a>Buffer-Objekt

Ein Puffer Objekt wird verwendet, um Beispiele zu speichern und diese zwischen den Objekten des Windows Media Format SDK und ihrer Anwendung zu übermitteln. Wenn Sie eine Datei schreiben, übergeben Sie die Eingabe Beispiele mithilfe von Puffer Objekten an den Writer. Beim Lesen einer Datei stellt das Reader-Objekt oder das synchrone Reader-Objekt der Anwendung in Puffer Objekten Beispiele zur Verfügung.

Zum Schreiben von Beispielen in eine Datei können Sie ein Puffer Objekt mithilfe der Methode [**iwmwriter:: Zuweisung**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample) erstellen. Zum Lesen von Beispielen erstellen sowohl das Reader-Objekt als auch das synchrone Reader-Objekt Puffer Objekte intern. Wenn Sie sich für entscheiden, können Sie mithilfe von [**iwmreaderallocatorex:: allocateforoutputex**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex) oder [**iwmreaderallocatorex:: allocateforstreamex**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex)eigene Puffer Objekte für das Lesen von Dateien zuordnen.

Die folgenden Schnittstellen werden von jedem Puffer Objekt unterstützt.



| Schnittstelle                          | BESCHREIBUNG                                                          |
|------------------------------------|----------------------------------------------------------------------|
| [**Inssbuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)   | Steuert und ermöglicht den Zugriff auf den Puffer.                          |
| [**INSSBuffer2**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer2) | Nicht implementiert.                                                     |
| [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) | Unterstützt Puffer Eigenschaften, die für dateneinheits Erweiterungen verwendet werden. |
| [**INSSBuffer4**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4) | Listet Puffer Eigenschaften auf.                                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Objekte**](objects.md)
</dt> </dl>

 

 




