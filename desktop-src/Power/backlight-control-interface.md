---
description: Die Timeout-Steuerungs Schnittstelle ist eine standardisierte ioctl-Schnittstelle zum Steuern der Helligkeit des LCD-Timeout.
ms.assetid: edf2b7ed-2676-483a-80ba-f148951e0e58
title: Backlight-Steuerungs Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ecbcc3d635d120c1049f8ec586d7296a953dfac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368746"
---
# <a name="backlight-control-interface"></a>Backlight-Steuerungs Schnittstelle

Die Timeout-Steuerungs Schnittstelle ist eine standardisierte ioctl-Schnittstelle zum Steuern der Helligkeit des LCD-Timeout.

Anwendungen, die eine programmgesteuerte Steuerung der Hintergrund Helligkeit erfordern oder Steuerelemente für den Benutzer bereitstellen sollten, sollten diese Schnittstelle anstelle einer proprietären Schnittstelle verwenden. Andernfalls kann das System die aktuelle Hardware Helligkeit nicht Abfragen und wird möglicherweise nicht synchronisiert.

Der erste Schritt besteht darin, das Gerät mit der von der [**IOCTL- \_ Video \_ Abfrage \_ unterstützten \_ Helligkeits**](ioctl-video-query-supported-brightness.md) Steuerungs Code auf die unterstützte Helligkeit abzufragen. Dieser Vorgang gibt einen Puffer zurück, der die verfügbaren Helligkeits Ebenen angibt. Als nächstes können Sie das Gerät mit dem Bildschirm Helligkeit-Steuercode der [**IOCTL- \_ Video \_ \_ \_ Abfrage**](ioctl-video-query-display-brightness.md) auf die aktuelle Anzeige Helligkeit Abfragen. Mit diesem Vorgang werden die aktuellen Einstellungen für die abwechselnde Helligkeit (AC), die Current Current (DC)-Helligkeit und den Energiezustand zurückgegeben.

Um die Anzeige Helligkeit zu ändern, verwenden Sie den [**IOCTL- \_ \_ Videosatz \_ Anzeige \_ Helligkeit**](ioctl-video-set-display-brightness.md) -Steuerungs Code. Sie können die Wechsel stromhelligkeit, die Domänen Controller Helligkeit oder beides festlegen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Energie Verwaltung](about-power-management.md)
</dt> </dl>

 

 



