---
title: Erstellen temporärer Streams
description: Erstellen temporärer Streams
ms.assetid: 8fe75ae1-0111-4b02-a00d-1ef2ca462452
keywords:
- Avistreamcreate-Funktion
- Avistreamrelease-Funktion
- Avimakecompressedstream-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209259f46e25275094dcd1eb5eeddd4f336ee906
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471196"
---
# <a name="creating-temporary-streams"></a>Erstellen temporärer Streams

Temporäre Datenströme können auf verschiedene Arten von Vorteil sein. Sie können einen temporären Stream als einen Arbeitsdaten Strom verwenden, z. b. Wenn Sie das Streamformat ändern. Oder Sie können einen temporären Stream erstellen, um Teile anderer Streams zu speichern, die kopiert wurden.

Sie können einen Stream im Speicher erstellen, der keiner Datei zugeordnet ist, indem Sie die [**avistreamcreate**](/windows/desktop/api/Vfw/nf-vfw-avistreamcreate) -Funktion verwenden. Diese Funktion gibt die Adresse der Schnittstelle an den neuen Stream an einem angegebenen Speicherort zurück und wird intern von anderen Funktionen verwendet, die temporäre Datenströme erstellen.

Mithilfe der [**avimakecompressedstream**](/windows/desktop/api/Vfw/nf-vfw-avimakecompressedstream) -Funktion können Sie einen komprimierten Stream aus einem unkomprimierten Datenstrom erstellen. Sie identifizieren den zu Komprimier erenden Stream, die Komprimierungs Methode und Komprimierungs Optionen sowie den Handler für den neuen Stream.

Wenn Sie einen Stream, der mit **avistreamcreate** oder **avimakecompressedstream** erstellt wurde, nicht mehr verwenden, schließen Sie den Datenstrom mithilfe der [**avistreamrelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) -Funktion. **Avistreamrelease** gibt die Ressourcen frei, die für den temporären Stream verwendet werden.

 

 




