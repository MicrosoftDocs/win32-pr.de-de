---
description: WMI implementiert eine Technik, mit der mehrere lokalisierte Versionen derselben Klasse im Repository gespeichert werden können.
ms.assetid: 01e1cee5-d882-45b6-ac93-68533c2c6c9d
ms.tgt_platform: multiple
title: Lokalisieren von WMI-Klasseninformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c3784128c48282d05620faf470217b195b26614d81b5b847e7a7a8ad6b9252f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131212"
---
# <a name="localizing-wmi-class-information"></a>Lokalisieren von WMI-Klasseninformationen

WMI implementiert eine Technik, mit der mehrere lokalisierte Versionen derselben Klasse im Repository gespeichert werden können.

Die Klassendefinition ist in die folgenden Versionen unterteilt:

-   Eine sprachneutrale Version, die nur eine grundlegende Klassendefinition enthält.
-   Eine sprachspezifische Version, die lokalisierte Informationen enthält, z. B. Eigenschaftenbeschreibungen, die für ein Gebietsschema spezifisch sind.

Die sprachspezifischen Klassendefinitionen werden in einem untergeordneten Namespace unter dem Namespace gespeichert, der eine sprachneutrale grundlegende Klassendefinition enthält.

Wenn Sie eine lokalisierte Klassendefinition für ein bestimmtes Gebietsschema anfordern, kombiniert WMI die grundlegende Klassendefinition und die lokalisierten Klasseninformationen, um eine vollständige lokalisierte Klasse zu bilden. Sie können eine lokalisierte Version einer WMI-Klasse abrufen, indem Sie ein Gebietsschema angeben, wenn Sie eine Verbindung mit WMI herstellen, und ein Flag festlegen, das angibt, dass Sie lokalisierte Informationen wünschen. WMI führt dann die Informationen aus den sprachneutralen und den sprachspezifischen Versionen der Klassendefinition zusammen, um eine lokalisierte Klasse zu bilden.

WMI-Klassen, die lokalisierte Informationen enthalten, werden mit dem **Zusatzqualifizierer** markiert und als geänderte Klassen bezeichnet. eine Klasse unterstützt lokalisierte Informationen, wenn sie über diesen Qualifizierer verfügt. Sie können bestimmen, für welches Gebietsschema die Klasse lokalisiert wurde, indem Sie nach einem anderen Qualifizierer namens [**Gebietsschema**](swbemobjectpath-locale.md)suchen. Der Gebietsschemaqualifizierer enthält einen Lokalisierungsbezeichner (Windows LCID), der ein Gebietsschema identifiziert. Das Gebietsschema für amerikanisches Englisch ist beispielsweise 0x409. Wenn ein Qualifizierer in einer geänderten Klasse lokalisierte Informationen enthält, enthält er die **geänderte** Qualifiziererart.

Die WMI-Lokalisierung umfasst die folgenden Aufgaben:

-   [Erstellen lokalisierter Klassendefinitionen](creating-localized-class-definitions.md)
-   [Kompilieren lokalisierter MOF-Dateien](compiling-localized-mof-files.md)
-   [Lokalisieren von Eigenschaftswerten](localizing-property-values.md)
-   [Abrufen von geänderten Klassen](retrieving-amended-classes.md)

Weitere Informationen finden Sie unter [Amended Class Considerations](amended-class-considerations.md).

 

 



