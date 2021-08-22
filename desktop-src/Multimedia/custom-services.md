---
title: Benutzerdefinierte Dienste
description: Benutzerdefinierte Dienste
ms.assetid: 98b68205-3a34-4406-84de-bf2c8a5ed5b0
keywords:
- Multimediadatei-E/A, benutzerdefinierte Dienste
- Datei-E/A, benutzerdefinierte Dienste
- Eingabe und Ausgabe (E/A), benutzerdefinierte Dienste
- E/A (Eingabe und Ausgabe), benutzerdefinierte Dienste
- Benutzerdefinierte E/A
- mmioInstallIOProc-Funktion
- mmioOpen-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8c2418d3a87669527feda37547674bee83175dd6e4533312e8b89c346048c04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144573"
---
# <a name="custom-services"></a>Benutzerdefinierte Dienste

Multimedia-Datei-E/A-Dienste verwenden E/A-Verfahren, um die physischen Eingaben und Ausgaben zu verarbeiten, die mit dem Lesen und Schreiben in verschiedene Arten von Speichersystemen verbunden sind, z. B. Dateiarchivierungssysteme und Datenbankspeichersysteme. Vordefinierte E/A-Prozeduren sind für die Standarddateisysteme und für Speicherdateien vorhanden. Sie können jedoch mithilfe der [**mmioInstallIOProc-Funktion**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) eine benutzerdefinierte E/A-Prozedur für den Zugriff auf ein eindeutiges Speichersystem verwenden.

Verwenden Sie die [**mmioOpen-Funktion,**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) um eine Datei mithilfe einer benutzerdefinierten E/A-Prozedur zu öffnen. Fügen Sie ein Pluszeichen (+) oder die CFSEPCHAR-Konstante in den Dateinamen ein, um den Namen der physischen Datei vom Namen des Elements der Datei zu trennen, das Sie öffnen möchten. Im folgenden Beispiel wird ein Dateielement mit dem Namen "element" aus einer Datei namens FILENAME geöffnet. Arc:


```C++
mmioOpen("filename.arc+element", NULL, MMIO_READ); 
```



Wenn der Datei-E/A-Manager auf ein Pluszeichen in einem Dateinamen stößt, wird die Dateinamenerweiterung untersucht, um zu bestimmen, welche E/A-Prozedur der Datei zugeordnet werden soll. Im vorherigen Beispiel hat der Datei-E/A-Manager versucht, die dem zugeordnete E/A-Prozedur zu verwenden. ARC-Dateinamenerweiterung; Diese E/A-Prozedur wäre mit [**mmioInstallIOProc installiert worden.**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) Wenn keine E/A-Prozedur installiert ist, [**gibt mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) einen Fehler zurück.

E/A-Prozeduren müssen auf die folgenden Meldungen reagieren:

-   [**MMIOM \_ CLOSE**](mmiom-close.md)
-   [**MMIOM \_ OPEN**](mmiom-open.md)
-   [**MMIOM \_ READ**](mmiom-read.md)
-   [**MMIOM \_ WRITE**](mmiom-write.md)
-   [**MMIOM \_ SEEK**](mmiom-seek.md)
-   [**\_MMIOM-UMBENENNUNG**](mmiom-rename.md)
-   [**MMIOM \_ WRITEFLUSH**](mmiom-writeflush.md)

Sie können auch benutzerdefinierte Nachrichten erstellen und mithilfe der [**mmioSendMessage-Funktion**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosendmessage) an Ihre E/A-Prozedur senden. Wenn Sie eigene Nachrichten definieren, stellen Sie sicher, dass sie bei oder über dem Wert definiert sind, der von der MMIOM \_ USER-Konstante definiert wird.

Zusätzlich zur Verarbeitung von Nachrichten muss eine E/A-Prozedur das **lDiskOffset-Element** der [**MMIOINFO-Struktur**](/previous-versions//dd757322(v=vs.85)) verwalten (auf das durch den *lpmmioinfo-Parameter* der **mmioOpen-Funktion** verwiesen wird). Das **lDiskOffset-Mitglied** muss immer den Dateioffset zu dem Speicherort enthalten, auf den die nächste \_ MMIOM READ- oder MMIOM \_ WRITE-Nachricht zugreifen wird. Der Offset wird in Bytes angegeben und ist relativ zum Anfang der Datei. Die E/A-Prozedur kann das **adwInfo-Element** verwenden, um alle erforderlichen Zustandsinformationen zu verwalten. Die E/A-Prozedur sollte keine anderen Member in der **MMIOINFO-Struktur** ändern.

 

 