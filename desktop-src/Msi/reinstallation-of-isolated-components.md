---
description: Windows Installer führt während der erneuten Installation einer Anwendung die folgenden Aktionen aus, wenn das Paket isolierte Komponenten enthält. In der Regel \_ handelt es sich bei der gemeinsam genutzten Komponente um eine DLL, die von Komponenten \_ Anwendungen und anderen ausführbaren Client Dateien gemeinsam genutzt wird
ms.assetid: 65909b47-dc09-4e9a-920a-9cb3f55b2e67
title: Neuinstallation isolierter Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ad1c7fb53eb09e96882209f7738e95be9b4a64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864828"
---
# <a name="reinstallation-of-isolated-components"></a>Neuinstallation isolierter Komponenten

Windows Installer führt während der erneuten Installation einer Anwendung die folgenden Aktionen aus, wenn das Paket isolierte Komponenten enthält. In der Regel \_ handelt es sich bei der gemeinsam genutzten Komponente um eine DLL, die von Komponenten \_ Anwendungen und anderen ausführbaren Client Dateien gemeinsam genutzt wird

## <a name="reinstallation"></a>Neuinstallation

-   Installieren Sie die Dateien der-Komponente, die \_ im selben Ordner wie die Komponenten Anwendung freigegeben \_ werden, neu, wenn die Komponenten \_ Anwendung ebenfalls neu installiert wird.
-   Erhöhen Sie nicht die Client Liste der freigegebenen Komponenten, \_ und erhöhen Sie die Anzahl der SHAREDDLL nicht.
-   Erstellen Sie die 0-Byte-Datei mit dem kurzen Dateinamen der Schlüsseldatei der Komponenten \_ Anwendung neu. Diese Datei muss sich im selben Ordner wie \_ die Komponenten Anwendung befinden und die Erweiterung aufweisen. Nah.
-   Installieren Sie wie gewohnt alle Ressourcen der Komponenten \_ Anwendung neu.

Wenn SHAREDDLL refcount für die frei \_ gegebene Komponente größer als 1 ist, oder wenn andere Produkte in der Client Liste der freigegebenen Komponenten verbleiben \_ :

-   Installieren Sie keine Dateien erneut an den freigegebenen Speicherort der frei \_ gegebenen Komponente.

Wenn SHAREDDLL refcount für die frei \_ gegebene Komponente 1 ist, oder wenn keine anderen verbleibenden Clients der Komponente frei \_ gegeben sind:

-   Installieren Sie die Dateien der an \_ den freigegebenen Speicherort freigegebenen Komponenten mithilfe der Regeln für die [Datei Versions](file-versioning-rules.md)Verwaltung neu.
-   Alle Neuinstallations Aktionen für freigegebene Komponenten verarbeiten \_ .
-   Wenn die \_ freigegebene Komponente eine COM-Komponente ist, registrieren Sie den vollständigen com-Pfad, sodass der Installer \[ $Component \] und den \[ \# filekey- \] Punkt auf den freigegebenen Speicherort der freigegebenen Komponente verweist \_ .

 

 



