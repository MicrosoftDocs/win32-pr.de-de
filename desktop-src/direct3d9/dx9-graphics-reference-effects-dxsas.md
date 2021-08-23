---
description: Standardanmerkungen und -semantik (DXSAS) bieten eine Methode zur Verwendung von Shadern in einer Standardmethode, die die Verwendung von Shadern mit Tools, Anwendungen und Spiel-Engines ermöglicht.
ms.assetid: b3206b30-56b4-4d56-a778-af3a6b3b8d9c
title: DirectX-Standardanmerkungen und Semantikreferenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6da1489f92fce16e4717d501a64ab862fb9292c271397aa4a77e00e74c2e7952
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119373634"
---
# <a name="directx-standard-annotations-and-semantics-reference"></a>DirectX-Standardanmerkungen und Semantikreferenz

Standardanmerkungen und -semantik (DXSAS) bieten eine Methode zur Verwendung von Shadern in einer Standardmethode, die die Verwendung von Shadern mit Tools, Anwendungen und Spiel-Engines ermöglicht. DXSAS definiert eine Reihe von Semantiken und Anmerkungen, die an Hostanwendungswerte und Effektparameter angefügt werden, um Effekte zu teilen. Damit diese Anmerkungen und Semantik nützlich sind, müssen sie sowohl in der Hostanwendung als auch in der Effektdatei implementiert werden. In diesem Dokument wird der DXSAS-Standard beschrieben, der die Leistung des DirectX Effect Framework nutzt, um Hostanwendungen und Tools das programmgesteuerte Freigeben von DirectX-Effekten (FX-Dateien) zu ermöglichen und die Interaktion mit der Benutzeroberfläche zu entwerfen.

## <a name="background-information"></a>Hintergrundinformationen

Standardanmerkungen und -semantik sind so konzipiert, dass Effect- und X-Dateiparameter an Hostanwendungswerte gebunden werden. Das D3DX Effect Framework (oder Effekte) kapselt den Renderingzustand. Indem Sie den Renderingzustand (einschließlich Scheitelpunkt, Textur und Pixelverarbeitungszustand) in einem Effekt kapseln, können Sie eine Bibliothek mit Effekten erstellen, die eine Vielzahl von Renderingoptionen abdecken. Dies kann Optionen wie das Rendern auf verschiedenen Hardwaretypen oder das Rendern mit Single- oder Multi-Pass-Blending umfassen. Weitere Informationen zum Effektframework finden Sie unter [Effect Reference (Auswirkungsreferenz).](dx9-graphics-reference-effects.md) DXSAS baut auf diesem Framework auf und ermöglicht entwicklern eine konsistentere Benutzererfahrung. Sobald das Renderingsetup in einem Effekt gekapselt ist, ermöglicht der DXSAS-Standard dem Effektentwickler, die Absicht der Effektparameter über Anmerkungen verfügbar zu machen. Diese Anmerkungen können dann von jeder Hostanwendung oder jedem Tool gelesen werden (nicht nur von der Anwendung, die für die Verwendung des Effekts konzipiert wurde), die mit dem Standard kompatibel ist, um zu verstehen, wie der Effekt so verwendet wird, wie er entworfen wurde.

Durch die Standardisierung des Satzes von Effektsemantik und Anmerkungen, die Von Hostanwendungen unterstützt werden, können Effektautoren Effekte erstellen, die in mehreren Projekten verwendet werden können, und so eine größere Community von Effektbenutzern fördern. Der DXSAS-Standard macht Dateien für Entwickler lesbar, austauschbar zwischen Tools und ermöglicht Es Entwicklern, Drittanbietertools für die Erstellung von Effekten für ihre Pipeline zu nutzen.

In diesem Dokument wird der DXSAS-Standard beschrieben, der Anmerkungen verwendet, um die Absicht von Effektparametern auszudrücken. Außerdem wird eine Sammlung von Hostanwendungswerten definiert, die Hostanwendungen akzeptieren, um sie für einen Effekt verfügbar zu machen.

## <a name="authoring-effects-with-standard-annotations-and-semantics"></a>Erstellungseffekte mit Standardanmerkungen und Semantik

Wie Sie im folgenden Diagramm sehen können, erfordert der DXSAS-Standard Anmerkungen in einer Effektdatei sowie eine Hostanwendung, die den hier beschriebenen Richtlinien entspricht, um mit der Datei zu arbeiten.

![Diagramm des dxsas-Standards für Hostanwendungen und Effektdateien](images/sas-2.png)

Die Hostanwendung muss die Benutzeroberflächenlogik und die Hostumgebung implementieren. Lesen Sie die folgenden Themen, um DXSAS-kompatible Effekte zu implementieren:

-   Der [globale Parameter](global-parameter.md) definiert Informationen, die für den Effekt relevant sind, z. B. die Version oder den Effektautor.
-   [Die Datenbindung](data-binding.md) definiert die Auflistung von Parametern (sowie deren Typ und Struktur), die von einem Effekt verwendet werden können, der von der Hostanwendung festgelegt werden kann, die Auswirkungen ausgesetzt ist.
-   Um ein Benutzeroberflächensteuerelement einem Effect-Parameter zu zuordnen, verwenden Sie eine [Benutzeroberflächenanmerkung.](ui-annotation.md) Diese Anmerkungen umfassen: [SasUiMax](ui-annotation.md), [SasUiMin](ui-annotation.md), [SasUiSteps](ui-annotation.md), [SasUiStepsPower](ui-annotation.md)und [SasUiStride](ui-annotation.md).
-   Verwenden Sie eine Parameterinitialisierungsanmerkung, um einen Effect-Parameter mit Daten zu [initialisieren,](parameter-initialization-annotation.md)die in einer externen Datei enthalten sind.
-   Wenn Daten zwischen der Hostanwendung und einem Effekt (oder umgekehrt) übertragen [werden,](casting-and-conversion.md) treten Umwandlung und Konvertierung auf, wenn die Typen nicht genau übereinstimmen. In diesem Abschnitt wird angegeben, wie Daten geschrieben werden, wenn sich quell- und zieltypen unterscheiden. Verwenden Sie außerdem [ParameterValueModifiers,](casting-and-conversion.md) um zu ändern, wie die Hostanwendung aus dem Effect-Parameter gelesene Daten interpretieren soll. Zu diesen Anmerkungen gehören: [SasNormalize](casting-and-conversion.md) und [SasUnits.](casting-and-conversion.md)

## <a name="case-sensitivity"></a>Groß- und Kleinschreibung

Bei allen Bezeichnern, Semantik- und Anmerkungswerten wird die Groß-/Kleinschreibung nicht beachtet. Bei Anmerkungsnamen (nicht bei Werten) wird die Kleinschreibung beachtet. Anmerkungsnamen werden vom D3DX-Effektsystem erkannt, daher auch SAS-Anmerkungsnamen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Referenz zu Effekten](dx9-graphics-reference-effects.md)
</dt> </dl>

 

 



