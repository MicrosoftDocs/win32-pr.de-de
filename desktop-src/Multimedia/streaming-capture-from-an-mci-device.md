---
title: Streaming-Erfassung von einem MCI-Gerät
description: Streaming-Erfassung von einem MCI-Gerät
ms.assetid: 44cbf375-f97e-426a-a703-dfb1b1933138
keywords:
- MCI (Medien Steuerungs Schnittstelle), streamingerfassung
- WM_CAP_SET_MCI_DEVICE Meldung
- capabtmcidevicename-Makro
- WM_CAP_GET_MCI_DEVICE Meldung
- capgetmcidevicename-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab8cf358a87a812024328abf7fc1aae0509a126f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515975"
---
# <a name="streaming-capture-from-an-mci-device"></a>Streaming-Erfassung von einem MCI-Gerät

MCI-Geräte vergrößern den Aufzeichnungs Vorgang in Echtzeit-Erfassung und Schritt-für-Schritt-Erfassung. Sie können das MCI-Gerät angeben, z. b. eine Videodisk oder Video-Kassettenrecorder (VCR), das als Videoquelle für Ihren Aufzeichnungs Vorgang dient, indem Sie die Richtlinien- [**\_ \_ \_ MCI- \_ Geräte**](wm-cap-set-mci-device.md) Nachricht (oder das " [**capsetmcidevicename**](/windows/desktop/api/Vfw/nf-vfw-capsetmcidevicename) "-Makro der WM-Obergrenze) verwenden und den Namen des Geräts angeben. Sie können den derzeit festgelegten Gerätenamen auch abrufen, indem Sie die [**\_ gatewaycap- \_ \_ MCI- \_ Geräte**](wm-cap-get-mci-device.md) Nachricht (oder das " [**capgetmcidevicename**](/windows/desktop/api/Vfw/nf-vfw-capgetmcidevicename) "-Makro) verwenden.

Bei der echt Zeiterfassung synchronisiert das Aufzeichnungs Fenster den Aufzeichnungs Vorgang und kompensiert Verzögerungen bei der Positionierung der MCI-Videoquelle und beim Initialisieren der Ressourcen (z. b. Erfassungs Puffer), die zum Erfassen von Daten erforderlich sind. Das Erfassungsfenster erwartet, dass ein gültiges MCI-Videogerät zum Erfassen von Daten auf diese Weise im System installiert wird.

Spezifikationen zum Steuern eines MCI-Geräts werden in den Membern der [**captumappms**](/windows/win32/api/vfw/ns-vfw-captureparms) -Struktur gespeichert. MCI-kompatible Videoquellen enthalten VCRs und Laser Disks. Wenn der **fmcicontrol** -Member dieser Struktur auf **true** festgelegt ist, koordiniert das Aufzeichnungs Fenster den MCI-Vorgang. Das Erfassungsfenster verwendet die Parameter, die in den Elementen **dwmcistarttime** und **dwmcistoptime** angegeben sind, um die Anfangs-und Stopp Positionen der Sequenz zu erhalten. Wenn der Wert von **fmcicontrol** **false** ist, wird die Videoquelle nicht als MCI-Gerät behandelt, und der Inhalt von **dwmcistarttime** und **dwmcistoptime** werden ignoriert.

Mit Media Player können Sie schnell überprüfen, ob ein MCI-Videogerät ordnungsgemäß mit dem System verbunden ist. Wenn Sie ein Gerät mit Media Player wiedergeben, wird überprüft, ob die MCI-Konfiguration für das Gerät richtig ist. Wenn ein Bild auf der Videoanzeige angezeigt wird, ist die Videoquelle ordnungsgemäß mit der Erfassungs Hardware verbunden.

Bei der Schritt-Frame-Erfassung synchronisiert das Aufzeichnungs Fenster den Aufzeichnungs Vorgang und kompensiert die Verzögerungen, die mit der Positionierung der MCI-Videoquelle und der Initialisierung der zum Erfassen von Daten erforderlichen Ressourcen verbunden sind. Außerdem wird durch das Erfassungsfenster sichergestellt, dass keine Frames abgelegt werden. die Video Frames werden einzeln durchlaufen, um sicherzustellen, dass der Frame aufgezeichnet und gespeichert wird, bevor der nächste Frame im Videostream erfasst wird.

Spezifikationen zum Steuern der Schritt-Frame-Erfassung werden in den Membern der [**captumappms**](/windows/win32/api/vfw/ns-vfw-captureparms) -Struktur gespeichert. Die Schritt-für-Schritt-Erfassung verwendet die folgenden Member zusätzlich zu den Membern, die für die echt Zeiterfassung verwendet werden: **fstepmcidevice**, **fStepCaptureAt2x** und **wstepcaptureaverageframes**. Wenn das **fstepmcidevice** -Element auf **true** festgelegt ist, koordiniert das Erfassungsfenster die Schritt-Frame-Erfassung. Das Erfassungsfenster verwendet die Parameter, die in den Elementen **dwmcistarttime** und **dwmcistoptime** angegeben sind, für die Start-und Stop-Positionen der Sequenz. Das Erfassungsfenster bestimmt mithilfe von **fStepCaptureAt2x** , ob die Aufzeichnungs Hardware Video Frames bei der doppelten Auflösung aufzeichnen soll, und verwendet **wstepcaptureaverageframes** , um anzugeben, wie oft jeder Frame im Aufzeichnungs Vorgang als Stichprobe verwendet wird.

Wenn **fstepmcidevice** den Wert **false** hat, wird die echt Zeiterfassung anstelle der Schritt-Frame-Erfassung verwendet, und der Inhalt von **fStepCaptureAt2x** und **wstepcaptureaverageframes** werden ignoriert.

Wenn eine Schritt-Frame-Erfassung angegeben und **fStepCaptureAt2x** auf **true** festgelegt ist, erfasst die Erfassungs Hardware bei der doppelten Auflösung die angegebene Auflösung. (Die Auflösung von Höhe und Breite wird verdoppelt.) Die Software interpoliert die Pixel im Bild mit höherer Auflösung, um das Bild bei der angegebenen Auflösung zu entwickeln. Diese Form der Durchschnittsberechnung kann die Kantendefinition von Bildern in einem Frame verbessern. Sie können diese Option aktivieren, wenn die Hardware keine hardwarebasierte Dezimierung unterstützt und Sie das RGB-Format erfassen.

> [!Note]  
> Wenn Ihre Hardware hardwarebasierte dezimierungen unterstützt, können Sie Stichproben mit einer höheren Rate als angegeben erfassen und diese zusätzlichen Beispiele zum Abrufen von Farb Definitionen verwenden, die mit dem Original Abbild konsistent sind. Die zusätzlichen Beispiele werden verworfen, nachdem Sie verwendet wurden, und die Hardware übergibt Beispiele an den Erfassungs Treiber mit der angegebenen Rate.

 

Wenn eine Schritt-für-Schritt-Erfassung angegeben wird, gibt das **wstepcaptureaverageframes** -Element an, wie oft ein Frame Stichprobe bei der Erstellung eines Frames auf der Grundlage des durchschnittlichen Beispiels ist. Diese Mittelwert Technik reduziert das Zufallsprinzip der Digitalisierung, das in einem Frame auftritt. Ein typischer Wert für die Anzahl der Durchschnittswerte ist 5.

Weitere Informationen zu MCI finden Sie unter [MCI](mci.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erfassungs Variationen](capture-variations.md)
</dt> </dl>

 

 




