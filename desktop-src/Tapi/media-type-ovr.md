---
description: Der Medientyp (oder Modus) eines Geräts beschreibt den Typ der Informationen, die ausgetauscht werden können, z. b. interaktive Stimme. Ein bestimmtes Gerät kann möglicherweise nur einen Medientyp verarbeiten, oder es kann mit einem Bereich von Typen umzugehen.
ms.assetid: fccf85e9-3889-4ebc-b1bf-a60e27ab4586
title: Medientyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 369954a4b0d1f78e12f6ea42bcc2ec61ca425012
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106354272"
---
# <a name="media-type"></a>Medientyp

Der *Medientyp* (oder Modus) eines Geräts beschreibt den Typ der Informationen, die ausgetauscht werden können, z. b. interaktive Stimme. Ein bestimmtes Gerät kann möglicherweise nur einen Medientyp verarbeiten, oder es kann mit einem Bereich von Typen umzugehen.

Dienstanbieter machen den Medientyp oder die Typen verfügbar, die von den von Ihnen kontrollierten Geräten unterstützt werden. Anwendungen Fragen den Medientyp ab und verwenden diese Informationen dann, um eine geeignete Adresse auszuwählen, auf der eine Sitzung initiiert werden soll. Die Anwendungs Antwort auf eine angebotene Sitzung kann auch für den Medientyp als Prädikat vorgegeben werden.

Eine bestimmte Kommunikationssitzung bzw. ein angegebener-Rückruf kann mehrere Medientypen einschließen. Weitere Informationen finden Sie unter Medientyp für eine Sitzung.

**TAPI 2. x:** Weitere Informationen finden Sie unter [**linegetaddresscaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps), **dwavailablemediamodes** -Member der [**lineaddresscaps**](/windows/win32/api/tapi/ns-tapi-lineaddresscaps) -Struktur, auf die von *lpaddresscaps* und [linemediamode- \_ Konstanten](./linemediamode--constants.md)verwiesen wird.

**TAPI 3. x:** Siehe [**itterminal:: get \_ mediaType**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_mediatype), [tapimediatype \_ Konstanten](tapimediatype--constants.md).
