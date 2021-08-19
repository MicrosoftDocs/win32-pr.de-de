---
title: Konfigurieren von Streams
description: Konfigurieren von Streams
ms.assetid: f8f1656e-69c6-47f7-a8eb-c1039a84ebf3
keywords:
- Streams,Konfigurieren von Skriptstreams
- Codecs,Konfigurieren von Skriptstreams
- Skriptstreams,Konfigurieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f95c4c43fcb29ec2f77dacbf5a66b1c8c36c666d80fd5f5c09779a4ecaf22f05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117655988"
---
# <a name="configuring-script-streams"></a>Konfigurieren von Streams

Wie bei allen beliebigen Streamtypen müssen für Skriptstreams eine Bitrate und ein Pufferfenster definiert sein. Der Hauptmedientyp in der [**WM \_ MEDIA \_ TYPE-Struktur**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) muss auf WMMEDIATYPE Script festgelegt \_ werden.

Für Skriptstreams muss der **formattype-Member** von **WM MEDIA \_ \_ TYPE** auf WMFORMAT Script festgelegt sein. Dies bedeutet, dass der pbFormat-Member auf eine \_ [**WMSCRIPTFORMAT-Struktur**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmscriptformat) verweist. 

Es gibt nur einen unterstützten Skripttyp, WMSCRIPTTYPE \_ TwoStrings.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Configuration Common to All Streams**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Konfigurieren beliebiger Streamtypen**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Skriptbefehle**](script-commands.md)
</dt> </dl>

 

 




