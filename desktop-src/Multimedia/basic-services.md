---
title: Basic Services
description: Basic Services
ms.assetid: 7b77ed5d-0bd9-4926-b73f-afc7070fe314
keywords:
- Multimediadatei-E/A, Grundlegende Dienste
- Datei-E/A, Grundlegende Dienste
- Eingabe und Ausgabe (E/A), grundlegende Dienste
- E/A (Eingabe und Ausgabe), grundlegende Dienste
- Einfache E/A
- mmioOpen-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3ef4ea778ad0c84137aa75d36f46dc30310180c69416a1240078f01e53d6931
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145123"
---
# <a name="basic-services"></a>Basic Services

Die Verwendung der grundlegenden E/A-Dienste ähnelt der Verwendung der Laufzeitdatei-E/A-Dienste der C-Laufzeitbibliothek. Dateien müssen geöffnet werden, bevor sie gelesen oder geschrieben werden können. Nach dem Lesen oder Schreiben muss die Datei geschlossen werden. Sie können auch den aktuellen Lese- oder Schreibspeicherort in einer geöffneten Datei ändern.

Bevor Sie E/A-Vorgänge für eine Datei starten, müssen Sie die Datei mithilfe der [**mmioOpen-Funktion**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) öffnen. Diese Funktion gibt ein Dateihand handle vom Typ **HMMIO zurück.** Sie können dieses Dateihand handle verwenden, um die geöffnete Datei beim Aufrufen anderer Datei-E/A-Funktionen zu identifizieren.

> [!Note]  
> Ein **HMMIO-Dateihand** handle ist kein Standarddateihand handle. Verwenden Sie keine **HMMIO-Dateihandles** mit Win32- oder C-Laufzeitdatei-E/A-Funktionen.

 

Wenn Sie [**mmioOpen verwenden,**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) um eine Datei zu öffnen, verwenden Sie ein Flag, um anzugeben, ob Sie sie zum Lesen, Schreiben oder beides öffnen. Sie können auch Flags angeben, mit denen Sie eine Datei erstellen oder löschen können. Verwenden Sie [**die mmioClose-Funktion,**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) um eine Datei zu schließen, wenn Sie mit dem Lesen oder Schreiben fertig sind.

Sie können Dateien mithilfe der [**Funktionen mmioRead**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread) bzw. [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) lesen und schreiben. Der nächste Lese- oder Schreibvorgang erfolgt an der aktuellen Dateiposition oder dem Dateizeiger in einer Datei. Die aktuelle Dateiposition wird jedes Mal erweitert, wenn eine Datei gelesen oder geschrieben wird.

Sie können die aktuelle Dateiposition auch mithilfe der [**mmioSeek-Funktion**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) ändern. Sie sollten sicherstellen, dass Sie einen gültigen Speicherort in einer Datei angeben. Wenn Sie einen ungültigen Speicherort angeben, z. B. hinter dem Ende der Datei, gibt **mmioSeek** möglicherweise keinen Fehler zurück, aber nachfolgende E/A-Vorgänge können fehlschlagen.

Es gibt Flags, die Sie mit der **mmioOpen-Funktion für** Vorgänge verwenden können, die über einfache Datei-E/A-Vorgänge hinausgehen. Wenn Sie beispielsweise eine [**MMIOINFO-Struktur**](/previous-versions//dd757322(v=vs.85)) angeben, können Sie Speicherdateien öffnen, eine benutzerdefinierte E/A-Prozedur angeben oder einen Puffer für gepufferte E/A-Daten angeben.

 

 