---
description: Standard Anmerkungen und-Semantik (dxsas) stellen eine Methode dar, mit der Shader auf eine standardmäßige Weise verwendet werden können, mit der Shader mit Tools, Anwendungen und Spiel Modulen verwendet werden können.
ms.assetid: b3206b30-56b4-4d56-a778-af3a6b3b8d9c
title: DirectX-Standard Anmerkungen und Semantik Referenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c989f4aed7c01c62d6133e01fe035223b74c8d3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481694"
---
# <a name="directx-standard-annotations-and-semantics-reference"></a>DirectX-Standard Anmerkungen und Semantik Referenz

Standard Anmerkungen und-Semantik (dxsas) stellen eine Methode dar, mit der Shader auf eine standardmäßige Weise verwendet werden können, mit der Shader mit Tools, Anwendungen und Spiel Modulen verwendet werden können. Dxsas definiert einen Satz von Semantik und Anmerkungen, die an Host Anwendungs Werte und Effektparameter zum Zweck der Freigabe von Effekten angefügt werden. Damit diese Anmerkungen und Semantik nützlich sein können, müssen Sie sowohl in der Host Anwendung als auch in der Effekt Datei implementiert werden. In diesem Dokument wird der dxsas-Standard beschrieben, der die Leistungsfähigkeit des DirectX-Effekts-Frameworks nutzt, damit Host Anwendungen und-Tools DirectX-Effekte (FX-Dateien) Programm gesteuert freigeben und die Interaktion mit der Benutzeroberfläche entwerfen können.

## <a name="background-information"></a>Hintergrundinformationen

Standard Anmerkungen und-Semantik dienen zum Binden von Effekt-und X-Datei Parametern zum Hosten von Anwendungs Werten. Das D3DX Effect-Framework (oder Effekte) kapselt den Renderingzustand. Durch das Kapseln eines Renderingzustands (einschließlich Scheitelpunkt, Textur und Pixel Verarbeitungs Status) können Sie eine Reihe von Effekten erstellen, die eine Vielzahl von Renderingoptionen abdecken. Dies kann z. b. Optionen wie das Rendern auf verschiedenen Hardwaretypen oder das Rendering mit Einzel-oder Multipass-Blending einschließen. Weitere Informationen zum Effect-Framework finden Sie unter [Wirkungs Referenz](dx9-graphics-reference-effects.md). Dxsas basiert auf diesem Framework und ermöglicht Entwicklern ein konsistenteres Verhalten. Sobald das renderingsetup in einem Effekt gekapselt ist, ermöglicht der dxsas-Standard dem Effekt Entwickler das verfügbar machen der Absicht der Effektparameter mithilfe von Anmerkungen. Diese Anmerkungen können dann von jeder Host Anwendung oder einem Tool gelesen werden (nicht nur die, die für die Verwendung des Effekts entworfen wurde), die mit dem Standard kompatibel ist. Sie erfahren, wie Sie die Auswirkungen in der Art und Weise verwenden, die entworfen wurde.

Durch die Standardisierung des Satzes von Effekt Semantik und Anmerkungen, die von Host Anwendungen unterstützt werden, können Autoren Ergebnisse erzeugen, die in mehreren Projekten verwendet werden können. auf diese Weise wird eine breitere Community von Effekten für Benutzer herauf gestuft. Der dxsas-Standard macht von Entwicklern lesbare Dateien, die zwischen Tools austauschbar sind, und ermöglicht Entwicklern das Nutzen von Drittanbieter Tools zum Erstellen von Effekten für ihre Pipeline.

In diesem Dokument wird der dxsas-Standard beschrieben, der mithilfe von Anmerkungen die Absicht von Effekt Parametern ausdrückt und eine Auflistung von Host Anwendungs Werten definiert, denen Host Anwendungen zustimmen, dass Sie für einen Effekt verfügbar gemacht werden.

## <a name="authoring-effects-with-standard-annotations-and-semantics"></a>Erstellen von Effekten mit Standard Anmerkungen und Semantik

Wie Sie aus dem folgenden Diagramm sehen können, erfordert der dxsas-Standard Anmerkungen in einer Effekt Datei sowie eine Host Anwendung, die die hier beschriebenen Richtlinien befolgt, um mit der Datei zu arbeiten.

![Diagramm des dxsas-Standards für Host Anwendungen und Effekt Dateien](images/sas-2.png)

Die Host Anwendung muss die Benutzeroberflächen Logik und die Host Umgebung implementieren. Informationen zum Implementieren von dxsas-kompatiblen Effekten finden Sie in den folgenden Themen:

-   Der [globale Parameter](global-parameter.md) definiert Informationen, die für den Effekt relevant sind, z. b. die Version oder den Effekt Autor.
-   Die [Datenbindung](data-binding.md) definiert die Auflistung von Parametern (sowie deren Typ und Struktur), die von einem Effekt verwendet werden können, der von der Host Anwendung festgelegt werden kann, die für Effekte verfügbar gemacht wird.
-   Wenn Sie ein Benutzeroberflächen Steuerelement einem Effektparameter zuordnen möchten, verwenden Sie eine [UI](ui-annotation.md)-Anmerkung. Folgende Anmerkungen sind enthalten: [sasuimax](ui-annotation.md), [sasuimin](ui-annotation.md), [sasuisteps](ui-annotation.md), [sasuistepspower](ui-annotation.md)und [sasuistride](ui-annotation.md).
-   Um einen Effektparameter mit Daten in einer externen Datei zu initialisieren, verwenden Sie eine [Parameter Initialisierungs Anmerkung](parameter-initialization-annotation.md).
-   Wenn Daten zwischen der Host Anwendung und einem Effekt (oder umgekehrt) übertragen werden, treten [Umwandlungen und Konvertierungen](casting-and-conversion.md) auf, wenn die Typen nicht genau übereinstimmen. In diesem Abschnitt wird angegeben, wie Daten geschrieben werden, wenn sich die Quell-und Zieltypen unterscheiden. Verwenden Sie außerdem [parametervaluemodifier](casting-and-conversion.md) , um zu ändern, wie die Host Anwendung aus dem Effekt-Parameter gelesene Daten interpretieren soll. Folgende Anmerkungen sind enthalten: [sasnormalize](casting-and-conversion.md) und [sasunits](casting-and-conversion.md).

## <a name="case-sensitivity"></a>Groß- und Kleinschreibung

Bei allen Bezeichner, Semantik und Anmerkung-Werten wird die Groß-/Kleinschreibung nicht beachtet. Bei Anmerkungen-Namen (keine Werte) wird die Groß-/Kleinschreibung beachtet Anmerkung-Namen werden vom D3DX Effects-System erkannt, und daher sind Namen von SAS-Anmerkungen ebenfalls zulässig.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effekt Referenz](dx9-graphics-reference-effects.md)
</dt> </dl>

 

 



