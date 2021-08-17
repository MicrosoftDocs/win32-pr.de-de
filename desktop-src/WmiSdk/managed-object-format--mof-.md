---
description: Managed Object Format (MOF) ist die Sprache, die zum Beschreiben von CIM-Klassen (Common Information Model) verwendet wird.
ms.assetid: 26494142-2078-4d46-a794-e43973255c2d
ms.tgt_platform: multiple
title: MOF-Datei (Managed Object Format)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ac36bd89979d6cf0de0a4d574a47a6ce7060f90e5577402eba77aa2de42bbedb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131177"
---
# <a name="managed-object-format-mof"></a>MOF-Datei (Managed Object Format)

Managed Object Format (MOF) ist die Sprache, die zum Beschreiben [*von CIM-Klassen (Common Information Model)*](gloss-c.md) verwendet wird.

WMI-Anbieter sollten neue WMI-Klassen in MOF-Dateien implementieren, die mit [**Mofcomp.exe**](mofcomp.md) in das [*WMI-Repository*](gloss-w.md)kompiliert werden. Es ist auch möglich, CIM-Klassen und -Instanzen mithilfe der [COM-API für WMI](com-api-for-wmi.md)zu erstellen und zu bearbeiten.

Ein WMI-Anbieter besteht normalerweise aus einer MOF-Datei, die die Daten- und Ereignisklassen definiert, für die der Anbieter Daten zurückgibt, und einer DLL-Datei, die den Code enthält, der Daten bereitstellt. Weitere Informationen finden Sie unter [Bereitstellen von Daten für WMI.](providing-data-to-wmi.md)

WMI-Clientskripts und -Anwendungen können Instanzen von MOF-Anbieterklassen abfragen oder Ereignisbenachrichtigungen abonnieren.

Sie können die folgenden Aufgaben mit MOF ausführen:

-   [Kompilieren von MOF-Dateien](compiling-mof-files.md)
-   [Erstellen einer Klasse](creating-a-class.md)
-   [Erstellen einer Instanz](creating-an-instance.md)
-   [Erstellen einer Methode](creating-a-method.md)
-   [Hinzufügen eines Qualifizierers](adding-a-qualifier.md)
-   [Erstellen eines Kommentars](creating-a-comment.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu WMI](about-wmi.md)
</dt> </dl>

 

 



