---
description: Beim Installieren einer Assembly an einem isolierten Speicherort für eine bestimmte Anwendung muss die Anwendung in der \_ Spalte Dateianwendung der MsiAssembly-Tabelle angegeben werden.
ms.assetid: 8d7fc09c-1017-4a30-be00-b7b0e5f2a057
title: Installieren und Entfernen von Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0117c29a9bcc49a549529a6e05f1124236cb845d9b7792d7bcbda143fd6d08e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043430"
---
# <a name="installing-and-removing-assemblies"></a>Installieren und Entfernen von Assemblys

Beim Installieren einer Assembly an einem isolierten Speicherort für eine bestimmte Anwendung muss die Anwendung in der \_ Spalte Dateianwendung der [MsiAssembly-Tabelle](msiassembly-table.md)angegeben werden. Dieses Feld ist ein Schlüssel in der [Dateitabelle](file-table.md). Das Installationsprogramm verwendet die Verzeichnisstruktur, die in der [Directory-Tabelle](directory-table.md) angegeben ist, um die Assembly in demselben Verzeichnis wie die Komponente zu installieren, die diese Datei enthält.

Beim Installieren einer Assembly im globalen Assemblycache muss der Wert in der \_ Spalte Dateianwendung der [MsiAssembly-Tabelle](msiassembly-table.md) NULL sein.

In den folgenden Abschnitten wird die Installation von Win32- und Common Language Runtime-Assemblys beschrieben:

-   [Installation von Win32-Assemblys](installation-of-win32-assemblies.md)
-   [Installation von Common Language Runtime-Assemblys](installation-of-common-language-runtime-assemblies.md)

 

 



