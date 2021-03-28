---
description: Ab Windows 7 werden Cascading-Menüs über den Registrierungs Eintrag Unterbefehle, den extendedsubcommandskey-Registrierungs Eintrag oder die IExplorerCommand-Schnittstelle erstellt.
title: Erstellen von statischen kaskadierenden Menüs
ms.topic: article
ms.date: 05/31/2018
ms.assetid: E3A6F174-BE53-48EF-AE9B-A3F297E91B95
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d812b4d3d2fb0754002cb37d72718e4fe861ce15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104569035"
---
# <a name="creating-static-cascading-menus"></a>Erstellen von statischen kaskadierenden Menüs

In Windows 7 und höher wird die Cascading-Menü Implementierung durch Registrierungs Einstellungen unterstützt. Vor Windows 7 war die Erstellung von kaskadierenden Menüs nur durch die Implementierung der [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) -Schnittstelle möglich. In Windows 7 und höher sollten Sie nur auf Component Object Model Code basierte Lösungen (com) zugreifen, wenn die statischen Methoden nicht ausreichen.

Der folgende Screenshot zeigt ein Beispiel für ein Cascading-Menü.

![Screenshot mit einem Beispiel für ein Cascading-Menü](images/file-assoc/filecascademenu2ndex.png)

In Windows 7 und höher gibt es drei Möglichkeiten, Kaskadierende Menüs zu erstellen, die in den folgenden Abschnitten beschrieben werden.

-   [Erstellen von kaskadierenden Menüs mit dem Registrierungs Eintrag "Unterbefehle"](how-to--create-cascading-menus-with-the-subcommands-registry-entry.md)
-   [Erstellen von kaskadierenden Menüs mit dem Registrierungs Eintrag "extendedsubcommandskey"](how-to-create-cascading-menus-with-the-extendedsubcommandskey-registry-entry.md)
-   [Erstellen von kaskadierenden Menüs mit der IExplorerCommand-Schnittstelle](how-to-create-cascading-menus-with-the-iexplorercommand-interface.md)

 

 
