---
title: Ermitteln der Funktionen des Geräte Formats
description: Ermitteln der Funktionen des Geräte Formats
ms.assetid: dd139816-dc8c-4e73-9a21-67287bfe6405
keywords:
- Windows Media Device Manager, Gerätefunktionen
- Device Manager, Gerätefunktionen
- Programmier Handbuch, Gerätefunktionen
- Desktop Anwendungen, Gerätefunktionen
- Erstellen von Windows Media Device Manager-Anwendungen, Gerätefunktionen
- Schreiben von Dateien auf Geräte, Gerätefunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0ee05476f6b84bc85bb81cc7cff5815649f5842
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337150"
---
# <a name="discovering-device-format-capabilities"></a>Ermitteln der Funktionen des Geräte Formats

Die Anwendung versucht möglicherweise, die Wiedergabe Funktionen eines Geräts zu bestimmen, bevor eine Datei an Sie gesendet wird. Wenn ein Gerät das Format einer Datei, die Sie senden möchten, nicht verarbeiten kann, kann die Anwendung versuchen, die Datei in ein Format zu transcodieren, das vom Gerät verwendet werden kann, oder den Benutzer darüber benachrichtigen, dass die angeforderte Datei vom Gerät nicht unterstützt wird.

Beachten Sie, dass einige Geräte, z. b. Massenspeicher Klassen-Geräte, möglicherweise nur als Wechselmedien ohne Wiedergabe Funktionen dienen. In diesem Fall wäre es für Ihre Anwendung ungeeignet, eine Datei zu transcodieren, bevor Sie an das Gerät gesendet wird.

Obwohl die [**iwmdmdevice:: GetType**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-gettype) -Methode es einem Gerät ermöglicht, seine Funktionen zu melden, geben einige Geräte falsche Werte für diese Methode zurück. Bevor Sie eine Datei auf ein Gerät kopieren, können Sie den Benutzer Fragen, ob die Wiedergabe beabsichtigt ist. wenn dies der Fall ist, versuchen Sie, die Datei in eines der gemeldeten Formate des Geräts zu transcodieren (oder ein vernünftiges Format, wenn das Gerät die Unterstützung für ein beliebiges Format beansprucht). Ein anderer Ansatz besteht darin, zu übernehmen, dass alle Formate, die vom Gerät unterstützt werden, für die Wiedergabe gedacht sind und alle anderen Dateien unverändert übertragen werden sollten.

Nachdem Sie das Format der zu übertragenden Datei und die von einem Gerät unterstützten Formate ermittelt haben, können Sie entscheiden, welches das beste Zielformat für die Transcodierung ist.

In der Vergangenheit war es üblich, dass eine Anwendung für eine Eigenschaft NULL zurückgibt, um die Unterstützung für alle Werte dieser Eigenschaft anzugeben. Beispielsweise würde ein Wert von 0 (null) für [**\_ WaveFormatEx**](-waveformatex.md). nsamplespersec die Unterstützung für jede Bitrate angeben. Die empfohlene Vorgehensweise, um die Unterstützung für beliebige Werte anzugeben, besteht darin, die WMDM-Enumerationswerte für \_ \_ \_ gültige \_ Werte \_ in [**WMDM- \_ Prop- \_ DESC**](wmdm-prop-desc.md)anzugeben. Validvaluesform. Einige Eigenschaften können jedoch recht NULL zurückgeben, um bestimmte Unterstützung anzugeben. Wenn [**\_ BITMAPINFOHEADER**](-bitmapinfoheader.md). bisizeimage beispielsweise auf 0 (null) festgelegt ist, deutet dies auf eine BI- \_ RGB-Bitmap hin. Ausnahmen für Nullwerte werden in der Dokumentation für die relevanten Strukturen angegeben.

Es ist jedoch wichtig zu beachten, dass Geräte ihre Formatfunktionen häufig nicht ordnungsgemäß oder standardmäßig melden. Beispielsweise melden Geräte häufig, dass Sie ein beliebiges Format unterstützen, wenn Sie tatsächlich nur bestimmte Formate oder bestimmte Bitraten innerhalb eines Formattyps verarbeiten können. Sie müssen entscheiden, ob Ihre Anwendung solche Berichte akzeptieren soll oder ob Sie eine Obergrenze für die Wiedergabe Fähigkeiten eines Geräts annehmen soll (z. b. 192 Kbit/s).

Die empfohlene Methode zum Anfordern der Formatunterstützung eines Geräts ist [**IWMDMDevice3:: getformatcapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability). Wenn diese Methode nicht unterstützt wird, sollte die Anwendung auf [**iwmdmdevice:: getformatsupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport)zurückgreifen. **Getformatsupport** gibt im Gegensatz zu **GetFormatSupport2** keine Videoinformationen zurück.

Wie eine Anwendung die Formatierungsfunktionen eines Geräts anfordert, hängt davon ab, welche Schnittstelle die Anwendung unterstützt. Weitere Einzelheiten dazu finden Sie in folgenden Themen:

-   [Erhalten von Format Funktionen auf Geräten, die IWMDMDevice3 unterstützen](getting-format-capabilities-on-devices-that-support-iwmdmdevice3.md)
-   [Erhalten von Format Funktionen auf Geräten, die nur iwmdmdevice unterstützen](getting-format-capabilities-on-devices-that-support-only-iwmdmdevice.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Schreiben von Dateien auf das Gerät**](writing-files-to-the-device.md)
</dt> </dl>

 

 




