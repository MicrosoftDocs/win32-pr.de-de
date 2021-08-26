---
description: Terminologie zur Beschreibung von Transaktions-NTFS (TxF).
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 44cb060c-e6a6-48d6-bbcf-d8dc1ae8ceb2
title: TxF-Glossar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06e6e296319dc1a9ccd02834fe6144c28d15d61a0fe0c1ec449a07d81f96dbe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900650"
---
# <a name="txf-glossary"></a>TxF-Glossar

<dl> <dt>

<span id="fs.availability"></span><span id="FS.AVAILABILITY"></span>**Verfügbarkeit**
</dt> <dd>

Verfügbarkeit bedeutet, dass ein Ressourcen-Manager Transaktionen auch dann abbricht, wenn dies die Konsistenz unterbricht, sodass das System weiterhin neue Arbeit durchführen kann. Der Standardressourcen-Manager erzwingt die Verfügbarkeit auf dem Systemvolumen. Wenn das Transaktionsprotokoll z. B. voll ist, kein neuer Transaktionsprotokollspeicherplatz hinzugefügt werden kann und eine ältere Transaktion, die abgebrochen würde, ein Ergebnis von einem übergeordneten Ressourcen-Manager übermittelt werden muss, damit eine verteilte Transaktion abgeschlossen wird, wartet der Ressourcen-Manager nicht auf den übergeordneten Transaktions-Manager und bricht diese Transaktion ab, obwohl dies die Konsistenz möglicherweise unterbricht.

</dd> <dt>

<span id="fs.consistency"></span><span id="FS.CONSISTENCY"></span>**Konsistenz**
</dt> <dd>

Konsistenz bedeutet, dass ein Ressourcen-Manager bei neuen Transaktionen fehlschlägt, wenn kein Fortschritt erzielt werden kann. Wenn das Transaktionsprotokoll beispielsweise voll ist, kein neuer Transaktionsprotokollspeicherplatz hinzugefügt werden kann und eine ältere Transaktion, die abgebrochen würde, ein Ergebnis von einem übergeordneten Ressourcen-Manager übermittelt werden muss, damit eine verteilte Transaktion abgeschlossen wird, wartet der Ressourcen-Manager auf dieses Ergebnis.

</dd> <dt>

<span id="fs.miniversion"></span><span id="FS.MINIVERSION"></span>**miniversion**
</dt> <dd>

Eine Miniversion ist eine Version einer Datei, die ein transaktiver Writer während einer Transaktion erstellt. Die Miniversion kann später in der Transaktion mit schreibgeschützten Zugriff geöffnet werden.

</dd> <dt>

<span id="fs.transacted_reader"></span><span id="FS.TRANSACTED_READER"></span>**Transaktiver Reader**
</dt> <dd>

Ein transaktiver Reader ist ein transaktives Dateihandles, das mit jeder Berechtigung geöffnet wird, die Teil des generischen Lesezugriffs, aber nicht Teil des generischen Schreibzugriffs ist.

</dd> <dt>

<span id="fs.transacted_writer"></span><span id="FS.TRANSACTED_WRITER"></span>**Transacted Writer**
</dt> <dd>

Ein transaktiver Writer ist ein transaktives Dateihandles, das mit jeder Berechtigung geöffnet wird, die nicht Teil des generischen Lesezugriffs ist, aber Teil des generischen Schreibzugriffs ist.

</dd> </dl>

 

 



