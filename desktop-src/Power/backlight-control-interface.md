---
description: Die Backlight-Steuerungsschnittstelle ist eine standardisierte IOCTL-Schnittstelle zum Steuern der Helligkeit des BACKEND-Hintergrundlichts.
ms.assetid: edf2b7ed-2676-483a-80ba-f148951e0e58
title: Backlight-Steuerelementschnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18a6a82cede03d18f9d237bab09a590f9bcdc0da86651dacd0912357c32d36ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143723"
---
# <a name="backlight-control-interface"></a>Backlight-Steuerelementschnittstelle

Die Backlight-Steuerungsschnittstelle ist eine standardisierte IOCTL-Schnittstelle zum Steuern der Helligkeit des BACKEND-Hintergrundlichts.

Anwendungen, die eine programmgesteuerte Steuerung der Helligkeit des Hintergrundlichts erfordern oder steuerelemente für den Benutzer bereitstellen, sollten diese Schnittstelle anstelle einer proprietären Schnittstelle verwenden. Andernfalls kann das System die aktuelle Hardware-Helligkeit nicht abfragen und wird möglicherweise nicht mehr synchronisiert.

Der erste Schritt besteht darin, das Gerät mithilfe des [**IOCTL \_ VIDEO QUERY SUPPORTED \_ \_ \_ BRIGHTNESS-Steuerelementcodes**](ioctl-video-query-supported-brightness.md) nach der unterstützten Helligkeit abzufragen. Dieser Vorgang gibt einen Puffer zurück, der die verfügbaren Helligkeitsstufen angibt. Als Nächstes können Sie das Gerät mithilfe des [**IOCTL \_ VIDEO QUERY DISPLAY \_ \_ \_ BRIGHTNESS-Steuerelementcodes**](ioctl-video-query-display-brightness.md) nach der aktuellen Helligkeit der Anzeige abfragen. Dieser Vorgang gibt die aktuellen Einstellungen für die Abwechselnde Aktuelle Helligkeit (AC), die Helligkeit des direkten Stroms (DC) und den Energiezustand zurück.

Um die Helligkeit der Anzeige zu ändern, verwenden Sie den [**IOCTL \_ VIDEO SET DISPLAY \_ \_ \_ BRIGHTNESS-Steuercode.**](ioctl-video-set-display-brightness.md) Sie können die Ac-Helligkeit, die DC-Helligkeit oder beides festlegen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Energieverwaltung](about-power-management.md)
</dt> </dl>

 

 



