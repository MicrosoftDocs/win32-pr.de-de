---
title: Kontextmenüs
description: Kontextmenüs
ms.assetid: d1ea899a-9087-4502-8825-5cef1a87ef03
keywords:
- Windows Media Player Online Stores, Kontextmenüs
- Online Stores, Kontextmenüs
- Typ 1 Online Stores, Kontextmenüs
- Windows Media Player Online Stores, benutzerdefinierte Kontextmenüs
- Online Stores, benutzerdefinierte Kontextmenüs
- Typ 1 Online Stores, benutzerdefinierte Kontextmenüs
- Kontextmenüs
- Benutzerdefinierte Kontextmenüs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ba3ed52b408651607cb1f6dab1a04f53282d3ef
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389838"
---
# <a name="context-menus"></a>Kontextmenüs

Online Stores können benutzerdefinierte Kontextmenüs bereitstellen. Hierzu implementiert das Online Store-Plug-in die Methode [iwmpcontentpartner:: GetCommands](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcommands) . Windows Media Player ruft diese Methode auf, um Informationen über den Speicherort in der Benutzeroberfläche bereitzustellen, auf der das Kontextmenü angezeigt wird (in dem der Benutzer mit der rechten Maustaste geklickt hat). Das Plug-in gibt ein Array von [wmpcontextmenuinfo](/previous-versions/windows/desktop/api/contentpartner/ns-contentpartner-wmpcontextmenuinfo) -Strukturen zurück, die die einzelnen Kontextmenü Elemente einschließlich einer Befehls-ID für jede beschreiben.

Nachdem der Windows-Media Player das Array abgerufen hat, verwendet der Player das Array, um das Kontextmenü zu erstellen, das der Benutzer sieht. Wenn der Benutzer im Kontextmenü auf ein Element klickt, ruft der Player [iwmpcontentpartner:: InvokeCommand](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-invokecommand)auf und übergibt dabei die Befehls-ID, die dem Menü Element über den *dwcommandid* -Parameter zugeordnet ist. Der Player übergibt außerdem einen Bibliotheks Speicherort Wert und ein Array von IDs, die die Elemente darstellen, für die das Menü aufgerufen wurde, z. b. ein Array von Track-IDs. Wenn Sie diese Informationen verwenden, kann das Plug-in jeden geeigneten Prozess als Reaktion auf den Maus Klick des Benutzers starten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zu Typ 1 Online Stores**](about-type-1-online-stores.md)
</dt> </dl>

 

 




