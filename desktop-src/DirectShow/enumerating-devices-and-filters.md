---
description: Aufzählen von Geräten und Filtern
ms.assetid: 334bba2a-7477-4115-9ce0-d4495c1fc290
title: Aufzählen von Geräten und Filtern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a53f4a36e2bf994cfeab34a49444d104b2213a839bb1fa8bd2aa4d70e0003b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401774"
---
# <a name="enumerating-devices-and-filters"></a>Aufzählen von Geräten und Filtern

Manchmal muss eine Anwendung einen bestimmten Filter auf dem System des Benutzers finden. Beispielsweise kann eine Videoerfassungsanwendung eine Liste der verfügbaren Erfassungsgeräte anzeigen. Da DirectShow eine komponentenbasierte Architektur verwendet, können Sie zur Entwurfszeit nicht wissen, welche Filter auf dem System des Benutzers installiert sind. Dies gilt insbesondere für Filter, die Hardwaregeräte darstellen. DirectShow bietet zwei Komponenten, die registrierte Filter suchen:

-   Der [Systemgeräte-Enumerator](system-device-enumerator.md) sucht filter nach seiner Kategorie.
-   Die [Filterzuordnung sucht](filter-mapper.md) Filter gemäß den von der Anwendung angegebenen Suchkriterien.

Die in diesem Abschnitt erläuterten Enumeratoren folgen der Standardform, die von COM-Enumerationsschnittstellen verwendet wird. Weitere Informationen finden Sie im Thema "IEnumXXXX" im Microsoft Platform Software Development Kit (SDK).

Dieser Abschnitt enthält die folgenden Themen:

-   [Verwenden des Systemgeräte-Enumerators](using-the-system-device-enumerator.md)
-   [Verwenden der Filterzuordnung](using-the-filter-mapper.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grundlegende DirectShow-Aufgaben](basic-directshow-tasks.md)
</dt> </dl>

 

 



