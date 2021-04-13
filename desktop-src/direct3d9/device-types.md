---
description: Gerätetypen (Direct3D 9)
ms.assetid: 860f3de2-beaf-4df1-82d0-a4b7508156c2
title: Gerätetypen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c84efe80c022403c36e760860893f3619e1c9356
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341628"
---
# <a name="device-types-direct3d-9"></a>Gerätetypen (Direct3D 9)

## <a name="hal-device"></a>Hal-Gerät

Der primäre Gerätetyp ist das HAL-Gerät, das die Beschleunigung von Hardware-und Software Scheitel Punkten unterstützt. Wenn der Computer, auf dem die Anwendung ausgeführt wird, mit einem Anzeige Adapter ausgestattet ist, der Direct3D unterstützt, sollte die Anwendung ihn für Direct3D-Vorgänge verwenden. Direct3D HAL-Geräte implementieren den gesamten oder einen Teil der Transformations-, Beleuchtungs-und rasterisierungsmodule in der Hardware.

Anwendungen greifen nicht direkt auf Grafikadapter zu. Sie werden Direct3D-Funktionen und-Methoden aufgerufen. Direct3D greift über die HAL auf die Hardware zu. Wenn der Computer, auf dem Ihre Anwendung ausgeführt wird, die HAL unterstützt, wird die beste Leistung durch die Verwendung eines HAL-Geräts erzielt.

Um ein HAL-Gerät zu erstellen [**, rufen Sie**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) mit D3DDEVTYPE \_ HAL als Gerätetyp auf.

## <a name="reference-device"></a>Referenzgerät

Direct3D unterstützt einen zusätzlichen Gerätetyp, der als Verweis Gerät oder Referenz Raster bezeichnet wird. Anders als bei einem Software Gerät unterstützt der Verweis-Raster jede Direct3D-Funktion. Dieses Gerät soll zu Debuggingzwecken verwendet werden und ist daher nur auf Computern verfügbar, auf denen das DirectX SDK installiert wurde. Da diese Features für Genauigkeit und nicht für Geschwindigkeit implementiert werden und in Software implementiert werden, sind die Ergebnisse nicht sehr schnell. Der Verweis Raster nutzt immer dann besondere CPU-Anweisungen, aber er ist nicht für Einzelhandelsanwendungen vorgesehen. Verwenden Sie den verweisrasterizer nur zum Testen von Features oder Demonstrationszwecken. Um ein Referenzgerät zu erstellen, rufen Sie die Methode " [**kreatedevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) " mithilfe von D3DDEVTYPE \_ ref als Gerätetyp auf.

## <a name="hal-vs-ref-devices"></a>HAL-und ref-Geräte

Geräte und ref-Geräte (Referenz-Rasterizer) der HAL-Geräte (Hardware Abstraktionsschicht) sind die beiden Haupttypen des Direct3D-Geräts. der erste basiert auf der Hardwareunterstützung und ist sehr schnell, unterstützt jedoch möglicherweise nicht alles. während das zweite keine Hardwarebeschleunigung verwendet, ist es sehr langsam, aber es wird sichergestellt, dass der gesamte Satz von Direct3D-Features auf die richtige Weise unterstützt wird. Im Allgemeinen müssen Sie nur HAL-Geräte verwenden. Wenn Sie jedoch einige erweiterte Features verwenden, die von der Grafikkarte nicht unterstützt werden, müssen Sie möglicherweise auf "ref" zurückgreifen.

Der andere Zeitpunkt für die Verwendung von ref ist, dass das HAL-Gerät merkwürdige Ergebnisse erzeugt, d. h., Sie sind sicher, dass Ihr Code korrekt ist, aber das Ergebnis ist nicht das, was Sie erwarten. Es ist sichergestellt, dass das ref-Gerät ordnungsgemäß funktioniert, sodass Sie die Anwendung auf dem ref-Gerät testen und überprüfen können, ob das seltsame Verhalten weiterhin auftritt. Wenn dies nicht der Fall ist, bedeutet dies, dass für Ihre Anwendung (a) angenommen wird, dass die Grafikkarte etwas von der Grafikkarte unterstützt, oder (b) Es ist ein Treiber Fehler. Wenn es immer noch nicht mit dem ref-Gerät funktioniert, ist es ein Anwendungsfehler.

## <a name="hardware-vs-software-vertex-processing"></a>Hardware-und Software Scheitelpunkt Verarbeitung

Hardware-und softwarvertex-Verarbeitung gilt nur für Hal-Geräte. Wenn Sie Scheitel Punkte durch die Pipeline verschieben, müssen Sie (von der Welt, von der Sicht und von Projektions Matrizen) transformiert und beleuchtet werden (durch D3D's-integrierte Beleuchtung). diese Verarbeitungsphase wird als T&L (für Transformation & Beleuchtung) bezeichnet. Die Verarbeitung von Hardware Scheitel Punkten bedeutet, dass dies auf Hardware erfolgt, wenn Sie von der Hardware unterstützt wird. ERGO die Software Vertex-Verarbeitung erfolgt durch Software. Im Allgemeinen wird zunächst versucht, ein Hardware-T-&L-Gerät zu erstellen, und wenn dies fehlschlägt, versuchen Sie es mit einem gemischten Vorgang (Wenn die Software ausfällt, wird ein Fehler ausgegeben, und der Vorgang wird beendet.)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Geräte](direct3d-devices.md)
</dt> </dl>

 

 
