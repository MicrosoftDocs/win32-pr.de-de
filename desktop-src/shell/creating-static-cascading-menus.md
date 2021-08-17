---
description: Ab Windows 7 werden kaskadierende Menüs über den Registrierungseintrag SubCommands, den Registrierungseintrag ExtendedSubCommandsKey oder die IExplorerCommand-Schnittstelle erstellt.
title: Erstellen statischer kaskadierender Menüs
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
# <a name="creating-static-cascading-menus"></a>Erstellen statischer kaskadierender Menüs

In Windows 7 und höher wird die Implementierung von kaskadierenden Menüs über Registrierungseinstellungen unterstützt. Vor Windows 7 war die Erstellung von kaskadierenden Menüs nur über die Implementierung der [**IContextMenu-Schnittstelle**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) möglich. In Windows 7 und höher sollten Sie nur dann auf Component Object Model (COM)-codebasierte Lösungen zurückgreifen, wenn die statischen Methoden nicht ausreichen.

Der folgende Screenshot zeigt ein Beispiel für ein kaskadierendes Menü.

![Screenshot eines Beispiels für ein kaskadierendes Menü](images/file-assoc/filecascademenu2ndex.png)

In Windows 7 und höher gibt es drei Möglichkeiten, kaskadierende Menüs zu erstellen, die in den folgenden Abschnitten beschrieben werden.

-   [Erstellen von kaskadierenden Menüs mit dem Registrierungseintrag "SubCommands"](how-to--create-cascading-menus-with-the-subcommands-registry-entry.md)
-   [Erstellen von kaskadierenden Menüs mit dem Registrierungseintrag ExtendedSubCommandsKey](how-to-create-cascading-menus-with-the-extendedsubcommandskey-registry-entry.md)
-   [Erstellen von kaskadierenden Menüs mit der IExplorerCommand-Schnittstelle](how-to-create-cascading-menus-with-the-iexplorercommand-interface.md)

 

 
