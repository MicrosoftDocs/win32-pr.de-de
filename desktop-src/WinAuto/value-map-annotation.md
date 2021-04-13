---
title: Werte Zuordnungs Anmerkung
description: Werte Zuordnungs Anmerkung
ms.assetid: f7c9304a-0eed-4a73-ab06-56723f3cfa5d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d21b04374344475689989c2570af6975dc97c13
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104552191"
---
# <a name="value-map-annotation"></a>Werte Zuordnungs Anmerkung

Mit der Wert Map-Anmerkung können Sie eine Zuordnungs Zeichenfolge verwenden, um anzugeben, wie der Bild Index eines Elements in einer Listenansicht oder Strukturansicht der Rolle bzw. dem Zustand entspricht. Beispielsweise kann eine Zuordnungs Zeichenfolge darauf hindeuten, dass der Bild Index 0 einer Listenansicht einer Rolle des Kontrollkästchens zugeordnet ist, während der Bild Index 1 einer Rolle eines Options Felds zugeordnet wird.

Sie können auch die Value Map-Anmerkung verwenden, um Zeichen folgen anzugeben, die den numerischen Werten eines Schiebereglers zugeordnet werden.

## <a name="when-to-use-this-technique"></a>Verwendungszwecke dieser Technik

Verwenden Sie in den folgenden Situationen die Verwendung der Wertkarten Anmerkung.

-   Wenn eine von einem Besitzer gezeichnete Listenansicht oder Strukturansicht die Verwendung von Bildern einschließt und Sie basierend auf diesem Bild eine benutzerdefinierte Beschreibungs Eigenschaft ([**Beschreibungs**](description-property.md) Eigenschaft) bereitstellen möchten. Die folgende Abbildung zeigt ein Beispiel.

    ![Abbildung des Startmenüs, wobei Symbole visuelle Hinweise zu Inhalten bereitstellen](images/iconlist.gif)

-   Wenn ein vom Besitzer gezeichnetes Listenansicht-oder Strukturansicht-Steuerelement die Verwendung von Bildern integriert, um die Struktur oder die Listenelemente wie einfache Steuerelemente zu agieren, werden in der Regel Kontrollkästchen oder Options Felder verwendet, und Sie möchten das Bild einer Rolle zuordnen. Der folgende Screenshot zeigt ein Beispiel.

    ![Screenshot der Internet Explorer-Optionen zum Festlegen des Werts von Kontrollkästchen und Options Feldern](images/customlist.gif)

-   Wenn ein Schieberegler verwendet wird, um einen Wert auszuwählen, der als etwas anderes als eine einfache Ganzzahl beschrieben werden kann, wie im folgenden Screenshot, bei dem die Einstellung für die Bildschirmauflösung durch eine Zeichenfolge beschrieben wird.

    ![Screenshot eines Schiebereglers, der zum Festlegen der Bildschirmauflösung verwendet wird](images/slider.gif)

Mit der Wertkarten Anmerkung gibt eine Zuordnungs Zeichenfolge an, wie der Bildindex der Liste oder der Struktur der Rolle bzw. dem Zustand entspricht. Oder es kann angegeben werden, wie der numerische Wert eines Schiebereglers einer Zeichenfolge entspricht. Beispielsweise kann eine Zuordnungs Zeichenfolge darauf hindeuten, dass der Bild Index 0 einer Listenansicht einer Rolle des Kontrollkästchens zugeordnet ist und Bild Index 1 einer Rolle eines Options Felds zugeordnet wird. Verwenden Sie [**IAccPropServices:: sthwndpropstr ()**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) , um die Mapping-Zeichenfolge an das-Steuerelement anzufügen.

Da für die Unterstützung der Wertzuordnung Steuer spezifische Kenntnisse erforderlich sind, gibt es eine begrenzte Anzahl von Steuerelementen und Eigenschaften, die eine Wertkarten Anmerkung unterstützen, einschließlich Schieberegler-Werte Zuordnungen, Listenansichten und Struktur Ansichten.

## <a name="slider-value-map&quot;></a>Schieberegler-Wertkarte

