---
title: Audiodatenströme
description: Audiodatenströme
ms.assetid: 7bb39c48-5d0b-483d-83ee-946adfc9724f
keywords:
- Windows Media Player Online Stores, Audiostreams
- Online Stores, Audiostreams
- Typ 1 Online Stores, Audiostreams
- Windows Media Player Online Stores, Streams von Musik Servern
- Online Stores, Streams von Musik Servern
- Geben Sie 1 Online Stores, Streams von Musik Servern ein.
- Windows Media Player Online Stores, Music Server Streams
- Online Stores, Music Server Streams
- Typ 1 Online Stores, Music Server Streams
- Audiodatenströme
- Musik-Serverdaten Ströme
- Streams von Musik Servern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7164a703417e2efb8e32b2632890972957f7adf7
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038581"
---
# <a name="audio-streams"></a>Audiodatenströme

Online Stores können Musik als Stream von einem Musikserver bereitstellen. Dies ist nützlich für das Bereitstellen von Beispielen, speziellen Aktions Artikeln oder das ermöglichen von Abonnement Benutzern, Musik zu nutzen, ohne den Inhalt herunterladen zu müssen. Es ist üblich, dass die URL des Streams nicht als Teil des musikkatalogs gespeichert wird, sondern stattdessen die URL vor der Wiedergabe basierend auf der ID des Titels aufgelöst wird. Um dies zu ermöglichen, ruft Windows Media Player [iwmpcontentpartner:: getstreamingurl](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getstreamingurl) auf und stellt den Streamingtyp (als [wmpstreamingtype](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmpstreamingtype) -Enumerationswert) und die ID für den Datenstrom bereit. Das Plug-in gibt die URL für den Datenstrom über den *pbstrinurl* -Parameter zurück.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zu Typ 1 Online Stores**](about-type-1-online-stores.md)
</dt> </dl>

 

 




