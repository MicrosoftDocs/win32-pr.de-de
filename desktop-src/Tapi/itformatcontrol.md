---
description: Die itformatcontrol-Schnittstelle macht Methoden verfügbar, mit denen eine Anwendung Informationen über das Format eines Empfangs-oder Übertragungsdaten Stroms für einen-Abruf abrufen kann.
ms.assetid: a3d15561-229e-4eb6-a0ac-2d69f170bced
title: Itformatcontrol-Schnittstelle (ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0735e7bfaf5222948cef5e047530a35cb19a125
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365764"
---
# <a name="itformatcontrol-interface"></a>Itformatcontrol-Schnittstelle

\[ Diese Schnittstelle ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **itformatcontrol** -Schnittstelle macht Methoden verfügbar, mit denen eine Anwendung Informationen über das Format eines Empfangs-oder Übertragungsdaten Stroms für einen-Abruf abrufen kann.

Diese Schnittstelle wird vom [h323-MSP](h323-msp.md) implementiert und wird nur verfügbar gemacht, wenn ein-Rückruf diesen Dienstanbieter verwendet.

## <a name="members"></a>Member

Die **itformatcontrol** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Itformatcontrol** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **itformatcontrol** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                     | BESCHREIBUNG                                                                    |
|:---------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**Getcurrentformat**](itformatcontrol-getcurrentformat.md)               | Ruft das Medienformat des aktuellen Streams ab.<br/>                        |
| [**Getnumof-Funktionen**](itformatcontrol-getnumberofcapabilities.md) | Ruft die Anzahl der Funktionen ab, die dem aktuellen Format zugeordnet sind.<br/> |
| [**Getstreamcaps**](itformatcontrol-getstreamcaps.md)                     | Ruft die Funktionen ab, die einem angegebenen Format Index zugeordnet sind.<br/>         |
| [**Releaseformat**](itformatcontrol-releaseformat.md)                     | Gibt die Struktur frei, die dem Format zugeordnet ist.<br/>                  |
| [**Reorderfunktionen**](itformatcontrol-reordercapabilities.md)         | Legt eine neue Reihenfolge für Formatierungsfunktionen fest.<br/>                           |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,1<br/>                                                         |
| Header<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



 

