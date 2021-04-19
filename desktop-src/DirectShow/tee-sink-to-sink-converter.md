---
description: Tee/Sink-zu-Sink-Konverter
ms.assetid: 8ee5e20c-f37a-4a9b-9382-2ed94333c6ec
title: Tee/Sink-zu-Sink-Konverter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cf85e3eb58f601273ff352a3878d352ca0f0d5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368954"
---
# <a name="teesink-to-sink-converter"></a>Tee/Sink-zu-Sink-Konverter

Der "Tee/Sink-to-Sink"-Konverter ist ein auf einem Kernel Modus basierender, ksproxy-basierter Filter. Sie wird in analogen Video-TV-Filter Diagrammen verwendet, in denen VBI-Daten gerendert oder aufgezeichnet werden. Der Filter ist mit dem [WDM-Video Erfassungs Filter](wdm-video-capture-filter.md) verbunden und bietet eine effiziente Möglichkeit, Datenströme innerhalb des Kernel Modus zu duplizieren, ohne die aufwendigen Übergänge zwischen Kernel-und Benutzermodus. Jeder empfangene Datenblock wird an alle Ausgabe Pins übermittelt, und der Downstream-Codec ist für die Suche nach bestimmten VBI-Daten zum Decodieren verantwortlich.

Der "Tee/Sink-to-Sink"-Konverter wird in der Filterkategorie "WDM-Streaming-Tee/Splitter Geräte" (am \_ kscategory- \_ Splitter) angezeigt.

Da es sich hierbei um einen Kernel Modus-Filter handelt, können Anwendungen ihn nicht direkt mithilfe von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)erstellen. Verwenden Sie stattdessen den [Enumerator "System Geräte](system-device-enumerator.md)". Weitere Informationen finden Sie unter [Erstellen von Kernel-Mode filtern](creating-kernel-mode-filters.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 
