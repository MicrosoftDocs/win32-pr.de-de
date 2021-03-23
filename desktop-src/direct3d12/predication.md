---
title: Prädikation übersprungen
description: Das-Prädikat ist ein Feature, mit dem die GPU anstelle der CPU feststellen kann, ob ein Objekt nicht gezeichnet, kopiert oder versendet werden soll.
ms.assetid: 5c5138c7-f6e8-4646-961a-0e2312b5356b
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a18df35c94fbd6b2b6f449585dfdcd4028bf2e9
ms.sourcegitcommit: 9dadca1a0d77cb2a372e5a941ec707f9d77b354d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2020
ms.locfileid: "104548725"
---
# <a name="predication"></a>Prädikation übersprungen

Das-Prädikat ist ein Feature, mit dem die GPU anstelle der CPU feststellen kann, ob ein Objekt nicht gezeichnet, kopiert oder versendet werden soll.

-   [Übersicht](#overview)
-   [Setprediation](#setpredication)
-   [Verwandte Themen](#related-topics)

## <a name="overview"></a>Überblick

Die typische Verwendung von Prädikaten ist die Okklusion. Wenn ein Begrenzungsfeld gezeichnet wird, das verdeckt wird, gibt es offensichtlich keinen Punkt, an dem das Objekt selbst gezeichnet wird. In dieser Situation kann das Zeichnen des Objekts "predicated" lauten, wodurch die Entfernung aus dem tatsächlichen Rendering durch die GPU ermöglicht wird.

Zunächst erscheint dies möglicherweise auf dem Standard tiefen Test plus einem frühen tiefen Durchlauf. Mit dem Prädikat kann jedoch der Aufwand des Draw-Befehls Zustands selbst und der rasterisierung entfernt werden. Während ein frühes tiefen Durchlauf unnötige Pixel entfernt, kann er weiterhin Scheitelpunkt-, Hull-, Domänen-und Geometry-Shader ausführen und den Eingabe Assembler, den tesselator und den Rasterizer für die Fixed-Funktion aufrufen. Durch das Zeichnen eines einfachen Begrenzungs Rahmens oder eines ähnlichen umgebenden Volumes &mdash; , das einfacher zu verarbeiten und zu verkleinern ist als das reale Modell, &mdash; vermeiden Sie unnötige rasterisierung und Verarbeitung.

Im Gegensatz zu Direct3D 11 wird das Prädikat von Abfragen entkoppelt und in Direct3D 12 erweitert, um einer Anwendung das Prädikat von Objekten basierend auf den Argumenten zu ermöglichen, für die der App-Entwickler möglicherweise entscheidet (nicht nur für die oksion).

## <a name="setpredication"></a>Setprediation

Das Prädikat kann basierend auf dem Wert von 64-Bits innerhalb eines Puffers festgelegt werden (siehe [**D3D12 \_ \_ prediationop**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op)).

Wenn die GPU einen [**setprediationbefehl**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication) ausführt, wird der Wert im Puffer angezeigt. Zukünftige Änderungen an den Daten im Puffer wirken sich nicht rückwirkend auf den prädikationszustand aus.

Wenn der Eingabeparameter Puffer NULL ist, wird das Prädikat deaktiviert.

Prädikationshinweise sind nicht in der Direct3D 12-API vorhanden. und ein Prädikat ist in den Befehlslisten direkt, COMPUTE und Copy zulässig. Der Quell Puffer kann einen beliebigen heaptyp aufweisen (Standard, Upload, Read Back, Custom).

Die Core-Laufzeit überprüft Folgendes:

-   *Alignedbufferoffset* ist ein Vielfaches von 8 Bytes.
-   Die Ressource ist ein Puffer.
-   Der Vorgang ist ein gültiger Member der-Enumeration.
-   " [**Setprediation**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication) " kann nicht innerhalb eines Pakets aufgerufen werden.
-   Der Befehls Auflistungstyp unterstützt das Prädikat.
-   Der Offset überschreitet die Puffergröße nicht.

Die debugschicht gibt einen Fehler aus, wenn sich der Quell Puffer nicht im [**D3D12_RESOURCE_STATE_PREDICATION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) befindet (der mit [**D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)und einfach einem Alias)-Zustand ist.

Die folgenden Vorgänge können als Prädikat festgelegt werden:

-   [**Drawinstanzierte**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced)
-   [**Drawindexedinstangeleitet**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced)
-   [**Dispatch**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
-   [**Copytextureregion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [**Copybufferregion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [**Copyresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [**Copytiles**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [**Resolvesubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource)
-   [**ClearDepthStencilView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-cleardepthstencilview)
-   [**ClearRenderTargetView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview)
-   [**Clearunorderedaccessviewuint**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
-   [**Clearunorderedaccessviewfloat**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
-   [**Executin Direct**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect)

[**Executebundle**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle) ist nicht selbst vorgegeben. Stattdessen werden die einzelnen Vorgänge aus der Liste oben, die auf der Seite des Bündels enthalten sind, als Prädikat festgestellt.

Die ID3D12GraphicsCommandList-Methoden [**resolvequerydata**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata), [**beginquery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) und [**endquery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) sind nicht als Prädikat festgelegt.

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Zähler und Abfragen](counters-and-queries.md)
</dt> <dt>

[Leistungsmessung](performance-measurement.md)
</dt> <dt>

[Exemplarische Vorgehensweise für prediationqueries](predication-queries.md)
</dt> </dl>

 

 




