---
description: Wenn eine Assembly an einem isolierten Speicherort für eine bestimmte Anwendung installiert wird, muss die Anwendung in der Datei \_ Anwendungs Spalte der MsiAssembly-Tabelle angegeben werden.
ms.assetid: 8d7fc09c-1017-4a30-be00-b7b0e5f2a057
title: Installieren und Entfernen von Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f44dee05940ab3c05e97a7145f9b2363226bb07c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218539"
---
# <a name="installing-and-removing-assemblies"></a>Installieren und Entfernen von Assemblys

Wenn eine Assembly an einem isolierten Speicherort für eine bestimmte Anwendung installiert wird, muss die Anwendung in der Datei \_ Anwendungs Spalte der [MsiAssembly-Tabelle](msiassembly-table.md)angegeben werden. Dieses Feld ist ein Schlüssel in die [Dateitabelle](file-table.md). Das Installationsprogramm verwendet die in der [Verzeichnis Tabelle](directory-table.md) angegebene Verzeichnisstruktur, um die Assembly im gleichen Verzeichnis wie die Komponente zu installieren, in der diese Datei enthalten ist.

Wenn eine Assembly in den globalen Assemblycache installiert wird, muss der Wert in der Datei \_ Anwendungs Spalte der [MsiAssembly-Tabelle](msiassembly-table.md) NULL sein.

In den folgenden Abschnitten wird die Installation von Win32-und Common Language Runtime-Assemblys beschrieben:

-   [Installation von Win32-Assemblys](installation-of-win32-assemblies.md)
-   [Installation von Common Language Runtime-Assemblys](installation-of-common-language-runtime-assemblies.md)

 

 



