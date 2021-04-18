---
title: Wieder verwenden von streamkonfigurationen
description: Wieder verwenden von streamkonfigurationen
ms.assetid: e2263c3a-56cd-4505-acd7-510dc7bac166
keywords:
- Streams, wieder verwenden von Konfigurationen
- Profile, wieder verwenden von streamkonfigurationen
- wieder verwenden von streamkonfigurationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9af10fd026904ccef33aba28d28e0e6a4975d3fd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106338240"
---
# <a name="reusing-stream-configurations"></a>Wieder verwenden von streamkonfigurationen

Es gibt häufig vorkommen, dass Sie ein Datenstrom-Konfigurationsobjekt aus einem vorhandenen Profil wieder verwenden möchten. Möglicherweise verfügen Sie über alte Profile, die aktualisiert werden müssen, oder Sie benötigen einen Datenstrom, der mit einem in einem Systemprofil identisch ist. Es ist einfacher, streamkonfigurationen wiederzuverwenden, als neue zu erstellen, und Sie können häufig einige Einstellungen in einer Konfiguration ändern, um Ihre Anforderungen zu erfüllen, anstatt eine völlig neue zu erstellen.

Beachten Sie, dass es Einschränkungen gibt, wie Sie Datenstrom Konfigurationen ändern können. Wenn Sie Einstellungen auf falsche Weise ändern, akzeptiert das Profil das Datenstrom-Konfigurationsobjekt möglicherweise nicht. Falsche streamkonfigurationen werden häufig vom Profil akzeptiert, bewirken jedoch, dass das Writer-Objekt das Profil ablehnt. Beachten Sie die folgenden Einschränkungen und Probleme beim verwenden und Ändern vorhandener streamkonfigurationen.

-   Ändern Sie den Inhalt einer PRX-Datei nie, um die streameinstellungen zu ändern. Wenn Profile in XML-Zeichen folgen gespeichert und in eine PRX-Datei geschrieben werden, können Sie mit einem beliebigen Text-Editor gelesen werden. Wenn Sie ein gespeichertes Profil betrachten, können Sie besser verstehen, wie Profile funktionieren. Sie sollten jedoch nie eine PRX-Datei ändern. Sogar scheinbar triviale Änderungen können das Profil für ungültig erklären.
-   Mehrere Versionen des Windows Media Audio Codecs verwenden die gleichen streamkonfigurationen. Wenn Sie über ein Datenstrom-Konfigurationsobjekt verfügen, das als Untertyp wmmediasubtype \_ WMAudioV2, wmmediasubtype \_ WMAudioV7 oder wmmediasubtype WMAudioV8 konfiguriert ist \_ , wird der resultierende Stream mit dem neuesten Windows Media Audio Codec komprimiert. Sie sollten jedoch Ihre Anforderungen auswerten, bevor Sie einen vorhandenen Audiocodec verwenden. Viele Arten von Dateien können durch ein Upgrade auf die neueste Version des Windows Media Audio Professional-Codecs oder den Windows Media Audio verlustfreien Codec verbessert werden.
-   Ändern Sie niemals den Untertyp eines Datenstroms, um ein Upgrade auf einen neuen Codec durchzuführen. Wenn Sie die-Methoden von [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) verwenden, um eine streamkonfiguration abzurufen, fügt der Codec einige Daten an den Codec an, der das bitstreamformat identifiziert. Wenn Sie den Untertyp eines vorhandenen Datenstrom-Konfigurations Objekts ändern, entspricht der Untertyp nicht den Codec-Daten. Ein Profil mit einer solchen Datenstrom Konfiguration wird vom Writer-Objekt nicht akzeptiert.
-   Ändern Sie nicht die Einstellungen von komprimierten audiostreamkonfigurationen. Wenn die Einstellungen eines Audiodatenstroms Ihren Anforderungen nicht entsprechen, können Sie mithilfe der Methoden von **IWMCodecInfo3** eine neue streamkonfiguration aus dem Codec abrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Konfigurieren von Streams**](configuring-streams.md)
</dt> <dt>

[**Informationen zu streamkonfigurations Informationen von Codecs**](getting-stream-configuration-information-from-codecs.md)
</dt> </dl>

 

 




