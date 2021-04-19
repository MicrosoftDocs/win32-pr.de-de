---
description: Windows Installer führt beim Entfernen einer Anwendung die folgenden Aktionen aus, wenn das Paket isolierte Komponenten enthält. In der Regel \_ handelt es sich bei der gemeinsam genutzten Komponente um eine DLL, die von Komponenten \_ Anwendungen und anderen ausführbaren Client Dateien gemeinsam genutzt wird
ms.assetid: 26343a01-9a06-43d5-bbe3-959faf51739d
title: Entfernen isolierter Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adf19769067230b82f68a35f7b9fbedcd1c56440
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358596"
---
# <a name="removal-of-isolated-components"></a>Entfernen isolierter Komponenten

Windows Installer führt beim Entfernen einer Anwendung die folgenden Aktionen aus, wenn das Paket isolierte Komponenten enthält. In der Regel \_ handelt es sich bei der gemeinsam genutzten Komponente um eine DLL, die von Komponenten \_ Anwendungen und anderen ausführbaren Client Dateien gemeinsam genutzt wird

## <a name="uninstall"></a>Deinstallieren

-   Entfernen Sie die Dateien der Komponente \_ , die aus dem Ordner mit der Komponenten Anwendung freigegeben \_ wurden, nur, wenn die Komponenten \_ Anwendung ebenfalls entfernt wird.
-   Wenn das msidbcomponentattributesshareddllrefcount-Bit in der [Komponenten Tabelle](component-table.md) festgelegt ist, wird der SHAREDDLL refcount-Wert verringert.
-   Entfernen Sie. Lokale 0-Byte-Datei aus dem Ordner, der die Komponenten \_ Anwendung enthält.
-   Entfernen Sie \_ die Komponenten Anwendung aus der Client Liste der frei \_ gegebenen Komponenten.
-   Entfernen Sie alle Ressourcen der Komponenten \_ Anwendung wie üblich.

Wenn in der Liste der freigegebenen Komponenten andere Produkte verbleiben \_ :

-   Entfernen Sie keine Dateien aus dem freigegebenen Speicherort der frei \_ gegebenen Komponente.

Wenn SHAREDDLL refcount für die frei \_ gegebene Komponente 0 ist, nachdem Sie verringert wurde, oder wenn keine anderen verbleibenden Clients der Komponente frei \_ gegeben sind:

-   Entfernen Sie die Dateien der Komponente, die \_ vom freigegebenen Speicherort verwendet wird.
-   Alle Deinstallations Aktionen in Bezug auf diese Komponente verarbeiten.

 

 



