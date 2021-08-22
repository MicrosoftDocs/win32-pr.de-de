---
description: Die ITFormatControl-Schnittstelle macht Methoden verfügbar, mit denen eine Anwendung Informationen zum Format eines Empfangs- oder Übertragungsstreams für einen Aufruf abrufen kann.
ms.assetid: a3d15561-229e-4eb6-a0ac-2d69f170bced
title: ITFormatControl-Schnittstelle (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab42a9cacdf7986a652fff4e15195fec5f6b1aa319f06b631ee992541db40b82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119406050"
---
# <a name="itformatcontrol-interface"></a>ITFormatControl-Schnittstelle

\[Diese Schnittstelle ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **ITFormatControl-Schnittstelle** macht Methoden verfügbar, mit denen eine Anwendung Informationen zum Format eines Empfangs- oder Übertragungsstreams für einen Aufruf abrufen kann.

Diese Schnittstelle wird vom [MSP H323](h323-msp.md) implementiert und nur verfügbar gemacht, wenn ein Aufruf diesen Dienstanbieter verwendet.

## <a name="members"></a>Member

Die **ITFormatControl-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITFormatControl** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ITFormatControl-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                     | Beschreibung                                                                    |
|:---------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**GetCurrentFormat**](itformatcontrol-getcurrentformat.md)               | Ruft das Medienformat des aktuellen Streams ab.<br/>                        |
| [**GetNumberOfCapabilities**](itformatcontrol-getnumberofcapabilities.md) | Ruft die Anzahl der Funktionen ab, die dem aktuellen Format zugeordnet sind.<br/> |
| [**GetStreamCaps**](itformatcontrol-getstreamcaps.md)                     | Ruft die einem angegebenen Formatindex zugeordneten Funktionen ab.<br/>         |
| [**ReleaseFormat**](itformatcontrol-releaseformat.md)                     | Gibt die dem Format zugeordnete Struktur frei.<br/>                  |
| [**ReOrderCapabilities**](itformatcontrol-reordercapabilities.md)         | Legt eine neue Reihenfolge für Formatfunktionen fest.<br/>                           |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.1<br/>                                                         |
| Header<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



 

