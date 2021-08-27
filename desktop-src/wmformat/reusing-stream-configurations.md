---
title: Wiederverwendung von Streamkonfigurationen
description: Wiederverwendung von Streamkonfigurationen
ms.assetid: e2263c3a-56cd-4505-acd7-510dc7bac166
keywords:
- Streams, Wiederverwendung von Konfigurationen
- Profile,Wiederverwendung von Streamkonfigurationen
- Wiederverwendung von Streamkonfigurationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25ee1a2b51d5a2a659cb24955ab74a5fb285308125b21781c9d42a709d7e4b64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110190"
---
# <a name="reusing-stream-configurations"></a>Wiederverwendung von Streamkonfigurationen

Häufig möchten Sie ein Streamkonfigurationsobjekt aus einem vorhandenen Profil wiederverwenden. Möglicherweise verfügen Sie über alte Profile, die aktualisiert werden müssen, oder Sie benötigen einen Stream, der mit dem in einem Systemprofil identisch ist. Es ist einfacher, Streamkonfigurationen wiederzuverwenden, als neue zu erstellen, und Sie können häufig einige Einstellungen in einer Konfiguration ändern, um Ihre Anforderungen zu erfüllen, anstatt eine völlig neue zu erstellen.

Beachten Sie, dass es Einschränkungen beim Ändern von Streamkonfigurationen gibt. Wenn Sie die Einstellungen falsch ändern, akzeptiert Ihr Profil möglicherweise das Streamkonfigurationsobjekt nicht. Falsche Streamkonfigurationen werden häufig vom Profil akzeptiert, führen jedoch dazu, dass das Writer-Objekt das Profil zurückweisen kann. Beachten Sie die folgenden Einschränkungen und Probleme beim Verwenden und Ändern vorhandener Streamkonfigurationen.

-   Ändern Sie niemals den Inhalt einer PRX-Datei, um die Streameinstellungen zu ändern. Wenn Profile in XML-Zeichenfolgen gespeichert und in eine PRX-Datei geschrieben werden, können sie mit einem beliebigen Text-Editor gelesen werden. Das Anzeigen eines gespeicherten Profils kann Ihnen helfen, die Funktionsweise von Profilen zu verstehen. Sie sollten jedoch niemals eine PRX-Datei ändern. Selbst scheinbar triviale Änderungen können das Profil für ungültig erklären.
-   Mehrere Versionen des Windows Medienaudiocodecs verwenden die gleichen Streamkonfigurationen. Wenn Sie über ein Streamkonfigurationsobjekt verfügen, das als Untertyp WMMEDIASUBTYPE \_ WMAudioV2, WMMEDIASUBTYPE \_ WMAudioV7 oder WMMEDIASUBTYPE WMAudioV8 konfiguriert ist, wird der resultierende Stream mit dem neuesten \_ Windows Media Audio-Codec komprimiert. Allerdings sollten Sie Ihre Anforderungen auswerten, bevor Sie einen vorhandenen Audiocodec verwenden. Viele Dateitypen können durch ein Upgrade auf die neueste Version des Windows Media Audio Professional-Codecs oder des Windows Media Audio Lossless-Codecs verbessert werden.
-   Ändern Sie niemals den Untertyp eines Streams, um ein Upgrade auf einen neuen Codec zu durchführen. Wenn Sie die Methoden von [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) verwenden, um eine Streamkonfiguration zu erhalten, werden vom Codec einige Daten angefügt, die das Bitstreamformat identifizieren. Wenn Sie den Untertyp eines vorhandenen Streamkonfigurationsobjekts ändern, wird der Untertyp nicht mit den Codecdaten übereinstimmen. Ein Profil mit einer solchen Streamkonfiguration wird vom Writerobjekt nicht akzeptiert.
-   Ändern Sie die Einstellungen komprimierter Audiostreamkonfigurationen nicht. Wenn die Einstellungen eines Audiostreams nicht Ihren Anforderungen entsprechen, erhalten Sie eine neue Streamkonfiguration aus dem Codec mithilfe der **Methoden von IWMCodecInfo3.**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Konfigurieren Streams**](configuring-streams.md)
</dt> <dt>

[**Abrufen von Streamkonfigurationsinformationen aus Codecs**](getting-stream-configuration-information-from-codecs.md)
</dt> </dl>

 

 




