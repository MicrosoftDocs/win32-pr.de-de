---
title: Erstellen von temporären Streams
description: Erstellen von temporären Streams
ms.assetid: 8fe75ae1-0111-4b02-a00d-1ef2ca462452
keywords:
- AVIStreamCreate-Funktion
- AVIStreamRelease-Funktion
- AVIMakeCompressedStream-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c33ce8d4ec6fd88a7283588d35955432cbe01a4855565928dca83d40afa8b64f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785700"
---
# <a name="creating-temporary-streams"></a>Erstellen von temporären Streams

Temporäre Streams können auf verschiedene Weise von Vorteil sein. Sie können einen temporären Stream als Arbeitsstream verwenden, z. B. beim Ändern des Streamformats. Sie können auch einen temporären Datenstrom erstellen, der Teile anderer Streams, die kopiert wurden, zu halten.

Sie können einen Stream im Arbeitsspeicher erstellen, der einer Datei nicht zugeordnet ist, indem Sie die [**FUNKTION AVIStreamCreate**](/windows/desktop/api/Vfw/nf-vfw-avistreamcreate) verwenden. Diese Funktion gibt die Adresse der Schnittstelle an den neuen Stream an einem angegebenen Speicherort zurück und wird intern von anderen Funktionen verwendet, die temporäre Streams erstellen.

Sie können einen komprimierten Stream aus einem nicht komprimierten Stream mithilfe der [**AVIMakeCompressedStream-Funktion**](/windows/desktop/api/Vfw/nf-vfw-avimakecompressedstream) erstellen. Sie identifizieren den zu komprimierenden Stream, die Komprimierungsmethode und die Komprimierungsoptionen sowie den Handler für den neuen Stream.

Wenn Sie mit der Verwendung eines Streams fertig sind, der mit **AVIStreamCreate** oder **AVIMakeCompressedStream** erstellt wurde, schließen Sie den Stream mithilfe der [**FUNKTION AVIStreamRelease.**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) **AVIStreamRelease gibt** die Ressourcen frei, die der temporäre Stream verwendet.

 

 




