---
title: Katalogcompiler für Onlineshops vom Typ 1
description: Katalogcompiler für Onlineshops vom Typ 1
ms.assetid: 49c03d3b-3381-4663-83c8-5bc8fa70f7c3
keywords:
- Windows Media Player,Katalogcompiler
- Onlineshops,Katalogcompiler
- Typ 1 Onlineshops,Katalogcompiler
- Windows Media Player Onlineshops,catcomp.exe
- Onlineshops,catcomp.exe
- Geben Sie 1 Onlineshops ein, catcomp.exe
- Katalogcompiler
- catcomp.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2764da5e19c84145bd0a11127aebc8f518031744626ca1b41c75c43c6e10093f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864210"
---
# <a name="catalog-compiler-for-type-1-online-stores"></a>Katalogcompiler für Onlineshops vom Typ 1

Der Katalogcompiler (catcomp.exe) ist ein Befehlszeilentool, das von Onlineshops vom Typ 1 verwendet wird, um den Satz von TSV-Dateien (Tab-Separated Value), die die Katalogdaten des Onlineshops enthalten, in einen komprimierten Katalog zu kompilieren, der von Windows Media Player heruntergeladen werden kann. Der Katalogcompiler kompiliert auch Katalogupdatedateien, die nur die Kataloginformationen enthalten, die sich seit dem letzten Katalogupdate geändert haben.

Die komprimierten Katalogdateien oder Katalogupdatedateien sollten Windows Media Player zum Download in der Implementierung von [IWMPContentPartner::GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl)des Onlineshop-Plug-Ins bereitgestellt werden.

Allgemeine Aufgaben

-   [Kompilieren eines vollständigen Katalogs aus TSV-Dateien](compiling-a-full-catalog-from-tsv-files.md)
-   [Kompilieren eines Katalogupdates aus vollständigen Katalogen](compiling-a-catalog-update-from-full-catalogs.md)

Diagnoseaufgaben

-   [Anzeigen der Hilfe](displaying-help.md)
-   [Abrufen von Kataloginformationen](retrieving-catalog-information.md)
-   [Anwenden eines Updates auf einen Katalog](applying-an-update-to-a-catalog.md)

 

 




