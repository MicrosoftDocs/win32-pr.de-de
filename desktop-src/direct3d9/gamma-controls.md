---
description: Mit Gamma Steuerelementen können Sie ändern, wie das System den Inhalt der Oberfläche anzeigt, ohne dass sich dies auf den Inhalt der Oberfläche auswirkt.
ms.assetid: 74f106be-8f47-4875-9908-32ff35912968
title: Gamma Steuerelemente (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6484bcf7e8fa5e07a3bf4bb718cd361330560f8c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104569434"
---
# <a name="gamma-controls-direct3d-9"></a>Gamma Steuerelemente (Direct3D 9)

Mit Gamma Steuerelementen können Sie ändern, wie das System den Inhalt der Oberfläche anzeigt, ohne dass sich dies auf den Inhalt der Oberfläche auswirkt. Stellen Sie sich diese Steuerelemente als sehr einfache Filter vor, die Direct3D auf Daten anwenden, wenn Sie eine Oberfläche verlassen und bevor Sie auf dem Bildschirm gerendert werden.

Gamma Steuerelemente sind eine Eigenschaft einer Swapkette. Gamma Steuerelemente ermöglichen es, dynamisch zu ändern, wie die roten, grünen und blauen Ebenen einer Oberfläche den tatsächlich vom System angezeigten Ebenen zugeordnet werden. Durch Festlegen von Gamma Levels können Sie bewirken, dass der Bildschirm des Benutzers Farben blinkt, wenn das Zeichen des Benutzers gedreht wird, grün, wenn das Zeichen ein neues Element aufnimmt, usw., ohne neue Bilder in den Frame Puffer zu kopieren, um den Effekt zu erzielen. Oder Sie können Farbebenen so anpassen, dass Sie eine Farbabweichung auf die Bilder im Hintergrund Puffer anwenden.

Es gibt immer mindestens eine Austausch Kette (die implizite SwapChain) für jedes Gerät, da Direct3D 9 eine SwapChain als Eigenschaft des Geräts aufweist. Da es sich bei der Gamma-Rampe um eine Eigenschaft der Swapkette handelt, kann die Gamma-Rampe angewendet werden, wenn die SwapChain angezeigt wird. Die Gamma-Rampe tritt sofort in Kraft. Es wird nicht auf einen vertikalen Synchronisierungs Vorgang gewartet.

Mit den Methoden [**setgammaramp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) und [**getgammaramp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp) können Sie die von den roten, grünen und blauen Farbkomponenten von Pixeln betroffenen Ebenen auf der Oberfläche bearbeiten, bevor Sie zur Anzeige an den Digital-to-Analog Converter (DAC) gesendet werden.

## <a name="gamma-ramp-levels"></a>Gamma-Rampen Ebenen

In Direct3D beschreibt der Begriff "Gamma Rampe" eine Reihe von Werten, die die Ebene einer bestimmten Farbkomponente (rot, grün, blau) für alle Pixel im Frame Puffer neuen Ebenen zuordnen, die von der DAC zur Anzeige empfangen werden. Die Neuzuordnung erfolgt mithilfe von drei Nachschlage Tabellen, einer für jede Farbkomponente.

So funktioniert es: Direct3D nimmt ein Pixel aus dem Frame Puffer und wertet seine einzelnen roten, grünen und blauen Farbkomponenten aus. Jede Komponente wird durch einen Wert zwischen 0 und 65535 dargestellt. Direct3D nimmt den ursprünglichen Wert an und verwendet ihn, um ein 256-Element-Array (die-Rampe) zu indizieren, wobei jedes Element einen Wert enthält, der das ursprüngliche-Element ersetzt. Direct3D führt diesen Such-und Ersetzungs Prozess für jede Farbkomponente jedes Pixels im Frame Puffer aus, sodass die endgültigen Farben für alle auf dem Bildschirm angezeigten Pixel geändert werden.

Es ist praktisch, die Schleifen Werte zu visualisieren, indem Sie Sie grafisch darstellen, wie in den folgenden beiden Diagrammen dargestellt. Das linke Diagramm zeigt eine Rampe, bei der keine Farben geändert werden. Das rechte Diagramm zeigt eine Abweichung, die der Farbkomponente, auf die Sie angewendet wird, einen negativen Bias auferlegt.

![Diagramme der Gamma-Ramp-Werte](images/gammalv.png)

Die Array Elemente für das Diagramm auf der linken Seite enthalten Werte, die mit Ihrem Index 0 im-Element bei Index 0 und 65535 bei Index 255 identisch sind. Diese Art von Rampe ist die Standardeinstellung, da Sie die Eingabewerte nicht ändert, bevor Sie angezeigt werden. Das rechte Diagramm bietet mehr Variation. die zugehörige-Rampe enthält Werte zwischen 0 (null) im ersten Element und 32768 im letzten-Element, wobei die Werte gleichmäßig dazwischen liegen. Der Effekt besteht darin, dass die Farbkomponente, die diese Rampe verwendet, auf der Anzeige stumm erscheint. Sie sind nicht auf die Verwendung von linearen Diagrammen beschränkt. , wenn Ihre Anwendung bei Bedarf eine beliebige Zuordnung zuweisen kann. Sie können sogar die Einträge auf alle Nullen festlegen, um eine Farbkomponente vollständig aus der Anzeige zu entfernen.

## <a name="setting-and-retrieving-gamma-ramp-levels"></a>Festlegen und Abrufen von Gamma-Verlaufs Ebenen

Gamma-Verlaufs Ebenen sind effektive Nachschlage Tabellen, die von Direct3D verwendet werden, um die Komponenten von Frame-Puffer Farben neuen Ebenen zuzuordnen, die angezeigt werden. Sie können die hubebenen für die primäre Oberfläche festlegen und abrufen, indem Sie die Methoden [**setgammaramp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) und [**getgammaramp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp) aufrufen. **Setgammaramp** akzeptiert zwei Parameter, und **getgammaramp** akzeptiert einen Parameter. Bei **setgammaramp** lautet der erste Parameter entweder D3DSGR \_ kalibriate oder D3DSGR \_ No- \_ Kalibrierung. Der zweite Parameter, "pramp", ist ein Zeiger auf eine [**D3DGAMMARAMP**](d3dgammaramp.md) -Struktur. Die **D3DGAMMARAMP** -Struktur enthält 3 256-Element Arrays von Wörtern, jeweils ein Array, das die roten, grünen und blauen Gamma Rampen enthalten soll. **Getgammaramp** verfügt über einen Parameter, der einen Zeiger auf einen **D3DGAMMARAMP** -Typ annimmt, der mit der aktuellen Gamma-Rampe gefüllt wird.

Sie können den Wert D3DSGR \_ kaliate für den ersten Parameter von [**setgammaramp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) einschließen, um beim Festlegen neuer Gamma Ebenen den kalierer aufzurufen. Die Kalibrierung von Gamma Rampen verursacht einen gewissen Verarbeitungsaufwand und sollte nicht häufig verwendet werden. Das Festlegen einer kalibrierten Gamma-Rampe bietet einen konsistenten und absoluten Gamma Wert für den Benutzer, unabhängig vom Anzeige Adapter und-Monitor.

Nicht alle Systeme unterstützen die Gamma-Kalibrierung. Um zu ermitteln, ob die Gamma-Kalibrierung unterstützt wird, nennen Sie [**GetDeviceCaps**](/windows/desktop/api), und untersuchen Sie den Caps2-Member der zugeordneten [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) -Struktur, nachdem die-Methode Wenn das D3DCAPS2 \_ cancalibrategamma-funktionsflag vorhanden ist, wird die Gamma-Kalibrierung unterstützt.

Beachten Sie beim Festlegen neuer Rampen Ebenen, dass die Ebenen, die Sie in den Arrays festlegen, nur verwendet werden, wenn sich die Anwendung im Vollbildmodus im exklusiven Modus befindet. Wenn sich die Anwendung im normalen Modus ändert, werden die Schwellenwerte außer Kraft gesetzt und werden erneut wirksam, wenn die Anwendung den Vollbildmodus wieder aufnimmt.

Wenn das Gerät Gamma Rampen im aktuellen Präsentationsmodus der SwapChain (Vollbild oder Fenster) nicht unterstützt, wird kein Fehlerwert zurückgegeben. Anwendungen können die D3DCAPS2 \_ fullscreengamma-und D3DCAPS2 \_ cancalibrategamma-Funktions Bits im Caps2-Member des D3DCAPS9-Typs überprüfen, um die Funktionen des Geräts zu ermitteln und festzulegen, ob ein kalikalierer installiert ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Oberflächen](direct3d-surfaces.md)
</dt> </dl>

 

 
