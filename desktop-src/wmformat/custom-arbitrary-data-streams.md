---
title: Benutzerdefinierte beliebige Datenströme
description: Benutzerdefinierte beliebige Datenströme
ms.assetid: 23e93b5d-719f-47dc-9f3b-7bef14161b90
keywords:
- Windows Media-Format-SDK, benutzerdefinierte beliebige Datenströme
- Advanced Systems Format (ASF), benutzerdefinierte beliebige Datenströme
- ASF (Advanced Systems Format), benutzerdefinierte beliebige Datenströme
- Windows Media-Format-SDK, Streams
- Advanced Systems Format (ASF), Streams
- ASF (Advanced Systems Format), Streams
- benutzerdefinierte beliebige Datenströme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c031e6d02864cae326a9cadb48577e1ea76c0e1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341681"
---
# <a name="custom-arbitrary-data-streams"></a>Benutzerdefinierte beliebige Datenströme

Sie können einen Stream in einer ASF-Datei erstellen, die beliebige Daten enthalten soll. Wenn keiner der unterstützten Streamtypen Ihren Anforderungen entspricht, müssen Sie einen beliebigen Datenstrom verwenden. Das Writer-Objekt verarbeitet einen beliebigen Datenstrom genauso wie alle nicht komprimierten Datenströme. die Beispiele werden packetisiert und mit den Beispielen aus anderen Streams im Daten Abschnitt der Datei kombiniert. Natürlich kann nur eine Leseanwendung, die speziell für den Umgang mit Ihrem beliebigen Typ programmiert wurde, die Daten verarbeiten, nachdem Sie vom Lese Objekt bereitgestellt wurde.

Eine häufige Verwendung beliebiger Datenströme ist für Mediendaten vorgesehen, die mit einem Drittanbieter-Codec codiert werden. Da die Objekte dieses SDK nicht direkt mit Codecs von Drittanbietern interagieren, muss die Schreib Anwendung die Beispiele mit dem Codierungs Teil des Codecs verarbeiten und die komprimierten Beispiele an den Writer übergeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Beliebige Streams**](arbitrary-streams.md)
</dt> <dt>

[**Konfigurieren von benutzerdefinierten beliebigen Streams**](configuring-custom-arbitrary-streams.md)
</dt> </dl>

 

 




