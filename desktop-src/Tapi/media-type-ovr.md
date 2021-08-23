---
description: Der Medientyp (oder -modus) eines Geräts beschreibt den Typ der Informationen, die ausgetauscht werden können, z. B. interaktive Stimme. Ein bestimmtes Gerät kann möglicherweise nur einen Medientyp oder eine Reihe von Typen verarbeiten.
ms.assetid: fccf85e9-3889-4ebc-b1bf-a60e27ab4586
title: Medientyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbf79b97adb9df491aef1ff86be62fb838246c85a45b5ce251f5c0e88df5814f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002888"
---
# <a name="media-type"></a>Medientyp

Der *Medientyp* (oder -modus) eines Geräts beschreibt den Typ der Informationen, die ausgetauscht werden können, z. B. interaktive Stimme. Ein bestimmtes Gerät kann möglicherweise nur einen Medientyp oder eine Reihe von Typen verarbeiten.

Dienstanbieter machen den Medientyp oder die Typen verfügbar, die von den von ihnen kontrollierten Geräten unterstützt werden. Anwendungen fragen den Medientyp ab und verwenden diese Informationen dann, um eine geeignete Adresse auszuwählen, unter der eine Sitzung initiiert werden soll. Die Anwendungsantwort auf eine angebotene Sitzung kann auch auf den Medientyp prädiziert sein.

Eine bestimmte Kommunikationssitzung oder ein Aufruf kann mehrere Medientypen umfassen. Weitere Informationen finden Sie unter Medientyp für eine Sitzung.

**TAPI 2.x:** Siehe [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps), **dwAvailableMediaModes-Member** der [**LINEADDRESSCAPS-Struktur,**](/windows/win32/api/tapi/ns-tapi-lineaddresscaps) auf die *von lpAddressCaps,* [LINEMEDIAMODE-Konstanten verwiesen \_ wird.](./linemediamode--constants.md)

**TAPI 3.x:** Weitere [**Informationen finden Sie unter ITTerminal::get \_ MediaType**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_mediatype), [TAPIMEDIATYPE \_ Constants](tapimediatype--constants.md).
