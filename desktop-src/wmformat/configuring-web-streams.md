---
title: Konfigurieren von Streams
description: Konfigurieren von Streams
ms.assetid: 1eeb6243-5095-4dba-994c-2083beda7b78
keywords:
- Streams,Konfigurieren von Webstreams
- Codecs,Konfigurieren von Webstreams
- Webstreams,Konfigurieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8df1ced96a772a26b674fb47a30a8664d6431ff946328f45467554857b1ee4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118199121"
---
# <a name="configuring-web-streams"></a>Konfigurieren von Streams

Webstreams sind ein spezieller Typ von Dateiübertragungsstream, der verwendet wird, um die dateien zu übertragen, die einer Website in einem einzelnen Stream zugeordnet sind. Die Webstreamkonfiguration wird in der folgenden Tabelle zusammengefasst.



| Einstellung                                            | BESCHREIBUNG                                                                       |
|----------------------------------------------------|-----------------------------------------------------------------------------------|
| **WM \_ MEDIA \_ TYPE.majortype**                      | Legen Sie auf WMMEDIATYPE \_ FileTransfer fest.                                                 |
| **WM \_ MEDIA \_ TYPE.subtype**                        | Legen Sie auf WMMEDIASUBTYPE \_ WebStream fest.                                                 |
| **WM \_ MEDIA \_ TYPE.bFixedSizeSamples**              | Legen Sie auf False fest.                                                                     |
| **WM \_ MEDIA \_ TYPE.bTemporalCompression**           | Legen Sie auf True fest.                                                                      |
| **WM \_ MEDIA \_ TYPE.lSampleSize**                    | Auf 0 festlegen.                                                                         |
| **WM \_ MEDIA \_ TYPE.formattype**                     | Legen Sie auf WMFORMAT \_ WebStream fest.                                                       |
| **WM \_ MEDIA \_ TYPE.pUnk**                           | Legen Sie auf **NULL fest.**                                                                  |
| **WM \_ MEDIA \_ TYPE.cbFormat**                       | Legen Sie diese Option auf `sizeof(WMT_WEBSTREAM_FORMAT)` fest.                                            |
| **WM \_ MEDIA \_ TYPE.pbFormat**                       | Legen Sie auf die Adresse einer ordnungsgemäß konfigurierten **WMT \_ WEBSTREAM \_ FORMAT-Struktur** fest. |
| **WMT \_ WEBSTREAM \_ FORMAT.cbSampleHeaderFixedData** | Legen Sie diese Option auf `sizeof(WMT_WEBSTREAM_SAMPLE_HEADER)` fest.                                     |
| **WMT \_ WEBSTREAM \_ FORMAT.wVersion**                | Auf 1 festlegen.                                                                         |
| **WMT \_ WEBSTREAM \_ FORMAT.wreserved**               | Auf 0 festlegen.                                                                         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Configuration Common to All Streams**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Konfigurieren beliebiger Streamtypen**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Web Streams**](web-streams.md)
</dt> </dl>

 

 




