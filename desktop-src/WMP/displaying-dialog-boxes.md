---
title: Anzeigen von Dialog Feldern
description: Anzeigen von Dialog Feldern
ms.assetid: 637555af-0a36-4aee-908f-496b52f7bd78
keywords:
- Windows Media Player Online Stores, Anzeigen von Dialogfeldern
- Online Stores, Anzeigen von Dialogfeldern
- Typ 1 Online Stores, Anzeigen von Dialogfeldern
- Windows Media Player Online Stores, Dialogfelder
- Online Stores, Dialogfelder
- Typ 1 Online Stores, Dialogfelder
- Anzeigen von Dialogfeldern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ebe008a6c3eac872edea497dc9d50da408aa7eb
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723512"
---
# <a name="displaying-dialog-boxes"></a>Anzeigen von Dialog Feldern

Der Online Shop kann Dialogfelder über Windows Media Player aufrufen. Um dies zu erreichen, müssen Sie im Skriptcode der Ermittlungs Seite " [extern. ShowPopup](external-showpopup.md) " aufrufen und einen benutzerdefinierten Indexwert bereitstellen, der das anzuzeigende Dialogfeld darstellt. Dieser Indexwert ist nur für den Online Store-Code von Bedeutung. Dieser Wert wird von Windows Media Player nicht interpretiert. Windows Media Player ruft dann [iwmpcontentpartner:: getiteminfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) \_ auf und übergibt g sziteminfo \_ popupurl für den *bstrinfoname* -Parameter und die Indexnummer für den *pContext* -Parameter. Das Plug-in gibt dann einen **BSTR** -Wert zurück, der die URL der Webseite enthält, die im Dialogfeld angezeigt werden soll, und der Player zeigt das Dialogfeld an.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmier Handbuch für den Typ 1 Online Stores**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




