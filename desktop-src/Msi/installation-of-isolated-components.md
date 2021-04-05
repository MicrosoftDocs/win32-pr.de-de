---
description: Windows Installer führt die folgenden Aktionen während der Installation einer Anwendung aus, wenn das Paket isolierte Komponenten enthält. In der Regel \_ handelt es sich bei der gemeinsam genutzten Komponente um eine DLL, die von Komponenten \_ Anwendungen und anderen ausführbaren Client Dateien gemeinsam genutzt wird
ms.assetid: fbc5dd86-5d38-4ce8-ab38-03c84cc77e80
title: Installation isolierter Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c1b9a7e21c212474701409e887d0afd5517774
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753768"
---
# <a name="installation-of-isolated-components"></a>Installation isolierter Komponenten

Windows Installer führt die folgenden Aktionen während der Installation einer Anwendung aus, wenn das Paket isolierte Komponenten enthält. In der Regel \_ handelt es sich bei der gemeinsam genutzten Komponente um eine DLL, die von Komponenten \_ Anwendungen und anderen ausführbaren Client Dateien gemeinsam genutzt wird

## <a name="installation"></a>Installation

-   Kopieren Sie die Dateien der frei \_ gegebenen Komponente in denselben Ordner wie die Komponenten \_ Anwendung, wenn auch die Komponenten \_ Anwendung installiert wird.
-   Erstellen Sie eine 0-Byte-Datei mit dem kurzen Dateinamen der Schlüsseldatei der Komponenten \_ Anwendung. Suchen Sie diese Datei im selben Ordner wie die Komponenten \_ Anwendung. Fügen Sie die Erweiterung an. Lokal mit diesem Dateinamen.
-   Erhöhen Sie SHAREDDLL refcount, wenn das msidbcomponentattributesshareddllrefcount-Bit in der Attribute-Spalte der [Komponenten Tabelle](component-table.md)festgelegt ist.
-   Registrieren \_ Sie die Komponenten Anwendung als Client der \_ gemeinsam genutzten Komponente, und registrieren Sie einen Schlüssel Pfad, der auf den freigegebenen Speicherort der freigegebenen Komponente verweist \_ .
-   Installieren Sie alle Ressourcen der Komponenten \_ Anwendung wie gewohnt.

Wenn \_ die freigegebene Komponente oder die zugehörige Schlüsseldatei bereits auf dem Computer installiert ist, kopieren Sie keine Dateien an den freigegebenen Speicherort der freigegebenen Komponente \_ .

Wenn \_ die freigegebene Komponente oder die zugehörige Schlüsseldatei noch nicht auf dem Computer installiert ist:

-   Kopieren Sie die Dateien der frei \_ gegebenen Komponente in den freigegebenen Speicherort.
-   Alle Installations Aktionen für freigegebene Komponenten verarbeiten \_ .
-   Wenn die \_ freigegebene Komponente eine COM-Komponente ist, registrieren Sie den vollständigen com-Pfad so, dass die Syntax \[ $Component \] und \[ \# File Key \] auf den freigegebenen Speicherort der freigegebenen Komponente verweisen \_ .

 

 



