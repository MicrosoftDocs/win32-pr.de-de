---
title: Bewährte Methoden für directcomposition
description: In diesem Thema werden bewährte Methoden für die Verwendung von Microsoft directcomposition beschrieben.
ms.assetid: D3A1ECD4-9358-44B9-8A84-7D901219D5CD
keywords:
- bewährte Methoden für directcomposition
- Empfohlene Vorgehensweisen für directcomposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0d19b82b188105c7914e89282c08b12dd4bdc4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729897"
---
# <a name="best-practices-for-directcomposition"></a>Bewährte Methoden für directcomposition

> [!NOTE]
> Für apps unter Windows 10 wird die Verwendung von Windows. UI. Composition-APIs anstelle von directcomposition empfohlen. Weitere Informationen finden Sie unter [modernisieren ihrer Desktop-App mithilfe der visuellen Ebene](/windows/uwp/composition/visual-layer-in-desktop-apps).

In diesem Thema werden bewährte Methoden für die Verwendung von Microsoft directcomposition beschrieben.

-   [bewährten Methoden](#best-practices-for-directcomposition)
-   [Überlegungen zur Sicherheit](#security-considerations)
-   [Zugehörige Themen](#related-topics)

## <a name="best-practices"></a>Bewährte Methoden

In der folgenden Tabelle sind die empfohlenen Vorgehensweisen für das Arbeiten mit Microsoft directcomposition-Visuals dargestellt.



| Üben                                                                                                                                                                                                                                                        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nachdem Sie ein directcomposition-Gerät erstellt haben, rufen Sie die [**idcompositiondevice:: CheckDeviceState**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-checkdevicestate) -Methode als Antwort auf jede [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) -Nachricht auf, um sicherzustellen, dass das Gerät noch gültig ist.<br/> | Wenn das Microsoft DirectX Graphics Infrastructure (DXGI)-Gerät verloren geht, geht auch das dem DXGI-Gerät zugeordnete directcomposition-Gerät verloren. Wenn ein verlorenes Gerät erkannt wird, sendet directcomposition die [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) -Meldung an alle Fenster. Wenn Sie [**CheckDeviceState**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-checkdevicestate) als Reaktion auf jede WM-Zeichnungs Nachricht aufrufen, können Sie bestimmen, ob das directcomposition-Geräte Objekt noch gültig ist, und andernfalls Schritte zum Wiederherstellen von Inhalten ausführen. **\_** <br/> Weitere Informationen finden Sie unter [Geräte Objekt](basic-concepts.md).<br/> |
| Erstellen Sie nur die Anzahl der visuellen Elemente, die für eine Komposition oder Animation benötigt werden, und zerstören Sie die visuellen Elemente sofort, sobald die directcomposition-Verwendung Sie beendet<br/>                                                                                            | Directcomposition verwendet die GPU (Graphics Processing Unit), eine Ressource, die Ihre Anwendung mit anderen Anwendungen und dem Betriebssystem freigibt. Dadurch wird sichergestellt, dass alle Anwendungen und das Betriebssystem geeignete GPU-Ressourcen erhalten.<br/> Weitere Informationen finden Sie unter [Visualisierungen](basic-concepts.md).<br/>                                                                                                                                                                                                                                                                     |
| Blenden Sie visuelle Elemente nicht durch Festlegen von Deckkraft auf 0% aus. Entfernen Sie stattdessen visuelle Elemente aus der visuellen Struktur.<br/>                                                                                                                                                          | Das Festlegen der Deckkraft auf 0% erfordert mehr Systemressourcen, als Sie aus der visuellen Struktur entfernt werden.<br/> Weitere Informationen finden Sie unter [Deckkraft](effects.md) und [visuelle](basic-concepts.md)Struktur.<br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| Blenden Sie ein visuelles Element nicht aus, indem Sie ein leeres Clip Rechteck (0) für ein visuelles Element anwenden. Entfernen Sie stattdessen die Visualisierung aus der visuellen Struktur. <br/>                                                                                                                 | Das Entfernen eines visuellen Elements aus der visuellen Struktur führt zu einer besseren Leistung als das Anwenden eines leeren Clip Rechtecks.<br/> Weitere Informationen finden Sie unter [Clipping](clipping.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Wenden Sie kein Clip Rechteck auf eine Visualisierung an, wenn das Clip Rechteck nicht benötigt wird, z. b. ein Clip Rechteck, das den gesamten Bitmapinhalt des visuellen Elements enthält.<br/>                                                                                       | Unnötige Clip Rechtecke beeinträchtigen die Systemleistung.<br/> Weitere Informationen finden Sie unter [Clipping](clipping.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Wenn Sie eine große, einzelfarbige Bitmap benötigen, erstellen Sie eine kleinere Bitmapoberfläche, und wenden Sie dann eine Skalierungs Transformation an, anstatt eine Oberfläche in voller Größe zu erstellen. <br/>                                                                                                | Das Anwenden einer Skalierungs Transformation auf eine kleinere Oberfläche verwendet weniger Systemressourcen als eine Oberfläche in voller Größe.<br/> Weitere Informationen finden Sie unter [Bitmap-Objekte](bitmap-surfaces.md) und- [Transformationen](transforms.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| Vermeiden Sie das Anwenden von 3D-Transformationen auf mehrere Ebenen einer visuellen Struktur, z. b. auf ein übergeordnetes Element und seine Nachfolger. <br/>                                                                                                                                        | Das Anwenden von 3D-Transformationen auf mehrere Ebenen eines visuellen Baums kann zu unbeabsichtigten Ergebnissen führen, da 3D-Transformationen nicht in der Struktur multipliziert werden. Beispielsweise führt eine 90-Grad-Drehung um die y-Achse eines untergeordneten Elements und eine 90-Grad-Drehung um die y-Achse eines übergeordneten Elements dazu, dass beide visuellen Elemente zu "Nothing" gedreht werden.<br/> Weitere Informationen finden Sie unter [Effekte](effects.md).<br/>                                                                                                                                                                                                     |



 

## <a name="security-considerations"></a>Sicherheitshinweise

Die folgenden Artikel bieten Anleitungen zum Schreiben von sicherem C++-Code.

-   [Bewährte Sicherheitsmethoden für C++](/cpp/security/security-best-practices-for-cpp?view=vs-2019)
-   [Muster & Praktiken Sicherheits Leit Fäden für Anwendungen](/previous-versions/msp-n-p/ff650760(v=pandp.10))

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von directcomposition](how-to-use-directcomposition.md)
</dt> </dl>

 

