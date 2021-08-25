---
title: Streamingerfassung von einem MCI-Gerät
description: Streamingerfassung von einem MCI-Gerät
ms.assetid: 44cbf375-f97e-426a-a703-dfb1b1933138
keywords:
- MCI (Media Control Interface), Streamingerfassung
- WM_CAP_SET_MCI_DEVICE-Nachricht
- capSetMCIDeviceName-Makro
- WM_CAP_GET_MCI_DEVICE Nachricht
- capGetMCIDeviceName-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24d469465f47e908bda2512261ea638ad23e931a43cbb0449df676829469c3d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892590"
---
# <a name="streaming-capture-from-an-mci-device"></a>Streamingerfassung von einem MCI-Gerät

MCI-Geräte unterstützen den Erfassungsvorgang in Echtzeiterfassung und Schrittframeerfassung. Sie können das MCI-Gerät angeben, z. B. videodisc oder video-cassette recorder (VCR), das als Videoquelle für Ihren Aufzeichnungsvorgang verwendet wird, indem Sie die [**WM \_ CAP SET \_ \_ MCI \_ DEVICE-Nachricht**](wm-cap-set-mci-device.md) (oder das [**Makro capSetMCIDeviceName)**](/windows/desktop/api/Vfw/nf-vfw-capsetmcidevicename) verwenden und den Namen des Geräts angeben. Sie können den derzeit festgelegten Gerätenamen auch mithilfe der [**WM \_ CAP GET \_ \_ MCI \_ DEVICE-Meldung**](wm-cap-get-mci-device.md) (oder des [**Makros capGetMCIDeviceName)**](/windows/desktop/api/Vfw/nf-vfw-capgetmcidevicename) abrufen.

Bei der Echtzeiterfassung synchronisiert das Erfassungsfenster den Erfassungsvorgang und gleicht Verzögerungen im Zusammenhang mit der Positionierung der MCI-Videoquelle und der Initialisierung der Ressourcen (z. B. Erfassungspuffer) aus, die zum Erfassen von Daten erforderlich sind. Das Erfassungsfenster erwartet, dass ein gültiges MCI-Videogerät im System installiert ist, um Daten auf diese Weise zu erfassen.

Spezifikationen zum Steuern eines MCI-Geräts werden in den Membern der [**CAPTUREPARMS-Struktur**](/windows/win32/api/vfw/ns-vfw-captureparms) gespeichert. MCI-kompatible Videoquellen umfassen VCRs undLaserdiscs. Wenn das **fMCIControl-Member** dieser Struktur auf **TRUE** festgelegt ist, koordiniert das Erfassungsfenster den MCI-Vorgang. Das Erfassungsfenster verwendet die in **den DwMCIStartTime-** und **dwMCIStopTime-Membern** angegebenen Parameter, um die Start- und Beendigungspositionen der Sequenz in Millisekunden zu erhalten. Wenn der Wert von **fMCIControl** **FALSE** ist, wird die Videoquelle nicht als MCI-Gerät behandelt, und der Inhalt von **dwMCIStartTime** und **dwMCIStopTime** wird ignoriert.

Sie können mit Media Player schnell überprüfen, ob ein MCI-Videogerät ordnungsgemäß mit dem System verbunden ist. Wenn Sie ein Gerät mit Media Player, wird überprüft, ob die MCI-Konfiguration für das Gerät korrekt ist. Wenn ein Bild auf der Videoanzeige angezeigt wird, ist die Videoquelle ordnungsgemäß mit der Erfassungshardware verbunden.

Bei der Schrittrahmenerfassung synchronisiert das Erfassungsfenster den Erfassungsvorgang und gleicht die Verzögerungen im Zusammenhang mit der Positionierung der MCI-Videoquelle und der Initialisierung der zum Erfassen von Daten erforderlichen Ressourcen aus. Darüber hinaus stellt das Erfassungsfenster sicher, dass keine Frames gelöscht werden. Sie durchlauft die Videoframes einzeln und stellt sicher, dass der Frame erfasst und gespeichert wird, bevor der nächste Frame im Videostream erfasst wird.

Spezifikationen zum Steuern der Schrittrahmenerfassung werden in den Membern der [**CAPTUREPARMS-Struktur**](/windows/win32/api/vfw/ns-vfw-captureparms) gespeichert. Die Schrittrahmenerfassung verwendet zusätzlich zu den Membern, die für die Echtzeiterfassung verwendet werden, die folgenden Member: **fStepMCIDevice,** **fStepCaptureAt2x** und **wStepCaptureAverageFrames**. Wenn das **fStepMCIDevice-Member** auf **TRUE** festgelegt ist, koordiniert das Erfassungsfenster die Schrittrahmenerfassung. Das Erfassungsfenster verwendet die in **den DwMCIStartTime-** und **dwMCIStopTime-Membern** angegebenen Parameter für die Start- und Beendigungspositionen der Sequenz in Millisekunden. Das Erfassungsfenster verwendet **fStepCaptureAt2x,** um zu bestimmen, ob die Erfassungshardware Videoframes mit doppelter normaler Auflösung erfassen soll, und **verwendet wStepCaptureAverageFrames,** um anzugeben, wie oft für jeden Frame im Erfassungsvorgang Stichproben erstellt werden.

Wenn **fStepMCIDevice** **auf FALSE** festgelegt ist, wird die Echtzeiterfassung anstelle der Schrittrahmenerfassung verwendet, und der Inhalt von **fStepCaptureAt2x** und **wStepCaptureAverageFrames** wird ignoriert.

Wenn eine Schrittrahmenerfassung angegeben und **fStepCaptureAt2x** auf **TRUE** festgelegt ist, wird die Erfassungshardware mit der doppelten angegebenen Auflösung erfasst. (Die Auflösungen von Höhe und Breite werden verdoppelt.) Die Software interpoliert die Pixel im Bild mit höherer Auflösung, um das Bild mit der angegebenen Auflösung zu erzeugen. Diese Form der Mittelung kann die Edgedefinition von Bildern in einem Frame verbessern. Sie können diese Option aktivieren, wenn die Hardware keine hardwarebasierte Dezimierung unterstützt und Sie die Erfassung im RGB-Format vornehmen.

> [!Note]  
> Wenn Ihre Hardware hardwarebasierte Dezimierung unterstützt, kann sie Stichproben mit einer höheren Rate als angegeben erfassen und diese zusätzlichen Beispiele verwenden, um Farbdefinitionen zu erhalten, die mit dem ursprünglichen Image konsistenter sind. Die zusätzlichen Stichproben werden verworfen, nachdem sie verwendet wurden, und die Hardware übergibt Stichproben mit der angegebenen Rate an den Erfassungstreiber.

 

Wenn eine Schrittrahmenerfassung angegeben wird, gibt das **wStepCaptureAverageFrames-Element** an, wie oft ein Frame beim Erstellen eines Frames basierend auf der durchschnittlichen Stichprobe entnommen wird. Diese Mittelungstechnik reduziert das zufällige Rauschen, das in einem Rahmen auftritt. Ein typischer Wert für die Anzahl der Durchschnittswerte ist 5.

Weitere Informationen zu MCI finden Sie unter [MCI](mci.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erfassungsvariationen](capture-variations.md)
</dt> </dl>

 

 




