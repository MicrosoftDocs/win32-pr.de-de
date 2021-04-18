---
description: Damit eine Anwendung ordnungsgemäß ausgeführt werden kann, müssen die entsprechenden DLLs auf dem Host Computer installiert sein. Diese DLLs können entweder vom Betriebssystem oder vom verteilbaren Paket der Anwendung bereitgestellt werden.
ms.assetid: fa5405e9-116f-4b7f-8f8e-791a79942570
title: Verknüpfen statischer und dynamischer Bibliotheken (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a7050b8a3b5e1e2544883eb140b67d50bc3cd11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106338899"
---
# <a name="linking-static-and-dynamic-libraries-direct3d-10"></a>Verknüpfen statischer und dynamischer Bibliotheken (Direct3D 10)

Damit eine Anwendung ordnungsgemäß ausgeführt werden kann, müssen die entsprechenden DLLs auf dem Host Computer installiert sein. Diese DLLs können entweder vom Betriebssystem oder vom verteilbaren Paket der Anwendung bereitgestellt werden.

## <a name="libraries-load-appropriate-dlls"></a>Bibliotheken laden geeignete DLLs

Die Bibliotheken, die im DirectX SDK enthalten sind, laden die richtigen DLLs zur Laufzeit automatisch. Die Ausnahme von dieser Regel ist d3dx10. lib/d3dx10d. lib, mit der die d3dx10.dll geladen wird, die mit dieser Version des SDK ausgeliefert wurde. Wenn das heruntergeladene SDK beispielsweise d3dx10 \_33.dll und d3dx10 \_34.dll enthält, wird die Bibliothek (d3dx10. lib), die mit diesem SDK ausgeliefert wurde, d3dx10 \_34.dll laden. Wenn ein nachfolgendes SDK später installiert wird \_ , das d3dx10 35. lib enthält, wird die Datei "d3dx10. lib" aus dem vorherigen SDK weiterhin d3dx10 \_34.dll geladen. Der d3dx10. lib-Eintrag aus dem neueren SDK lädt d3dx10 \_35.dll.

## <a name="redistributing-binaries"></a>Neuverteilen von Binärdateien

Nur d3dx10.dll (und nachfolgende Versionen der gleichen Datei) können neu verteilt werden. Zum erneuten Verteilen dieser Datei müssen Sie die **directxsetup** -Funktion verwenden. Ausführliche Informationen zur Verwendung dieser Funktion und zum Verbinden eines verteilbaren Pakets finden Sie unter [Installieren von DirectX mit DirectSetup](https://msdn.microsoft.com/library/Ee418267(v=VS.85).aspx). Alle anderen erforderlichen Binärdateien sind in Windows Vista enthalten. Die einzigen Binärdateien, die neu verteilt werden können, sind die, die sich im folgenden Verzeichnis befinden.


```
(SDK root)\Redist
```



In der folgenden Tabelle werden die Binärdateien beschrieben, die Entwicklern bekannt sein sollten.



| Direct3D 10-Binärdateien   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| d3dx10.dll/d3dx10d.dll | Einzelhandel und Debuggen d3dx10 Komponenten; die Einzelhandels Komponenten können im Redist-CAB neu verteilt werden.                                                                                                                                                                                                                                                                                                                                                                                                             |
| d3d10ref.dll           | Verweis Raster. Stellt die Software Implementierung der Grafik Pipeline bereit. Nur als Teil des DirectX SDK für Windows SDK oder Legacy enthalten und kann nicht weiter verteilt werden. Der Verweis Raster dient nur zum Debuggen. Explizites verknüpfen ist nicht erforderlich. Wenn Sie versuchen, ein Referenzgerät zu erstellen (siehe [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice)), wird diese DLL geladen, sofern Sie vorhanden ist.                                                                                                    |
| d3d10sdklayers.dll     | Eine Reihe von SDK-Hilfsprogrammen, die als Schicht zwischen API-aufrufen und Lauf Zeit Ausführung fungieren, einschließlich der [Debug-Ebene](d3d10-graphics-programming-guide-api-features-layers.md) und der Switch-to-Reference-Schicht. Explizites verknüpfen ist nicht erforderlich. Wenn ein Gerät mit dem entsprechenden ebenenflag erstellt wird, wird diese DLL automatisch geladen. Diese Komponente ist nur für Entwicklungs-und Debugzwecke gedacht. Nur als Teil des DirectX SDK für Windows SDK oder Legacy enthalten und kann nicht weiter verteilt werden. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmier Handbuch für Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> <dt>

[Direct3D 10-Grafiken](d3d10-graphics.md)
</dt> </dl>

 

 



