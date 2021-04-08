---
description: Die GetFileSize-Funktion Ruft die Größe einer Datei ab.
ms.assetid: 4d3a3925-72e8-4350-b46d-e2c25791e862
title: Bestimmen der Größe einer Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19f7205c47fe25b223dbcc12322516ff2b162fcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959879"
---
# <a name="determining-the-size-of-a-file"></a>Bestimmen der Größe einer Datei

Die [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) -Funktion Ruft die Größe einer Datei ab.

Da die NTFS-Dateisystem Implementierung von Dateien mehrere Datenströme innerhalb einer Datei zulässt, muss jede Anwendung, die Sie für den Zugriff auf Dateien schreiben, die Möglichkeit berücksichtigen, dass der Ersteller der Datei mehrere Datenströme in die Datei einschließen kann. Wenn in einer Datei nicht auf mehrere Datenströme geprüft wird, kann die Anwendung die Gesamtgröße der Datei unterschätzen, unter anderem Fehler.

 

 



