---
description: Windows Installer 5,0, das unter Windows Server 2008 R2 oder Windows 7 ausgeführt wird, kann alle auf dem Computer installierten Komponenten auflisten und den Schlüssel Pfad für die Komponente abrufen.
ms.assetid: a6676340-1695-48c7-a1e4-7a02a7bc3fef
title: Auflisten von Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea314ee91c35fb021f5a8da64b6430e8cf950ecd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755417"
---
# <a name="enumerating-components"></a>Auflisten von Komponenten

Windows Installer 5,0, das unter Windows Server 2008 R2 oder Windows 7 ausgeführt wird, kann alle auf dem Computer installierten Komponenten auflisten und den Schlüssel Pfad für die Komponente abrufen. Ein Paket, das für Windows Installer 5,0 erstellt wurde, kann die Funktionen " [**msienübercomponentsex**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa)", " [**msienumschlag clientsex**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)" und " [**msigetcomponentpathex**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa) " verwenden, um Komponenten und Produkte über Benutzerkonten und Installations Kontexte hinweg zu suchen. Die Funktionen [**msienumcomponents**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa), [**msienumclients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa)und [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) geben nur Informationen für Komponenten und Produkte zurück, die für das Benutzerkonto installiert wurden, das die Funktion aufgerufen hat. Mehrere Aufrufe dieser Funktionen, mindestens einmal für jedes Benutzerkonto, sind erforderlich, um Informationen für den gesamten Computer zu sammeln.

Die Funktion [**msienumcomponentsex**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa) listet die installierten Komponenten auf. Die-Funktion Ruft jedes Mal einen Komponenten Code ab, wenn Sie aufgerufen wird. Das [**Komponenten Objekt**](components.md) empfängt Informationen über eine installierte Komponente durch diese Funktion.

Die Funktion [**msienumclientsex**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa) listet Produkte auf, bei denen es sich um Clients einer angegebenen installierten Komponente handelt. Das [**Client Objekt**](client.md) empfängt von dieser Funktion Informationen zu einem Client.

Die [**msigetcomponentpathex**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa) -Funktion gibt den vollständigen Pfad zu einer installierten Komponente zurück. Die-Funktion gibt den Registrierungsschlüssel zurück, wenn der Schlüssel Pfad für die Komponente ein Registrierungsschlüssel ist. Das [**ComponentInfo-Objekt**](componentinfo.md) empfängt Informationen über eine installierte Komponente durch diese Funktion.

**[Windows Installer 4,5 oder früher](not-supported-in-windows-installer-4-5.md):** Nicht unterstützt. Diese Funktionalität ist ab Windows Installer 5,0, die unter Windows 7 oder Windows Server 2008 R2 ausgeführt wird.

 

 



