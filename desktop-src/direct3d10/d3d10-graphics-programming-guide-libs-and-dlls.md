---
description: Damit eine Anwendung ordnungsgemäß ausgeführt werden kann, müssen auf dem Hostcomputer die entsprechenden DLLs installiert sein. Diese DLLs können entweder vom Betriebssystem oder vom verteilbaren Anwendungspaket bereitgestellt werden.
ms.assetid: fa5405e9-116f-4b7f-8f8e-791a79942570
title: Verknüpfen statischer und dynamischer Bibliotheken (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b5c05599371521f81b488c5d3e10467a28a3c3241efd180edae15dfd40f279c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118101483"
---
# <a name="linking-static-and-dynamic-libraries-direct3d-10"></a>Verknüpfen statischer und dynamischer Bibliotheken (Direct3D 10)

Damit eine Anwendung ordnungsgemäß ausgeführt werden kann, müssen auf dem Hostcomputer die entsprechenden DLLs installiert sein. Diese DLLs können entweder vom Betriebssystem oder vom verteilbaren Anwendungspaket bereitgestellt werden.

## <a name="libraries-load-appropriate-dlls"></a>Bibliotheken laden entsprechende DLLs

Die im DirectX SDK enthaltenen Bibliotheken laden zur Laufzeit automatisch die richtigen DLLs. Die Ausnahme von dieser Regel ist d3dx10.lib/d3dx10d.lib, die die d3dx10.dll lädt, die mit dieser SDK-Version ausgeliefert wurde. Wenn das heruntergeladene SDK z. B. d3dx10 \_33.dll und d3dx10 \_34.dll enthält, lädt die Bibliothek (d3dx10.lib), die mit diesem SDK ausgeliefert wird, d3dx10 \_34.dll. Wenn später ein nachfolgendes SDK installiert wird, das d3dx10 \_ 35.lib enthält, lädt d3dx10.lib aus dem vorherigen SDK weiterhin d3dx10 \_34.dll. Die Datei d3dx10.lib aus dem neueren SDK lädt d3dx10 \_35.dll.

## <a name="redistributing-binaries"></a>Verteilen von Binärdateien

Nur d3dx10.dll (und nachfolgende Versionen derselben Datei) können neu verteilt werden. Um diese Datei neu zu verteilen, müssen Sie die **DirectXSetup-Funktion** verwenden. Ausführliche Informationen zur Verwendung dieser Funktion und zum Zusammenstellen eines verteilbaren Pakets finden Sie unter [Installieren von DirectX mit DirectSetup.](https://msdn.microsoft.com/library/Ee418267(v=VS.85).aspx) Alle anderen erforderlichen Binärdateien sind in Windows Vista enthalten. Die einzigen Binärdateien, die neu verteilt werden können, sind diejenigen, die sich im folgenden Verzeichnis befinden.


```
(SDK root)\Redist
```



In der folgenden Tabelle werden die Binärdateien beschrieben, die Entwickler beachten sollten.



| Direct3D 10-Binärdateien   | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| d3dx10.dll/d3dx10d.dll | Einzelhandels- und Debuggen von D3DX10-Komponenten Die Einzelhandelskomponenten können im REDIST CAB neu verteilt werden.                                                                                                                                                                                                                                                                                                                                                                                                             |
| d3d10ref.dll           | Referenzrasterizer. Stellt die Softwareimplementierungen der Grafikpipeline bereit. Nur als Teil des Windows SDK oder des älteren DirectX SDK enthalten und kann nicht neu verteilt werden. Der Verweisrasterizer ist nur für das Debuggen vorgesehen. Eine explizite Verknüpfung ist nicht erforderlich. Beim Versuch, ein Referenzgerät zu erstellen (siehe [**D3D10CreateDevice),**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice)wird diese DLL geladen, wenn sie vorhanden ist.                                                                                                    |
| d3d10sdklayers.dll     | Eine Reihe von SDK-Hilfsprogrammen, die als Ebene zwischen API-Aufrufen und Laufzeitausführung fungieren, einschließlich der [Debugebene](d3d10-graphics-programming-guide-api-features-layers.md) und der Switch-to-Reference-Ebene. Eine explizite Verknüpfung ist nicht erforderlich. Wenn ein Gerät mit dem entsprechenden Ebenenflag erstellt wird, wird diese DLL automatisch geladen. Diese Komponente ist nur für Entwicklungs- und Debugzwecke vorgesehen. Nur als Teil des Windows SDK oder des älteren DirectX SDK enthalten und kann nicht neu verteilt werden. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmierhandbuch für Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> <dt>

[Direct3D 10-Grafiken](d3d10-graphics.md)
</dt> </dl>

 

 



