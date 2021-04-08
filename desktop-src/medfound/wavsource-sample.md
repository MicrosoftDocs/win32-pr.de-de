---
description: Wavsource-Beispiel
ms.assetid: 905fbba5-0a04-4048-80bd-f8707c4879da
title: Wavsource-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 050edb9df75032384f93c6e1f37c52e89f14a748
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863923"
---
# <a name="wavsource-sample"></a>Wavsource-Beispiel

Zeigt, wie eine benutzerdefinierte Medienquelle in Microsoft Media Foundation erstellt wird. Im Beispiel wird eine Medienquelle implementiert, mit der WAV-Audiodateien analysiert werden.

Dieses Beispiel ist ein relativ einfaches Beispiel für eine Medienquelle:

-   Es ist nur ein Stream vorhanden, sodass kein Code zum Implementieren der Streamauswahl vorhanden ist.
-   Die Medienquelle implementiert nicht die Raten Kontrolle (d. h. die schnelle vorwärts-oder rückwärts Wiedergabe).
-   Alle Quell-und Datenstrom Methoden werden als synchrone Methoden implementiert.
-   Da es sich bei dem Datenteil einer WAV-Datei um einen einzelnen Block nicht komprimierter PCM-Audiodaten handelt, muss die Medienquelle keine Paket Header lesen oder den Stream bei der Wiedergabe anderweitig analysieren, außer wenn der anfängliche [**wellenformat**](/windows/win32/api/mmreg/ns-mmreg-waveformat) -Header gelesen wird.

Ein erweitertes Beispiel für eine Medienquelle finden Sie im [MPEG1Source](mpeg1source-sample.md)-Beispiel.

## <a name="apis-demonstrated"></a>Gezeigte APIs

In diesem Beispiel werden die folgenden Media Foundation Schnittstellen veranschaulicht:

-   [**IMF bytestreamhandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)
-   [**Imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
-   [**IMF Media Stream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)

## <a name="usage"></a>Verbrauch

Das wavsource-Beispiel erstellt eine DLL, bei der es sich um einen com-Server für den bytestreamhandler der Medienquelle und der Medienquelle handelt. Vor der Verwendung der Medienquelle müssen Sie die dll registrieren.

Wenn Sie die Medienquelle verwenden möchten, können Sie die [basicplayback](/previous-versions//bb970475(v=vs.85))ausführen. Der quellresolver lädt automatisch die Medienquelle, wenn Sie eine WAV-Datei für die Wiedergabe auswählen. (Wenn ein Fehler auftritt, stellen Sie sicher, dass Sie die wavsource-dll erfolgreich registriert haben.)

Sie können auch das Tool topoedit verwenden, um eine Wiedergabe Topologie zu erstellen, die die Medienquelle enthält. Weitere Informationen zu topoedit finden Sie unter [topoedit](topoedit.md).

## <a name="requirements"></a>Anforderungen



| Produkt                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist im [GitHub-Repository für klassische Windows-Beispiele](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsource)verfügbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation-SDK-Beispiele](media-foundation-sdk-samples.md)
</dt> <dt>

[Medienquellen](media-sources.md)
</dt> <dt>

[MPEG1Source-Beispiel](mpeg1source-sample.md)
</dt> <dt>

[Schema Handler und Byte-Stream Handler](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[Schreiben einer benutzerdefinierten Medienquelle](writing-a-custom-media-source.md)
</dt> </dl>

 

 
