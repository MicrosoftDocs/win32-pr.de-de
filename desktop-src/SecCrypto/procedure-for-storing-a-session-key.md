---
description: Erläutert das Verfahren zum Speichern eines Sitzungsschlüssels.
ms.assetid: 9ab7f747-9c69-40b5-af78-163f3ba315bf
title: Speichern eines Sitzungsschlüssels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3b17de657ddba47dd77f68c1ee7a2adfdf93e7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356189"
---
# <a name="storing-a-session-key"></a>Speichern eines Sitzungsschlüssels

> [!Note]  
> In diesem Abschnitt wird davon ausgegangen, dass Benutzer über einen Satz von [*öffentlichen/privaten Schlüsselpaaren*](../secgloss/p-gly.md)verfügen. Anweisungen und ein Beispiel zum Erstellen von Schlüsselpaaren finden Sie im [Beispiel C-Programm: Erstellen eines Schlüssel Containers und](example-c-program-creating-a-key-container-and-generating-keys.md)Erstellen von Schlüsseln.

 

**So speichern Sie einen Sitzungsschlüssel**

1.  Erstellen Sie ein einfaches [*Schlüsselblob*](../secgloss/k-gly.md) mithilfe der [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) -Funktion. Dadurch wird der Sitzungsschlüssel vom CSP in den Speicherbereich einer Anwendung übertragen. Geben Sie an, dass ein öffentlicher Exchange-Schlüssel zum Signieren des Schlüssel-BLOBs verwendet werden soll.
2.  Speichert das signierte Schlüsselblob auf dem Datenträger. Es wird davon ausgegangen, dass alle Datenträger nicht sicher sind.
3.  Wenn der Schlüssel benötigt wird, lesen Sie den Schlüssel-BLOB von der Festplatte.
4.  Importieren Sie das Schlüsselblob mithilfe der [**cryptimportkey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) -Funktion wieder in den CSP.

Ein Beispiel für das Erstellen eines [*Sitzungsschlüssels*](../secgloss/s-gly.md) und das Exportieren des Schlüssels in ein [*einfaches Schlüsselblob*](../secgloss/s-gly.md) , das in eine Datenträger Datei geschrieben werden kann, finden Sie unter [Beispiel C-Programm: Exportieren eines Sitzungsschlüssels](example-c-program-exporting-a-session-key.md).

Diese Prozedur bietet nur minimale Sicherheit. Wenn der gespeicherte Sitzungsschlüssel verwendet wird, um Daten zu einem späteren Zeitpunkt zu verschlüsseln, bietet das vorherige Verfahren keine angemessene Sicherheit.

Signieren Sie das Schlüsselblob mit einem privaten Exchange-Schlüssel, bevor es auf einem Datenträger gespeichert wird, um die Sicherheit zu erhöhen. Wenn das Schlüssel-BLOB später von der Festplatte gelesen wird, kann die Signatur überprüft werden, um sicherzustellen, dass das Schlüsselblob intakt ist.

Wenn das Schlüsselblob nicht signiert ist, kann jeder Benutzer mit Zugriff auf den Datenträger oder auf ein anderes Medium, auf dem der Schlüssel gespeichert ist, einen neuen Sitzungsschlüssel erstellen.

Der neue Sitzungsschlüssel kann mit dem [*öffentlichen Schlüssel*](../secgloss/p-gly.md) [*Austausch Schlüssel*](../secgloss/e-gly.md)des Benutzers verschlüsselt werden, und dieser neue Schlüssel kann durch den ursprünglichen Schlüssel ersetzt werden. Wenn der Benutzer den ersetzten Sitzungsschlüssel zum Verschlüsseln von Dateien und Nachrichten unwissentlich verwendet hat, kann die Person, die den Ersatzschlüssel erstellt hat, Sie problemlos entschlüsseln.

Digitale Signaturen werden in [Hashes und digitalen Signaturen](hashes-and-digital-signatures.md)ausführlich erläutert.

 

 
