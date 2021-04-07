---
title: Typ 1 Online Store-Plug-in
description: Typ 1 Online Store-Plug-in
ms.assetid: 3aa74282-522b-4240-8d72-73bd3015abeb
keywords:
- Windows Media Player Online Stores, Plug-ins
- Online Stores, Plug-ins
- Typ 1 Online Stores, Plug-ins
- Windows Media Player Online Stores, iwmpcontentpartner-Schnittstelle
- Online Stores, iwmpcontentpartner-Schnittstelle
- Typ 1 Online Stores, iwmpcontentpartner-Schnittstelle
- Plug-ins, Windows Media Player Online Stores
- Plug-ins, Online Stores
- Plug-ins, Typ 1 Online Stores
- Plug-ins, iwmpcontentpartner-Schnittstelle
- Windows Media Player-Plug-ins, geben Sie 1 Online Stores ein.
- Windows Media Player-Plug-ins, Online Stores
- Windows Media Player-Plug-ins, Windows Media Player Online Stores
- Windows Media Player-Plug-ins, iwmpcontentpartner-Schnittstelle
- Iwmpcontentpartner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fe42095d08262520734603a5418ac6831ce6685
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104038690"
---
# <a name="type-1-online-store-plug-in"></a>Typ 1 Online Store-Plug-in

Um die Funktionen der Bibliotheks Integration nutzen zu können, müssen Sie vom Typ 1 Online Store-Anbieter ein Plug-in erstellen, das die [iwmpcontentpartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) -Schnittstelle implementiert. Diese Schnittstelle stellt die Methoden bereit, die von Windows Media Player aufgerufen werden, um den Online Store über Aktivitäten zu benachrichtigen, die im Player stattfinden, und um bestimmte Informationen über Online Store-Inhalte, den Katalog oder den Speicher selbst abzurufen.

Nachdem das Plug-in von Windows Media Player instanziiert wurde, ruft der Player [iwmpcontentpartner:: SetCallback](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-setcallback)auf und stellt einen Zeiger auf die **iwmpcontentpartnercallback** -Schnittstelle bereit. Diese Schnittstelle ermöglicht dem Online Shop das Ausführen von Aufrufen an Windows Media Player, um Statusinformationen bereitzustellen oder bestimmte Prozesse, z. b. das Herunterladen eines Musiktitels, zu initiieren.

Windows Media Player und das Plug-in werden in separaten Prozessen ausgeführt. Das Plug-in ist ein in-Process-Server, der im standardmäßigen dll-Ersatz dllhost.exe ausgeführt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zu Typ 1 Online Stores**](about-type-1-online-stores.md)
</dt> <dt>

[**Iwmpcontentpartner-Schnittstelle**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner)
</dt> <dt>

[**Iwmpcontentpartnercallback-Schnittstelle**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartnercallback)
</dt> </dl>

 

 




