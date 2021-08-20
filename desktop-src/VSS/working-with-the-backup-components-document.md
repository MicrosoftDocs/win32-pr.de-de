---
description: Ein Anforderer erstellt zu Beginn der Ausführung einer Sicherung ein Sicherungskomponentendokument.
ms.assetid: 5e40e45d-6afa-401a-a6b4-7bec460cb9ec
title: Arbeiten mit dem Sicherungskomponentendokument
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a401bb38634cae0f00659f618979012d28327070e8d1e23e9b85cc598300636
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117937354"
---
# <a name="working-with-the-backup-components-document"></a>Arbeiten mit dem Sicherungskomponentendokument

Ein Anforderer erstellt zu Beginn der Ausführung einer Sicherung ein Sicherungskomponentendokument. Das Dokument enthält anfänglich nur eine Beschreibung des Zustands des Sicherungsvorgangs. Während der Wiederherstellung sollte das Dokument Anweisungen dazu enthalten, wie ein Anforderer beim Kopieren von Dateien zurück auf den Datenträger vorgehen soll. Im Verlauf des Wiederherstellungsvorgangs wird das Sicherungskomponentendokument geändert und enthält den Status dieses Vorgangs.

Im Gegensatz zum Schreibmetadatendokument, das schreibgeschützt ist, gibt es ein Fenster, in dem das Sicherungskomponentendokument sowohl von Anfordernden als auch von Writern geändert werden kann. Das Dokument kann aktualisiert werden, bis während Sicherungsvorgängen ein [*BackupComplete-*](vssgloss-b.md) oder [*BackupShutdown-Ereignis*](vssgloss-b.md) und während der Wiederherstellung ein [*PostRestore-Ereignis*](vssgloss-p.md) erstellt wird.

Um das Sicherungskomponentendokument eines Anforderers verwenden zu können, müssen Sie die folgenden Themen verstehen:

-   [Sicherungskomponenten – Dokumentlebenszyklus](backup-components-document-life-cycle.md)
-   [Inhalt des Sicherungskomponentendokuments](backup-components-document-contents.md)

 

 



