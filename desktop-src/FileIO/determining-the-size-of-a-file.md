---
description: Die GetFileSize-Funktion ruft die Größe einer Datei ab.
ms.assetid: 4d3a3925-72e8-4350-b46d-e2c25791e862
title: Bestimmen der Größe einer Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cdf4185d0bb695d73dc3afd03bb1ee7d6fe95cf606960fbdc41c4ce0b33b732
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150613"
---
# <a name="determining-the-size-of-a-file"></a>Bestimmen der Größe einer Datei

Die [**GetFileSize-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) ruft die Größe einer Datei ab.

Da die NTFS-Dateisystemimplementierung von Dateien mehrere Datenströme innerhalb einer Datei zulässt, muss jede Anwendung, die auf Dateien zugreift, die Möglichkeit berücksichtigen, dass der Ersteller der Datei mehrere Streams in die Datei einschließen kann. Wenn in einer Datei nicht nach mehreren Datenströmen gesucht wird, kann die Anwendung die Gesamtgröße der Datei unter anderem durch Fehler abschätzen.

 

 



