---
description: Mit Gammasteuerelementen können Sie ändern, wie das System den Inhalt der Oberfläche anzeigt, ohne den Inhalt der Oberfläche selbst zu beeinflussen.
ms.assetid: 74f106be-8f47-4875-9908-32ff35912968
title: Gamma-Steuerelemente (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5074f60199364ba86a0b5ad743fcc03121351cad0ac071d9231beef7c7156f9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122203"
---
# <a name="gamma-controls-direct3d-9"></a>Gamma-Steuerelemente (Direct3D 9)

Mit Gammasteuerelementen können Sie ändern, wie das System den Inhalt der Oberfläche anzeigt, ohne den Inhalt der Oberfläche selbst zu beeinflussen. Stellen Sie sich diese Steuerelemente als sehr einfache Filter vor, die Direct3D auf Daten anwendet, während sie eine Oberfläche verlassen und bevor sie auf dem Bildschirm gerendert werden.

Gammasteuerelemente sind eine Eigenschaft einer Swapkette. Gammasteuerelemente ermöglichen es, dynamisch zu ändern, wie die Rot-, Grün- und Blauwerte einer Oberfläche den tatsächlichen Ebenen zugeordnet werden, die das System anzeigt. Durch Festlegen von Gammawerten können Sie bewirken, dass der Bildschirm des Benutzers Farben blinkt – Rot, wenn das Zeichen des Benutzers gedreht wird, Grün, wenn das Zeichen ein neues Element aufnimmt usw., ohne neue Bilder in den Framepuffer zu kopieren, um den Effekt zu erzielen. Alternativ können Sie Farbebenen anpassen, um eine Farbabweichung auf die Bilder im Hintergrundpuffer anzuwenden.

Es gibt immer mindestens eine Swapkette (die implizite Swapkette) für jedes Gerät, da Direct3D 9 über eine Swapkette als Eigenschaft des Geräts verfügt. Da die Gamma-Rampe eine Eigenschaft der Swapkette ist, kann die Gamma-Rampe angewendet werden, wenn die Swapkette eingeblendet wird. Die Gamma-Rampe wird sofort wirksam. Es wird nicht auf einen vertikalen Synchronisierungsvorgang gewartet.

Mit den [**Methoden SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) und [**GetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp) können Sie Rampenebenen bearbeiten, die sich auf die Rot-, Grün- und Blaufarbkomponenten von Pixeln von der Oberfläche auswirken, bevor sie zur Anzeige an den Digital-to-Analog-Konverter (Digital-to-Analog Converter, DAC) gesendet werden.

## <a name="gamma-ramp-levels"></a>Gammaverlaufsebenen

In Direct3D beschreibt der Begriff Gammaverlauf eine Reihe von Werten, die den Grad einer bestimmten Farbkomponente (rot, grün, blau) für alle Pixel im Framepuffer neuen Ebenen zuordnen, die von der DAC zur Anzeige empfangen werden. Die Neuzuordnung erfolgt über drei Nachschlagetabellen, eine für jede Farbkomponente.

So funktioniert es: Direct3D nimmt ein Pixel aus dem Framepuffer und wertet seine einzelnen Rot-, Grün- und Blau-Farbkomponenten aus. Jede Komponente wird durch einen Wert von 0 bis 65535 dargestellt. Direct3D verwendet den ursprünglichen Wert und verwendet ihn zum Indizierung eines Arrays mit 256 Elementen (der Rampe), wobei jedes Element einen Wert enthält, der den ursprünglichen ersetzt. Direct3D führt diesen Such- und Ersetzungsprozess für jede Farbkomponente jedes Pixels im Framepuffer aus und ändert so die endgültigen Farben für alle Bildschirmpixel.

Es ist praktisch, die Rampenwerte zu visualisieren, indem Sie sie grafisch darstellen, wie in den folgenden beiden Diagrammen gezeigt. Das linke Diagramm zeigt eine Rampe, die die Farben überhaupt nicht ändert. Das rechte Diagramm zeigt eine Rampe, die eine negative Verschiebung auf die Farbkomponente erzwingt, auf die sie angewendet wird.

![Graphen der Gammaverlaufswerte](images/gammalv.png)

Die Arrayelemente für das Diagramm auf der linken Seite enthalten Werte, die mit ihrem Index identisch sind: 0 im Element bei Index 0 und 65535 bei Index 255. Diese Art von Rampe ist die Standardeinstellung, da sie die Eingabewerte nicht ändert, bevor sie angezeigt werden. Das rechte Diagramm bietet mehr Abweichungen. Die Rampe enthält Werte zwischen 0 im ersten Element und 32768 im letzten Element, wobei werte gleichmäßig dazwischen liegen. Der Effekt ist, dass die Farbkomponente, die diese Rampe verwendet, stumm auf der Anzeige angezeigt wird. Sie sind nicht auf die Verwendung von linearen Diagrammen beschränkt. , wenn Ihre Anwendung bei Bedarf eine beliebige Zuordnung zuweisen kann. Sie können sogar die Einträge auf alle Nullen festlegen, um eine Farbkomponente vollständig aus der Anzeige zu entfernen.

## <a name="setting-and-retrieving-gamma-ramp-levels"></a>Festlegen und Abrufen von Gammaverlaufsebenen

Gammaverlaufsebenen sind effektiv Nachschlagen von Tabellen, die Direct3D verwendet, um die Framepufferfarbkomponenten neuen Ebenen zuzuordnen, die angezeigt werden. Sie können Rampenebenen für die primäre Oberfläche festlegen und abrufen, indem Sie die [**Methoden SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) und [**GetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp) aufrufen. **SetGammaRamp** akzeptiert zwei Parameter, **und GetGammaRamp** akzeptiert einen Parameter. Für **SetGammaRamp** ist der erste Parameter entweder D3LOCKR \_ CALIBRATIONE oder D3GABER \_ NO \_ CALIBRATION. Der zweite Parameter, pRamp, ist ein Zeiger auf eine [**D3DGAMMARAMP-Struktur.**](d3dgammaramp.md) Die **D3DGAMMARAMP-Struktur** enthält drei 256-Element-Arrays von WORDs, jeweils ein Array, das die roten, grünen und blauen Gamma-Rampen enthält. **GetGammaRamp** verfügt über einen Parameter, der einen Zeiger auf einen **D3DGAMMARAMP-Typ** annimmt, der mit der aktuellen Gammaverlauf gefüllt wird.

Sie können den \_ D3LOCKR-KALIBRIERUNGswert für den ersten Parameter von [**SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) einschließen, um den Kalibrierer aufzurufen, wenn Sie neue Gammawerte festlegen. Das Kalibrieren von Gamma-Rampen verursacht einen gewissen Verarbeitungsaufwand und sollte nicht häufig verwendet werden. Das Festlegen einer kalibrierten Gamma-Rampe bietet dem Benutzer unabhängig vom Anzeigeadapter und Monitor einen konsistenten und absoluten Gammawert.

Nicht alle Systeme unterstützen die Gamma-Kalibrierung. Rufen [**Sie GetDeviceCaps**](/windows/desktop/api)auf, und untersuchen Sie den Caps2-Member der zugeordneten [**D3DCAPS9-Struktur,**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) nachdem die Methode zurückgegeben wurde, um zu ermitteln, ob die Gamma-Kalibrierung unterstützt wird. Wenn das D3DCAPS2 \_ CANCALIBRATEGAMMA-Funktionsflag vorhanden ist, wird die Gamma-Kalibrierung unterstützt.

Beachten Sie beim Festlegen neuer Rampenebenen, dass die Ebenen, die Sie in den Arrays festlegen, nur verwendet werden, wenn sich Ihre Anwendung im exklusiven Vollbildmodus befindet. Wenn ihre Anwendung in den normalen Modus wechselt, werden die Rampenebenen zurückgestellt, die wieder wirksam werden, wenn die Anwendung den Vollbildmodus wieder aktiviert.

Wenn das Gerät gamma ramps im aktuellen Präsentationsmodus der Swapkette (Vollbild oder Fenster) nicht unterstützt, wird kein Fehlerwert zurückgegeben. Anwendungen können die Funktionsbits D3DCAPS2 \_ FULLSCREENGAMMA und D3DCAPS2 \_ CANCALIBRATEGAMMA im Caps2-Member des D3DCAPS9-Typs überprüfen, um die Funktionen des Geräts zu bestimmen und zu ermitteln, ob ein Kalibrierer installiert ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Oberflächen](direct3d-surfaces.md)
</dt> </dl>

 

 
