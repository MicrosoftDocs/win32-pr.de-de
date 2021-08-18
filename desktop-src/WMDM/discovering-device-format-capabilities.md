---
title: Entdecken von Geräteformatfunktionen
description: Entdecken von Geräteformatfunktionen
ms.assetid: dd139816-dc8c-4e73-9a21-67287bfe6405
keywords:
- Windows Medien Geräte-Manager,Gerätefunktionen
- Geräte-Manager,Gerätefunktionen
- Programmierhandbuch, Gerätefunktionen
- Desktopanwendungen,Gerätefunktionen
- Erstellen Windows Media Geräte-Manager Anwendungen,Gerätefunktionen
- Schreiben von Dateien auf Geräte,Gerätefunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03e4fc32c0980a1022f7affb225918ccf0d49e5d14c5bb7310e70e7aa4f83a62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585146"
---
# <a name="discovering-device-format-capabilities"></a>Entdecken von Geräteformatfunktionen

Ihre Anwendung versucht möglicherweise, die Wiedergabefunktionen eines Geräts zu ermitteln, bevor eine Datei an das Gerät sendet. Wenn ein Gerät das Format einer Datei, die Sie senden möchten, nicht verarbeiten kann, versucht Ihre Anwendung möglicherweise, die Datei in ein Format zu transcodieren, das das Gerät verwenden kann, oder den Benutzer zu benachrichtigen, dass das Gerät die angeforderte Datei nicht unterstützen kann.

Beachten Sie, dass einige Geräte, z. B. Massenspeicherklassengeräte, möglicherweise nur als Wechselmedien ohne Wiedergabefunktionen dienen. In diesem Fall wäre es für Ihre Anwendung ungeeignet, eine Datei vor dem Senden an das Gerät zu transcodieren.

Obwohl die [**IWMDMDevice::GetType-Methode**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-gettype) es einem Gerät ermöglicht, seine Funktionen zu melden, geben einige Geräte falsche Werte für diese Methode zurück. Bevor Sie eine Datei auf ein Gerät kopieren, sollten Sie den Benutzer fragen, ob die Wiedergabe beabsichtigt ist, und in diesem Fall versuchen, die Datei in eines der gemeldeten Formate des Geräts zu transcodieren (oder ein angemessenes Format, wenn das Gerät Unterstützung für ein beliebiges Format beansprucht). Ein anderer Ansatz besteht in der Annahme, dass alle Formate, die speziell als vom Gerät unterstützt aufgeführt sind, für die Wiedergabe vorgesehen sind und alle anderen Dateien unverändert übertragen werden sollten.

Nachdem Sie das Format der zu übertragenden Datei und die von einem Gerät unterstützten Formate gefunden haben, können Sie entscheiden, welches Zielformat für die Transcodierung am besten ist.

In der Vergangenheit war es üblich, dass eine Anwendung 0 (null) für eine Eigenschaft zurück gab, um die Unterstützung für alle Werte dieser Eigenschaft anzugeben. Ein Wert von 0 (null) für [**\_ WAVEFORMATEX**](-waveformatex.md).nSamplesPerSec würde beispielsweise die Unterstützung für jede Bitrate angeben. Nun wird empfohlen, die Unterstützung für jeden Wert anzugeben, indem Sie WMDM \_ ENUM \_ PROP VALID VALUES ANY in \_ \_ \_ [**WMDM \_ PROP \_ DESC angeben.**](wmdm-prop-desc.md) ValidValuesForm. Einige Eigenschaften können jedoch 0 (null) zurückgeben, um eine bestimmte Unterstützung anzugeben. Wenn z. B. [**\_ BITMAPINFOHEADER**](-bitmapinfoheader.md).biSizeImage auf 0 (null) festgelegt ist, gibt dies eine BI \_ RGB-Bitmap an. Ausnahmen für Nullwerte sind in der Dokumentation für die relevanten Strukturen angegeben.

Es ist jedoch wichtig zu beachten, dass Geräte ihre Formatfunktionen häufig nicht ordnungsgemäß oder standardmäßig melden. Beispielsweise melden Geräte häufig, dass sie jedes Format unterstützen, wenn sie tatsächlich nur bestimmte Formate oder bestimmte Bitraten innerhalb eines Formattyps verarbeiten können. Sie müssen entscheiden, ob Ihre Anwendung solche Berichte akzeptieren soll oder ob eine Obergrenze für die Wiedergabefähigkeit eines Geräts angenommen werden soll (z. B. 192 KBit/s).

Die empfohlene Methode zum Anfordern der Formatunterstützung eines Geräts ist [**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability). Wenn diese Methode nicht unterstützt wird, sollte Ihre Anwendung auf [**IWMDMDevice::GetFormatSupport zurückfallen.**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) Im Gegensatz zu **GetFormatSupport2 gibt** **GetFormatSupport** keine Videoinformationen zurück.

Wie eine Anwendung die Formatfunktionen eines Geräts an fordert, hängt davon ab, welche Schnittstelle die Anwendung unterstützt. Weitere Einzelheiten dazu finden Sie in folgenden Themen:

-   [Abrufen von Formatfunktionen auf Geräten, die IWMDMDevice3 unterstützen](getting-format-capabilities-on-devices-that-support-iwmdmdevice3.md)
-   [Abrufen von Formatfunktionen auf Geräten, die nur IWMDMDevice unterstützen](getting-format-capabilities-on-devices-that-support-only-iwmdmdevice.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Schreiben von Dateien auf das Gerät**](writing-files-to-the-device.md)
</dt> </dl>

 

 




