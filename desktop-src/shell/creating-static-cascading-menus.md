---
description: Ab Windows 7 werden kaskadierenden Menüs über den Registrierungseintrag SubCommands, den Registrierungseintrag ExtendedSubCommandsKey oder die IExplorerCommand-Schnittstelle erstellt.
title: Erstellen von statischen kaskadierenden Menüs
ms.topic: article
ms.date: 05/31/2018
ms.assetid: E3A6F174-BE53-48EF-AE9B-A3F297E91B95
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 22fdc261012697affd99b5a1491ef5829fcc5329d5570ae4e3c37dcd111b457f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119456330"
---
# <a name="creating-static-cascading-menus"></a>Erstellen von statischen kaskadierenden Menüs

In Windows 7 und höher wird die Implementierung des kaskadierenden Menüs über Registrierungseinstellungen unterstützt. Vor Windows 7 war die Erstellung von kaskadierenden Menüs nur über die Implementierung der [**IContextMenu-Schnittstelle**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) möglich. In Windows 7 und höher sollten Sie nur dann Component Object Model (COM) codebasierte Lösungen verwenden, wenn die statischen Methoden nicht ausreichen.

Der folgende Screenshot enthält ein Beispiel für ein kaskadiertes Menü.

![Screenshot, der ein Beispiel für ein kaskadiertes Menü zeigt](images/file-assoc/filecascademenu2ndex.png)

In Windows 7 und höher gibt es drei Möglichkeiten zum Erstellen von kaskadierenden Menüs, die in den folgenden Abschnitten beschrieben werden.

-   [Erstellen von kaskadierenden Menüs mit dem Registrierungseintrag "SubCommands"](how-to--create-cascading-menus-with-the-subcommands-registry-entry.md)
-   [Erstellen von kaskadierenden Menüs mit dem Registrierungseintrag ExtendedSubCommandsKey](how-to-create-cascading-menus-with-the-extendedsubcommandskey-registry-entry.md)
-   [Erstellen von kaskadierenden Menüs mit der IExplorerCommand-Schnittstelle](how-to-create-cascading-menus-with-the-iexplorercommand-interface.md)

 

 
