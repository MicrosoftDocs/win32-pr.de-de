---
description: Im Laufe der Zeit sind möglicherweise verschiedene Versionen für TAPI-Anwendungen, TAPI und die Dienstanbieter vorhanden.
ms.assetid: 39b16328-931e-4d75-a6ec-1edc97f1a287
title: Versionsaushandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beffff7ceeb90ccf419e138986562ca90f83c204
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960534"
---
# <a name="version-negotiation"></a>Versionsaushandlung

Im Laufe der Zeit sind möglicherweise verschiedene Versionen für TAPI-Anwendungen, TAPI und die Dienstanbieter vorhanden. Die optimale Interoperabilität einer TAPI-Anwendung erfordert nicht nur die TAPI-Version der Anwendung, sondern auch die TAPI-dll, die TAPISVR-Version und die Dienstanbieter Version.

Wenn keine ordnungsgemäße Versions Aushandlung durchzuführen ist, kann dies zu schwerwiegenden Problemen führen. Beispielsweise verfügen einige stark verwendete Strukturen über Datenmember, die von einer Version zur nächsten hinzugefügt werden. Wenn die Struktur Größe nicht mit der von der Anwendung oder TAPI erwarteten Größe identisch ist, reichen die Konsequenzen von Speicher Verlusten bis hin zu zeitweiligen AVS.

Weitere Informationen finden Sie unter [TAPI-Versions](./tapi-versioning.md)Verwaltung.

**TAPI 2. x:** Anwendungen aushandeln bei " [**lineinitializeex**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa)" mit TAPI und TAPISVR. Anwendungen führen eine Geräte Aushandlung mit Dienstanbietern durch, indem Sie für jede Zeile, die von der Anwendung verwendet werden kann, [**lineNegotiateAPIVersion**](/windows/win32/api/tapi/nf-tapi-linenegotiateapiversion) aufrufen.

**TAPI 3. x:** Es ist nicht erforderlich, eine Versions Aushandlung auszuführen. Sie können jedoch [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) verwenden, um zu bestimmen, ob eine Schnittstelle in Ihrer Version verfügbar ist.

 

 