**PROPID \_ ACC \_ ValueMap** enthält eine Zuordnung von internen Schieberegler-Positionen zu lesbaren Zeichen folgen. Diese Eigenschaft wird vom Oleacc.dll Schieberegler-Proxy unterstützt. Wenn der aktuelle Schieberegler-Wert in der Werte Zuordnung gefunden wird, wird die entsprechende Zeichenfolge als-Wert anstelle der standardmäßigen Prozent Zeichenfolge (z. b. &quot;50") verfügbar gemacht.

## <a name="list-view-and-tree-view"></a>Listenansicht und Strukturansicht

**PROPID \_ Die \_** Tools für die Bereitstellung von "rolemap", " **PROPID \_ ACC \_**" und " **PROPID- \_ ACC \_** " bieten Zuordnungen von Zustands Bild Indizes zu Rollen-und Zustands Werten. Diese Zuordnungen ermöglichen die Zuordnung dieser Bild Indizes zu den entsprechenden Rollen (normalerweise die Options Schaltfläche des [**Rollen \_ Systems \_**](object-roles.md) oder das [**\_ \_ Häkchen des Rollen**](object-roles.md)Systems) und zusätzliche Zustands Bits (normalerweise über [**\_ \_ prüfte Zustands Systeme**](object-state-constants.md)).

Weitere Informationen zur Anmerkung von Wertkarten finden Sie in den folgenden Themen:

-   [Verwenden von Value Map-Anmerkungen](using-value-map-annotation.md)
-   [Beispiel für eine wertmap-Anmerkung](value-map-annotation-sample.md)

## <a name="annotation-map-format"></a>Annotation-Zuordnungs Format

In der folgenden Tabelle werden die Felder beschrieben, die in einer Anmerkung enthalten sind.



| Feld               | BESCHREIBUNG                                                                                                                                                                                                                                                                   |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ein                 | Gibt an, dass ein bestimmtes Codierungsschema verwendet wird. Für künftige Codierungs Schemas werden möglicherweise zusätzliche Präfixe unterstützt.                                                                                                                                                          |
| Trennzeichen | Normalerweise ein Doppelpunkt (:) wird verwendet, kann jedoch ein anderes Zeichen mit Ausnahme von **null** oder einem leeren Leerzeichen sein. Da dieses Zeichen als Trennzeichen für die verbleibenden Felder verwendet wird, kann es nicht als Teil eines Werts in der Zuordnung verwendet werden.                                               |
| 0, 1 oder 2          | Ein Wert, der angibt, welcher Schlüssel verwendet wird. Für die Strukturansicht und die Listen Ansichts Rollen-und Zustands Zuordnungen kann dieser Schlüssel 0 (Bild Index), 1 (State Image Index) oder 2 (Überlagerungs Bild Index) sein. Für Schieberegler und andere Steuerelemente, die keine Schlüsselauswahl bieten, muss dieser Wert 0 (null) sein. |
| Trennzeichen | :                                                                                                                                                                                                                                                                             |
| Schlüssel-Wert-Paare     | Jedes Paar besteht aus einer Schlüssel Zeichenfolge und einem Trennzeichen. Die Schlüssel Zeichenfolge ist eine Zahl, die sich im Dezimal-oder Hexadezimal Format (mit dem vorangehendem Präfix "0x") befinden kann.                                                                                                            |
| Wert Zeichenfolge        | Bei Wert Maps ist dies eine Zeichenfolge. Bei Rollen-und Zustands Zuordnungen handelt es sich hierbei um eine Zahl (Decimal oder hexadezimal).                                                                                                                                                                         |
| Trennzeichen | :                                                                                                                                                                                                                                                                             |



 

Eine Karte könnte beispielsweise wie folgt aussehen:


```C++
A:0:0:Cold:1:Warm:3:Hot:
```



Wenn diese Werte Zuordnung auf ein Schieberegler-Steuerelement angewendet wird, wird der Wert "warm" angezeigt, wenn sich der Schieberegler an Position 1 befindet. Da Wert 2 in diesem Beispiel nicht enthalten ist, wird der Standardwert für diese Position verfügbar gemacht. Der Standardwert für einen Schieberegler ist ein Prozentwert, z. b. 33.

 

 




