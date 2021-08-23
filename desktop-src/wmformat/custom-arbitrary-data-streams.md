---
title: Benutzerdefinierte beliebige Streams
description: Benutzerdefinierte beliebige Streams
ms.assetid: 23e93b5d-719f-47dc-9f3b-7bef14161b90
keywords:
- Windows Medienformat-SDK, benutzerdefinierte beliebige Datenströme
- Advanced Systems Format (ASF), benutzerdefinierte beliebige Datenströme
- ASF (Advanced Systems Format), benutzerdefinierte beliebige Datenströme
- Windows Medienformat-SDK,Streams
- Advanced Systems Format (ASF),streams
- ASF (Advanced Systems Format), Streams
- Benutzerdefinierte beliebige Datenströme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde40c7283620aba9c0bbdd0a1b376538ce7e4f22ac12e9fcdfe78d75195a516
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027938"
---
# <a name="custom-arbitrary-data-streams"></a>Benutzerdefinierte beliebige Streams

Sie können einen Stream in einer ASF-Datei erstellen, der beliebige Arten von Daten enthält. Wenn keiner der unterstützten Streamtypen Ihren Anforderungen entspricht, müssen Sie einen beliebigen Datenstrom verwenden. Das Writer-Objekt verarbeitet einen beliebigen Datenstrom genauso wie jeden unkomprimierten Stream. Die Beispiele werden paketiert und mit den Beispielen aus anderen Datenströmen im Datenabschnitt der Datei kombiniert. Natürlich kann nur eine Leseanwendung, die speziell für den Umgang mit Ihrem beliebigen Typ programmiert wurde, die Daten verarbeiten, nachdem sie vom Leseobjekt übermittelt wurden.

Eine häufige Verwendung beliebiger Datenströme ist die Verwendung von Mediendaten, die mithilfe eines Drittanbietercodecs codiert werden. Da die Objekte dieses SDK nicht direkt mit Codecs von Drittanbietern interagieren, muss Ihre Schreiben-Anwendung die Beispiele mit dem Codierungsteil des Codecs verarbeiten und die komprimierten Beispiele an den Writer übergeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Beliebige Streams**](arbitrary-streams.md)
</dt> <dt>

[**Konfigurieren benutzerdefinierter Streams**](configuring-custom-arbitrary-streams.md)
</dt> </dl>

 

 




