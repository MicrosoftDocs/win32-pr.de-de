---
description: WMI implementiert eine Technik, die es ermöglicht, dass mehrere lokalisierte Versionen derselben Klasse im Repository gespeichert werden.
ms.assetid: 01e1cee5-d882-45b6-ac93-68533c2c6c9d
ms.tgt_platform: multiple
title: Lokalisieren von WMI-Klassen Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa9f1a7e34c3ba230655ebba4c070981a8dab901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348398"
---
# <a name="localizing-wmi-class-information"></a>Lokalisieren von WMI-Klassen Informationen

WMI implementiert eine Technik, die es ermöglicht, dass mehrere lokalisierte Versionen derselben Klasse im Repository gespeichert werden.

Die Klassendefinition ist in die folgenden Versionen unterteilt:

-   Eine sprachneutrale Version, die nur eine einfache Klassendefinition enthält.
-   Eine sprachspezifische Version, die lokalisierte Informationen enthält, z. b. Eigenschafts Beschreibungen, die für ein Gebiets Schema spezifisch sind.

Die sprachspezifischen Klassendefinitionen werden in einem untergeordneten Namespace unterhalb des Namespaces gespeichert, der eine sprachneutrale Grundklassen Definition enthält.

Wenn Sie eine lokalisierte Klassendefinition für ein bestimmtes Gebiets Schema anfordern, kombiniert WMI die grundlegende Klassendefinition und die lokalisierten Klassen Informationen, um eine komplette lokalisierte Klasse zu bilden. Sie können eine lokalisierte Version einer WMI-Klasse erhalten, indem Sie beim Herstellen einer Verbindung mit WMI ein Gebiets Schema angeben und ein Flag festlegen, das angibt, dass lokalisierte Informationen angezeigt werden sollen. Die Informationen werden dann von WMI aus den sprach neutralen und sprachspezifischen Versionen der Klassendefinition zusammengeführt, um eine lokalisierte Klasse zu bilden.

WMI-Klassen, die lokalisierte Informationen enthalten, werden mit dem **Zusatz** Qualifizierer gekennzeichnet und als geänderte Klassen bezeichnet. eine Klasse unterstützt lokalisierte Informationen, wenn Sie diesen Qualifizierer aufweist. Sie können bestimmen, für welches Gebiets Schema die Klasse lokalisiert wurde, indem Sie nach einem anderen Qualifizierer namens [**locale**](swbemobjectpath-locale.md)suchen. Der Gebiets Schema Qualifizierer enthält eine Lokalisierungs-ID (Windows LCID), die ein Gebiets Schema identifiziert. Beispielsweise lautet das Gebiets Schema für amerikanisches Englisch 0x409. Wenn ein Qualifizierer in einer geänderten Klasse lokalisierte Informationen enthält, enthält er die **geänderte** qualifiziererkonfiguration.

Die WMI-Lokalisierung umfasst die folgenden Aufgaben:

-   [Erstellen von lokalisierten Klassendefinitionen](creating-localized-class-definitions.md)
-   [Kompilieren lokalisierter MOF-Dateien](compiling-localized-mof-files.md)
-   [Lokalisieren von Eigenschafts Werten](localizing-property-values.md)
-   [Abrufen von geänderten Klassen](retrieving-amended-classes.md)

Weitere Informationen finden Sie unter [Überlegungen zur geänderten Klasse](amended-class-considerations.md).

 

 



