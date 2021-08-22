---
description: Windows Installationsprogramm 5.0, das auf Windows Server 2008 R2 oder Windows 7 ausgeführt wird, kann alle auf dem Computer installierten Komponenten aufzählen und den Schlüsselpfad für die Komponente abrufen.
ms.assetid: a6676340-1695-48c7-a1e4-7a02a7bc3fef
title: Aufzählen von Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 598e80e270d0442b06fdb6db50cc5b58df529a1305936f2610211f192c8572be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947041"
---
# <a name="enumerating-components"></a>Aufzählen von Komponenten

Windows Installationsprogramm 5.0, das auf Windows Server 2008 R2 oder Windows 7 ausgeführt wird, kann alle auf dem Computer installierten Komponenten aufzählen und den Schlüsselpfad für die Komponente abrufen. Ein Paket, das für Windows Installer 5.0 erstellt wurde, kann die Funktionen [**MsiEnumComponentsEx,**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa) [**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)und [**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa) verwenden, um über Benutzerkonten und Installationskontexte hinweg nach Komponenten und Produkten zu suchen. Die [**Funktionen MsiEnumComponents,**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa) [**MsiEnumClients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa)und [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) geben nur Informationen zu Komponenten und Produkten zurück, die für das Benutzerkonto installiert sind, das die Funktion aufgerufen hat. Mehrere Aufrufe dieser Funktionen, mindestens einmal für jedes Benutzerkonto, sind erforderlich, um Informationen für den gesamten Computer zu sammeln.

Die [**MsiEnumComponentsEx-Funktion**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa) aufzählt installierte Komponenten. Die Funktion ruft bei jedem Aufgerufenen einen Komponentencode ab. Das [**Komponentenobjekt**](components.md) empfängt Von dieser Funktion Informationen zu einer installierten Komponente.

Die [**MsiEnumClientsEx-Funktion**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa) aufzählt Produkte, die Clients einer angegebenen installierten Komponente sind. Das [**Clientobjekt**](client.md) empfängt von dieser Funktion Informationen zu einem Client.

Die [**MsiGetComponentPathEx-Funktion**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa) gibt den vollständigen Pfad zu einer installierten Komponente zurück. Die Funktion gibt den Registrierungsschlüssel zurück, wenn der Schlüsselpfad für die Komponente ein Registrierungsschlüssel ist. Das [**ComponentInfo-Objekt**](componentinfo.md) empfängt Von dieser Funktion Informationen zu einer installierten Komponente.

**[Windows Installer 4.5 oder früher:](not-supported-in-windows-installer-4-5.md)** Nicht unterstützt. Diese Funktionalität ist ab Windows Installer 5.0 verfügbar, das auf Windows 7 oder Windows Server 2008 R2 ausgeführt wird.

 

 



