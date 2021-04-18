---
description: Ein Anforderer erstellt ein Sicherungs Komponenten Dokument zu Beginn der Sicherung.
ms.assetid: 5e40e45d-6afa-401a-a6b4-7bec460cb9ec
title: Arbeiten mit dem Dokument mit den Sicherungs Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40d5d3c97696b85d589501f6d3af0b6c7d0e6d47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347183"
---
# <a name="working-with-the-backup-components-document"></a>Arbeiten mit dem Dokument mit den Sicherungs Komponenten

Ein Anforderer erstellt ein Sicherungs Komponenten Dokument zu Beginn der Sicherung. Das Dokument enthält zunächst nur eine Beschreibung des Status des Sicherungs Vorgangs. Während der Wiederherstellung sollte das Dokument Anweisungen dazu bereitstellen, wie ein Anforderer mit dem Kopieren von Dateien auf den Datenträger fortfahren soll. Im Verlauf des Wiederherstellungs Vorgangs wird das Dokument mit den Sicherungs Komponenten geändert, das den Status dieses Vorgangs enthält.

Im Gegensatz zum schreibgeschützten Writer-Metadatendokument gibt es ein Fenster, in dem das Dokument mit den Sicherungs Komponenten von Anforderern und Writern geändert werden kann. Das Dokument kann bis zur Generierung eines [*BackupComplete*](vssgloss-b.md) -oder [*BackupShutdown*](vssgloss-b.md) -Ereignisses während Sicherungs Vorgängen und bis zu einem [*postrestore*](vssgloss-p.md) -Ereignis während der Wiederherstellung aktualisiert werden.

Um das Dokument mit den Sicherungs Komponenten eines Anforderers zu verwenden, ist ein Verständnis der folgenden Themen erforderlich:

-   [Lebenszyklus von Sicherungs Komponenten Dokumenten](backup-components-document-life-cycle.md)
-   [Dokumentinhalte der Sicherungs Komponenten](backup-components-document-contents.md)

 

 



