---
title: Konfigurieren von Webstreams
description: Konfigurieren von Webstreams
ms.assetid: 1eeb6243-5095-4dba-994c-2083beda7b78
keywords:
- Streams, Konfigurieren von Webstreams
- Codecs, Konfigurieren von Webstreams
- Webstreams, konfigurieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27c91c36788b858b2378ebf46b553f076c5ec490
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311012"
---
# <a name="configuring-web-streams"></a>Konfigurieren von Webstreams

Webstreams sind ein spezieller Typ von Datei Übertragungsdaten Strom, der verwendet wird, um die einer Website zugeordneten Dateien in einem einzigen Stream bereitzustellen. Die Webstream-Konfiguration ist in der folgenden Tabelle zusammengefasst.



| Einstellung                                            | BESCHREIBUNG                                                                       |
|----------------------------------------------------|-----------------------------------------------------------------------------------|
| **WM \_ - \_ Medientyp. majortype**                      | Legen Sie auf wmmediatype \_ Filetransfer fest.                                                 |
| **WM \_ - \_ Medientyp. Untertyp**                        | Legen Sie auf wmmediasubtype \_ Webstream fest.                                                 |
| **WM \_ - \_ Medientyp. bfixedsizesamples**              | Legen Sie auf false fest.                                                                     |
| **WM \_ - \_ Medientyp. btemporalcompression**           | Legen Sie den Wert auf True fest.                                                                      |
| **WM \_ - \_ Medientyp. lsamplesize**                    | Auf 0 festlegen.                                                                         |
| **WM \_ - \_ Medientyp. formatType**                     | Legen Sie auf wmformat \_ Webstream fest.                                                       |
| **WM \_ - \_ Medientyp. Punk**                           | Auf **null** festgelegt.                                                                  |
| **WM \_ - \_ Medientyp. cbformat**                       | Legen Sie diese Option auf `sizeof(WMT_WEBSTREAM_FORMAT)` fest.                                            |
| **WM \_ - \_ Medientyp. pbformat**                       | Legen Sie die Adresse einer ordnungsgemäß konfigurierten **WMT- \_ Webstream- \_ Format** Struktur fest. |
| **WMT- \_ Webstream- \_ Format. cbsampleheaderfixeddata** | Legen Sie diese Option auf `sizeof(WMT_WEBSTREAM_SAMPLE_HEADER)` fest.                                     |
| **WMT- \_ Webstream- \_ Format. wversion**                | Auf 1 festlegen.                                                                         |
| **WMT- \_ Webstream- \_ Format. wReserved**               | Auf 0 festlegen.                                                                         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Allgemeine Konfiguration für alle Streams**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Konfigurieren beliebiger Streamtypen**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Webstreams**](web-streams.md)
</dt> </dl>

 

 




