---
description: Nachdem Sie die Erweiterungs-Snap-in-Erweiterung erstellt haben, müssen Sie diese registrieren, damit die MMC und die Sicherheitskonfigurations-Snap-Ins Sie finden und verwenden können.
ms.assetid: 176a658c-b1fd-40c5-a2ac-c9a2b7060c55
title: Registrieren einer Anlage-Snap-in-Erweiterung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7726131325433aa920ff22c9b71a4f7184000a69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106341203"
---
# <a name="registering-an-attachment-snap-in-extension"></a>Registrieren einer Anlage-Snap-in-Erweiterung

Nachdem Sie die Erweiterungs-Snap-in-Erweiterung erstellt haben, müssen Sie diese registrieren, damit die MMC und die Sicherheitskonfigurations-Snap-Ins Sie finden und verwenden können.

Das Anlagen-Snap-in muss den Namespace der Sicherheitskonfigurations-Snap-Ins erweitern, indem er einen eigenen Knoten hinzufügt, wie im folgenden Verfahren beschrieben.

**So installieren und registrieren Sie die Erweiterungs-Snap-in-Erweiterung**

1.  Registrieren Sie die Snap-in-Erweiterung unter dem folgenden Registrierungsschlüssel. Erstellen Sie keinen eigenständigen Schlüssel im-Snap-in. Erweiterungen für Anlagen-Snap-Ins dürfen nur Erweiterungen sein.

    ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             MMC
                SnapIns
    ```

2.  Registrieren Sie die Erweiterungs-Snap-in-Erweiterung unter den folgenden unter Schlüsseln. Dies kann als Teil der **DllRegisterServer** -und **DllUnregisterServer** -Funktions Implementierungen erfolgen.

    [Sicherheitsvorlagen](security-templates.md) -Namespace:

    ```
    HKLM
       SOFTWARE
          Microsoft
             MMC
                NodeTypes
                   24a7f717-1f0c-11d1-affb-00c04fb984f9
                      Extensions
                         NameSpace
    ```

    [Sicherheitskonfigurations-und Analyse-](security-configuration-and-analysis.md) Namespace:

    ```
    HKLM
       SOFTWARE
          Microsoft
             MMC
                NodeTypes
                   678050c7-1ff8-11d1-affb-00c04fb984f9
                      Extensions
                         NameSpace
    ```

 

 



