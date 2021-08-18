---
title: Kontextmenüs
description: Kontextmenüs
ms.assetid: d1ea899a-9087-4502-8825-5cef1a87ef03
keywords:
- Windows Media Player,Kontextmenüs
- Onlineshops,Kontextmenüs
- Geben Sie 1 Onlineshops,Kontextmenüs ein.
- Windows Media Player,benutzerdefinierte Kontextmenüs
- Onlineshops,benutzerdefinierte Kontextmenüs
- Geben Sie 1 Onlineshops,benutzerdefinierte Kontextmenüs ein.
- Kontextmenüs
- Benutzerdefinierte Kontextmenüs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6ad3bba5863f83b5f324821ec0904e7ef4c5881c7f10b9214eebde1081b217d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119349"
---
# <a name="context-menus"></a>Kontextmenüs

Onlineshops können benutzerdefinierte Kontextmenüs bereitstellen. Hierzu implementiert das Onlineshop-Plug-In die [IWMPContentPartner::GetCommands-Methode.](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcommands) Windows Media Player diese Methode auf, um Informationen über den Speicherort auf der Benutzeroberfläche zu geben, an dem das Kontextmenü angezeigt wird (wo der Benutzer mit der rechten Maustaste geklickt hat). Das Plug-In gibt ein Array von [WMPContextMenuInfo-Strukturen](/previous-versions/windows/desktop/api/contentpartner/ns-contentpartner-wmpcontextmenuinfo) zurück, die jedes Kontextmenüelement beschreiben, einschließlich einer Befehls-ID für jedes.

Nachdem Windows Media Player Array abgerufen hat, verwendet der Player das Array, um das Kontextmenü zu erstellen, das dem Benutzer angezeigt wird. Wenn der Benutzer im Kontextmenü auf ein Element klickt, ruft der Player [IWMPContentPartner::InvokeCommand](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-invokecommand)auf und übergibt die dem Menüelement zugeordnete Befehls-ID über den *parameter dwCommandID.* Der Player übergibt auch einen Bibliotheksspeicherortwert und ein Array von IDs, das die Elemente darstellt, auf die das Menü aufgerufen wurde, z. B. ein Array von Track-IDs. Mithilfe dieser Informationen kann das Plug-In einen beliebigen geeigneten Prozess als Reaktion auf den Mausklick des Benutzers starten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zu Onlineshops vom Typ 1**](about-type-1-online-stores.md)
</dt> </dl>

 

 




