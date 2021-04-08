---
title: Protokollrollover
description: Protokollrollover
ms.assetid: 61db5e2b-4858-446e-9a27-e0305b46683d
keywords:
- Windows Media-Format-SDK, Protokollrollover
- Advanced Systems Format (ASF), Protokollrollover
- ASF (Advanced Systems Format), Protokollrollover
- Protokollrollover
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2de8d0496467535f5740a10082f82e285c11ef6
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038560"
---
# <a name="protocol-rollover"></a>Protokollrollover

Der Protokollrollover ist ein Prozess, bei dem das Reader-Objekt das beste Streamingprotokoll erkennt, das auf einem Server verfügbar ist Der Reader verwendet beim Öffnen einer URL, die ein "MMS"-Schema enthält, den Protokollrollover.

Der Reader unterstützt mehrere Protokolle:

-   Real-Time Streaming Protocol (RTSP)
-   Hypertext Transfer-Protokoll (HTTP)
-   Microsoft Media Server (MMS)

Die Protokolle "RTSP" und "MMS" sind in zwei Varianten enthalten: eine, die [*UDP*](wmformat-glossary.md) als zugrunde liegendes Übermittlungs Protokoll verwendet, und die andere mit TCP.

Das Reader-Objekt verwendet immer TCP für Wiedergabe Steuerungsbefehle, aber es kann entweder TCP oder UDP für die Übermittlung des gestreuten Inhalts verwenden. UDP wird für die Inhalts Übermittlung bevorzugt, da dadurch weniger Bandbreiten Aufwand als bei TCP erzwungen wird. Das TCP-Protokoll gewährleistet einen zuverlässigen Transport durch die Verwendung von "virtuellen Leitungen", aber die Kosten hierfür bedeuten, dass TCP nicht so gut für digitale Medienströme geeignet ist, wenn die effiziente Nutzung der Bandbreite wichtiger ist, dass gelegentlich verlorene Pakete verloren gehen.

Wenn eine URL "MMS://" angibt, versucht der Reader, die folgenden Protokolle für die Datenübermittlung in der folgenden Reihenfolge zu verwenden:

1.  RTSPU (RTSP mithilfe von UDP)
2.  RTSPT (RTSP mit TCP)
3.  MMSU (MMS mithilfe von UDP)
4.  Mmst (MMS mit TCP)
5.  HTTP

HTTP ist ein unidirektionales Protokoll, das auf TCP basiert, und ist das Protokoll, das von Webservern verwendet wird. Streaming mit http ist mit RTSP weniger effizient. Die meisten Firewalls sind jedoch so konfiguriert, dass HTTP-Anforderungen akzeptiert werden, während Sie in der Regel andere Streamingprotokolle ablehnen.

Die Windows Media Services 9-Reihe in Microsoft Windows Server 2003 lehnt alle MMSU-oder mmst-Anforderungen von einem SDK-Reader des Windows Media-Formats ab, da RTSP das bevorzugte Streamingprotokoll ist. RTSP wird von Windows Media Services Version 4,1 und früher nicht unterstützt. In diesem Fall greift das Reader-Objekt auf "MMSU" oder "http" zurück.

Der Protokollrollover trifft nicht zu, wenn das URL-Schema ein bestimmtes Protokoll (z. b. "rtspu://" für RTSPU oder "https://" für http) enthält. Wenn das URL-Schema "RTSP://" ist, versucht der Reader RTSPU und RTSPT, aber keine anderen.

Nachdem der Reader eine Datei geöffnet hat, können Sie Abfragen, welches Protokoll verwendet wird, indem Sie die [**IWMReaderAdvanced2:: getprotocolname**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname) -Methode für den Reader aufrufen. Während der Inhalt gestreamt oder heruntergeladen wird, gibt diese Methode den Namen zurück, sobald der Inhalt vollständig zwischengespeichert ist. die **getprotocolname** -Methode gibt die Zeichenfolge "Cache" zurück.

Um die Namen aller Windows Media Server-Protokolle abzurufen, die der Reader unterstützt, müssen Sie die [**iwmreadernetworkconfig:: getsupportedprotocolname**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-getsupportedprotocolname) -Methode für den Reader aufrufen. Sie können ein oder mehrere der Protokolle in der protokollrolloverliste des Readers mithilfe der **iwmreadernetworkconfig** -Schnittstelle deaktivieren. Die [**iwmreadernetworkconfig:: abtenabletcp**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setenabletcp) -Methode aktiviert oder deaktiviert z. b. die TCP-basierten Protokolle, und [**iwmreadernetworkconfig:: ableudp**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setenableudp) aktiviert oder deaktiviert die UDP-basierten Protokolle. Diese Methoden gelten nur für Protokollrollover. die Protokolle sind weiterhin verfügbar, wenn das URL-Schema ein bestimmtes Protokoll enthält. Es gibt in der Regel keinen Grund, die Protokolle zu deaktivieren, die im Protokollrollover verwendet werden. Dadurch kann die Leistung beeinträchtigt werden. Dies kann jedoch für Tests hilfreich sein.

 

 




