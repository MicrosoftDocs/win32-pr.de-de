---
title: Katalog Compiler für Typ 1-Online Speicher
description: Katalog Compiler für Typ 1-Online Speicher
ms.assetid: 49c03d3b-3381-4663-83c8-5bc8fa70f7c3
keywords:
- Windows Media Player Online Stores, Katalog Compiler
- Online Stores, Katalog Compiler
- Typ 1 Online Stores, Katalog Compiler
- Windows Media Player Online Stores catcomp.exe
- Online Stores, catcomp.exe
- Geben Sie 1 Online Stores, catcomp.exe
- Katalog Compiler
- catcomp.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4c54ffd054c5e72b04ddd32eef12c7fe6b6cc89
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106341501"
---
# <a name="catalog-compiler-for-type-1-online-stores"></a>Katalog Compiler für Typ 1-Online Speicher

Der Katalog Compiler (catcomp.exe) ist ein Befehlszeilen Tool, das vom Typ 1 Online Stores verwendet wird, um den Satz von TSV-Dateien, die die Katalogdaten des Online Stores enthalten, in einen komprimierten Katalog zu kompilieren, der von Windows Media Player heruntergeladen werden kann. Der Katalog Compiler kompiliert auch Katalog Update Dateien, die nur die Katalog Informationen enthalten, die seit dem letzten Katalog Update geändert wurden.

Die komprimierten Katalogdateien oder Katalog Update Dateien sollten für Windows-Media Player bereitgestellt werden, um Sie in der Implementierung von [iwmpcontentpartner:: getcatalogurl](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl)des Online Store-Plug-ins herunterzuladen.

Allgemeine Aufgaben

-   [Kompilieren eines vollständigen Katalogs aus TSV-Dateien](compiling-a-full-catalog-from-tsv-files.md)
-   [Kompilieren eines Katalog Updates aus vollständigen Katalogen](compiling-a-catalog-update-from-full-catalogs.md)

Diagnose Tasks

-   [Anzeigen der Hilfe](displaying-help.md)
-   [Abrufen von Katalog Informationen](retrieving-catalog-information.md)
-   [Anwenden eines Updates auf einen Katalog](applying-an-update-to-a-catalog.md)

 

 




