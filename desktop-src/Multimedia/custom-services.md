---
title: Benutzerdefinierte Dienste
description: Benutzerdefinierte Dienste
ms.assetid: 98b68205-3a34-4406-84de-bf2c8a5ed5b0
keywords:
- Multimedia-Datei-e/a, benutzerdefinierte Dienste
- Datei-e/a, benutzerdefinierte Dienste
- Eingabe und Ausgabe (e/a), benutzerdefinierte Dienste
- E/a (Eingabe und Ausgabe), benutzerdefinierte Dienste
- benutzerdefinierte e/a
- mmioinstallioproc-Funktion
- mmioopen-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e41e3c5974fee9903c0864b1cfefccc8354b26a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038943"
---
# <a name="custom-services"></a>Benutzerdefinierte Dienste

Multimedia-Datei-e/a-Dienste verwenden e/a-Prozeduren, um die physische Eingabe und Ausgabe zu verarbeiten, die dem Lesen und Schreiben in verschiedene Typen von Speichersystemen zugeordnet sind, z. b. Datei Archivierungssysteme und Daten Bank Speicher Vordefinierte e/a-Prozeduren sind für die Standarddatei Systeme und für Speicherdateien vorhanden, Sie können jedoch eine benutzerdefinierte e/a-Prozedur für den Zugriff auf ein eindeutiges Speichersystem mithilfe der [**mmioinstallioproc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) -Funktion bereitstellen.

Verwenden Sie zum Öffnen einer Datei mit einer benutzerdefinierten e/a-Prozedur die [**mmioopen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) -Funktion. Fügen Sie ein Pluszeichen (+) oder die cfsepchar-Konstante in den Dateinamen ein, um den Namen der physischen Datei von dem Namen des Elements der Datei zu trennen, die Sie öffnen möchten. Im folgenden Beispiel wird ein Datei Element mit dem Namen "Element" aus der Datei "filename" geöffnet. Bogen


```C++
mmioOpen("filename.arc+element", NULL, MMIO_READ); 
```



Wenn der Datei-e/a-Manager ein Pluszeichen in einem Dateinamen erkennt, wird die Dateinamenerweiterung untersucht, um zu bestimmen, welche e/a-Prozedur der Datei zugeordnet werden soll. Im vorherigen Beispiel hat der Datei-e/a-Manager versucht, die e/a-Prozedur zu verwenden, die dem zugeordnet ist. Dateinamenerweiterung des Bogens; Diese e/a-Prozedur wurde mithilfe von [**mmioinstallioproc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc)installiert. Wenn keine e/a-Prozedur installiert ist, gibt [**mmioopen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) einen Fehler zurück.

E/a-Prozeduren müssen auf die folgenden Meldungen Antworten:

-   [**mmiom \_ Schließen**](mmiom-close.md)
-   [**mmiom \_ geöffnet**](mmiom-open.md)
-   [**mmiom- \_ Lesevorgang**](mmiom-read.md)
-   [**mmiom- \_ Schreibvorgang**](mmiom-write.md)
-   [**mmiom- \_ Suche**](mmiom-seek.md)
-   [**Umbenennen von mmiom \_**](mmiom-rename.md)
-   [**mmiom- \_ Schreibvorgang**](mmiom-writeflush.md)

Sie können auch benutzerdefinierte Nachrichten erstellen und Sie mithilfe der [**mmiosendmessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosendmessage) -Funktion an Ihre e/a-Prozedur senden. Wenn Sie Ihre eigenen Nachrichten definieren, stellen Sie sicher, dass Sie mit dem durch die mmiom-Benutzer Konstante definierten Wert definiert oder überschritten werden \_ .

Zusätzlich zum Verarbeiten von Nachrichten muss ein e/a-Vorgang das **ldiskoffset** -Element der [**mmioinfo**](/previous-versions//dd757322(v=vs.85)) -Struktur beibehalten (auf den der *lpmmioinfo* -Parameter der **mmioopen** -Funktion verweist). Der **ldiskoffset** -Member muss immer den Dateioffset an dem Speicherort enthalten, auf den die nächste mmiom- \_ Lese-oder mmiom- \_ Schreib Nachricht zugreift. Der Offset wird in Bytes angegeben und ist relativ zum Anfang der Datei. Die e/a-Prozedur kann den **adwinfo** -Member verwenden, um alle erforderlichen Zustandsinformationen zu erhalten. Die e/a-Prozedur sollte keine anderen Member in der **mmioinfo** -Struktur ändern.

 

 