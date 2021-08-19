---
description: Nachdem Sie eine Snap-In-Erweiterung für Anlagen erstellt haben, müssen Sie sie registrieren, damit die MMC und die Sicherheitskonfigurations-Snap-Ins diese suchen und verwenden können.
ms.assetid: 176a658c-b1fd-40c5-a2ac-c9a2b7060c55
title: Registrieren einer Snap-In-Erweiterung für Anlagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7af8b586f0071a5718b420612fd552d578bf30bb083cca45a43f38198e1aee7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005018"
---
# <a name="registering-an-attachment-snap-in-extension"></a>Registrieren einer Snap-In-Erweiterung für Anlagen

Nachdem Sie eine Snap-In-Erweiterung für Anlagen erstellt haben, müssen Sie sie registrieren, damit die MMC und die Sicherheitskonfigurations-Snap-Ins diese suchen und verwenden können.

Ihr Anlagen-Snap-In muss den Namespace der Sicherheitskonfigurations-Snap-Ins erweitern, indem ein eigener Knoten hinzugefügt wird, wie im folgenden Verfahren beschrieben.

**So installieren und registrieren Sie die Snap-In-Erweiterung für Anlagen**

1.  Registrieren Sie die Snap-In-Erweiterung unter dem folgenden Registrierungsschlüssel. Erstellen Sie keinen StandAlone-Schlüssel unter dem Snap-In. Erweiterungen für Anlagen-Snap-Ins dürfen nur Erweiterungen sein.

    ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             MMC
                SnapIns
    ```

2.  Registrieren Sie die Snap-In-Erweiterung für Anlagen unter den folgenden Unterschlüsseln. Dies kann als Teil ihrer **DllRegisterServer-** und **DllUnregisterServer-Funktionsimplementierung** erfolgen.

    [Namespace "Sicherheitsvorlagen":](security-templates.md)

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

    [Sicherheitskonfigurations- und Analysenamespace:](security-configuration-and-analysis.md)

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

 

 



