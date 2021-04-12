---
title: Grundlegende Dienste
description: Grundlegende Dienste
ms.assetid: 7b77ed5d-0bd9-4926-b73f-afc7070fe314
keywords:
- Multimedia-Datei-e/a, grundlegende Dienste
- Datei-e/a, grundlegende Dienste
- Eingabe und Ausgabe (e/a), grundlegende Dienste
- E/a (Eingabe und Ausgabe), grundlegende Dienste
- grundlegende e/a
- mmioopen-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 688dc6b96c612d94524758acce5d8c742fc13a36
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390278"
---
# <a name="basic-services"></a>Grundlegende Dienste

Die Verwendung der grundlegenden e/a-Dienste ähnelt der Verwendung der Lauf Zeit Datei-e/a-Dienste der C-Lauf Zeit Bibliothek. Dateien müssen geöffnet werden, bevor Sie gelesen oder geschrieben werden können. Nach dem Lesen oder schreiben muss die Datei geschlossen werden. Sie können auch den aktuellen Lese-oder Schreib Speicherort innerhalb einer geöffneten Datei ändern.

Bevor Sie mit e/a-Vorgängen in einer Datei beginnen, müssen Sie die Datei mit der [**mmioopen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) -Funktion öffnen. Diese Funktion gibt ein Datei Handle vom Typ **hmmio** zurück. Sie können dieses Datei Handle verwenden, um die geöffnete Datei zu identifizieren, wenn Sie andere Datei-e/a-Funktionen aufrufen.

> [!Note]  
> Ein **hmmio** -Datei Handle ist kein Standarddatei handle. Verwenden Sie keine **hmmio** -Datei Handles mit Win32-oder C-Lauf Zeit Datei-e/a-Funktionen.

 

Wenn Sie [**mmioopen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) verwenden, um eine Datei zu öffnen, verwenden Sie ein Flag, um anzugeben, ob Sie es zum Lesen, schreiben oder beides öffnen. Sie können auch Flags angeben, die es Ihnen ermöglichen, eine Datei zu erstellen oder zu löschen. Verwenden Sie die Funktion " [**mmioclose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) ", um eine Datei zu schließen, wenn Sie das Lesen oder schreiben in Sie abgeschlossen haben.

Sie können Dateien mit den Funktionen [**mmioread**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread) und [**mmiowrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) lesen und schreiben. Der nächste Lese-oder Schreibvorgang erfolgt an der aktuellen Dateiposition oder dem Dateizeiger in einer Datei. Die aktuelle Dateiposition wird immer dann erweitert, wenn eine Datei gelesen oder geschrieben wird.

Sie können auch die aktuelle Dateiposition ändern, indem Sie die [**mmioseek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) -Funktion verwenden. Stellen Sie sicher, dass Sie einen gültigen Speicherort in einer Datei angeben. Wenn Sie einen ungültigen Speicherort angeben, z. b. nach dem Ende der Datei, gibt **mmioseek** möglicherweise keinen Fehler zurück, aber nachfolgende e/a-Vorgänge könnten fehlschlagen.

Es gibt Flags, die Sie mit der **mmioopen** -Funktion für Vorgänge über einfache Datei-e/a verwenden können. Durch Angeben einer [**mmioinfo**](/previous-versions//dd757322(v=vs.85)) -Struktur können Sie z. b. Arbeitsspeicher Dateien öffnen, eine benutzerdefinierte e/a-Prozedur angeben oder einen Puffer für gepufferte e/a-Vorgänge angeben.

 

 