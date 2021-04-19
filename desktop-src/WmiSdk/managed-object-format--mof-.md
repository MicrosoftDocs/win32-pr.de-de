---
description: Managed Object Format (MOF) ist die Sprache, mit der Common Information Model (CIM)-Klassen beschrieben werden.
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
ms.openlocfilehash: 16f95c6868943a2f41c4326c341207ff26a03af6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360757"
---
# <a name="managed-object-format-mof"></a>MOF-Datei (Managed Object Format)

Managed Object Format (MOF) ist die Sprache, mit der [*Common Information Model (CIM)*](gloss-c.md) -Klassen beschrieben werden.

Die empfohlene Vorgehensweise für WMI-Anbieter, neue WMI-Klassen zu implementieren, ist in MOF-Dateien, die mithilfe von [**Mofcomp.exe**](mofcomp.md) in das [*WMI-Repository*](gloss-w.md)kompiliert werden. Es ist auch möglich, CIM-Klassen und-Instanzen mithilfe der [com-API für WMI](com-api-for-wmi.md)zu erstellen und zu bearbeiten.

Ein WMI-Anbieter besteht normalerweise aus einer MOF-Datei, die die Daten-und Ereignis Klassen definiert, für die der Anbieter Daten zurückgibt, sowie eine DLL-Datei, die den Code enthält, der Daten bereitstellt. Weitere Informationen finden Sie unter [Bereitstellen von Daten für WMI](providing-data-to-wmi.md).

WMI-Client Skripts und-Anwendungen können Instanzen von MOF-Anbieter Klassen Abfragen oder Empfangs Ereignis Benachrichtigungen abonnieren.

Mit MOF können Sie die folgenden Aufgaben ausführen:

-   [Kompilieren von MOF-Dateien](compiling-mof-files.md)
-   [Erstellen einer Klasse](creating-a-class.md)
-   [Erstellen einer Instanz](creating-an-instance.md)
-   [Erstellen einer Methode](creating-a-method.md)
-   [Fügen eines Qualifizierers](adding-a-qualifier.md)
-   [Erstellen eines Kommentars](creating-a-comment.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu WMI](about-wmi.md)
</dt> </dl>

 

 



