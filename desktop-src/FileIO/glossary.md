---
description: Terminologie, die zum Beschreiben von Transaktions-NTFS (TxF) verwendet wird.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 44cb060c-e6a6-48d6-bbcf-d8dc1ae8ceb2
title: TxF-Glossar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee17e9c53b804995e7ef3491b68e963e9311a37f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218012"
---
# <a name="txf-glossary"></a>TxF-Glossar

<dl> <dt>

<span id="fs.availability"></span><span id="FS.AVAILABILITY"></span>**verfüg**
</dt> <dd>

Verfügbarkeit bedeutet, dass ein Ressourcen-Manager Transaktionen abbricht, auch wenn dies zu einer Unterbrechung der Konsistenz führt, damit das System weiterhin neue Aufgaben ausführen kann. Der Standard Ressourcen-Manager erzwingt die Verfügbarkeit auf dem System Volume. Wenn das Transaktionsprotokoll z. b. voll ist, kann kein neuer Transaktionsprotokoll-Speicherplatz hinzugefügt werden, und eine ältere Transaktion, die abgebrochen wird, erfordert ein Ergebnis, das von einem übergeordneten Ressourcen-Manager bereitgestellt werden muss, damit eine verteilte Transaktion abgeschlossen wird. der Ressourcen-Manager wartet nicht auf den übergeordneten Transaktions-Manager und bricht diese Transaktion ab

</dd> <dt>

<span id="fs.consistency"></span><span id="FS.CONSISTENCY"></span>**konsistent**
</dt> <dd>

Konsistenz bedeutet, dass ein Ressourcen-Manager für neue Transaktionen einen Fehler erzeugt, wenn der Vorgang nicht fortgesetzt werden kann. Wenn das Transaktionsprotokoll z. b. voll ist, kann kein neuer Transaktionsprotokoll-Speicherplatz hinzugefügt werden, und für eine ältere Transaktion, die abgebrochen wird, muss ein Ergebnis von einem übergeordneten Ressourcen-Manager bereitgestellt werden, damit eine verteilte Transaktion abgeschlossen werden kann. der Ressourcen-Manager wartet auf das Ergebnis.

</dd> <dt>

<span id="fs.miniversion"></span><span id="FS.MINIVERSION"></span>**Triggerszenarios**
</dt> <dd>

Eine Triggerszenarios ist eine Version einer Datei, die von einem transaktiven Writer während einer Transaktion erstellt wird. Die Triggerszenarios kann später in der Transaktion mit Schreib geschütztem Zugriff geöffnet werden.

</dd> <dt>

<span id="fs.transacted_reader"></span><span id="FS.TRANSACTED_READER"></span>**transaktive Reader**
</dt> <dd>

Bei einem transaktiven Reader handelt es sich um ein transaktives Datei Handle, das mit einer beliebigen Berechtigung geöffnet ist, die Teil des generischen Lese Zugriffs ist, aber nicht Teil des generischen Schreibzugriffs ist.

</dd> <dt>

<span id="fs.transacted_writer"></span><span id="FS.TRANSACTED_WRITER"></span>**Transaktiver Writer**
</dt> <dd>

Bei einem transaktiven Writer handelt es sich um ein transaktives Datei Handle, das mit einer beliebigen Berechtigung geöffnet ist, die nicht Teil des allgemeinen Lese Zugriffs ist, aber Teil des generischen Schreibzugriffs ist.

</dd> </dl>

 

 



