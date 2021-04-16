---
description: Die Leistung von Scheitelpunkt Verarbeitungsvorgängen, einschließlich Transformation und Beleuchtung, hängt stark davon ab, wo der Vertex-Puffer im Arbeitsspeicher vorhanden ist und welche Art von renderinggerät verwendet wird.
ms.assetid: 4f9ca83d-c9d6-4749-944d-78f831b0f44e
title: Gerätetypen und Vertex-Verarbeitungsanforderungen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 590cf2f5423d9c3bdf3e19c91f30b3e8c0586687
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521443"
---
# <a name="device-types-and-vertex-processing-requirements-direct3d-9"></a>Gerätetypen und Vertex-Verarbeitungsanforderungen (Direct3D 9)

Die Leistung von Scheitelpunkt Verarbeitungsvorgängen, einschließlich Transformation und Beleuchtung, hängt stark davon ab, wo der Vertex-Puffer im Arbeitsspeicher vorhanden ist und welche Art von renderinggerät verwendet wird. Anwendungen steuern die Speicher Belegung für Vertex-Puffer, wenn Sie erstellt werden. Wenn das D3DPOOL \_ SystemMem-Speicherflag festgelegt ist, wird der Vertex-Puffer im Systemspeicher erstellt. Wenn das D3DPOOL- \_ standardarbeitsspeicherflag verwendet wird, bestimmt der Gerätetreiber, wo der Speicher für den Vertex-Puffer am besten zugewiesen wird. Dies wird häufig als Treiber optimaler Arbeitsspeicher bezeichnet. Treiber-optimaler Arbeitsspeicher kann lokaler Videospeicher, nicht lokaler Videospeicher oder System Arbeitsspeicher sein.

Durch das Festlegen der D3DUSAGE \_ softwareprocessing-Konstante mit [**IDirect3DDevice9:: featevertexbuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) wird die Verarbeitung von Software Scheitel Punkten in den Vertex-Puffer Daten ermöglicht. Dieses Flag ist für die Verarbeitung von Software Scheitel Punkten im gemischten Modus erforderlich. Das Flag darf nicht für den Hardware-Scheitelpunkt Verarbeitungsmodus verwendet werden. Vertex-Puffer, die bei der Verarbeitung von Software Vertex verwendet werden, umfassen Folgendes:

-   Alle Eingabedaten Ströme für [**IDirect3DDevice9::P rocess Vertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices).
-   Alle Eingabedaten Ströme für [**IDirect3DDevice9::D rawprimitiv**](/windows/desktop/api) und [**IDirect3DDevice9::D rawindexedprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive).

Die Argumentation, die Sie verwenden, um den Speicherort des Systems oder des Treibers optimal zu ermitteln, ist für Scheitelpunkt Puffer identisch mit der für Texturen. Die Vertex-Verarbeitung, einschließlich Transformation und Beleuchtung, in Hardware funktioniert am besten, wenn die Vertex-Puffer im Treiber optimalen Arbeitsspeicher zugeordnet werden, während die Verarbeitung von Software Scheitel Punkten am besten mit Vertex-Puffern im Systemspeicher funktioniert. Für Texturen funktioniert die Hardware-rasterisierung am besten, wenn Texturen im Treiber optimalen Arbeitsspeicher zugeordnet werden, während die Software rasterisierung am besten mit System-Memory-Texturen funktioniert.

Microsoft Direct3D 9 unterstützt die eigenständige Verarbeitung von Vertices, ohne dass primitive mit der [**IDirect3DDevice9::P rocess Vertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) -Methode gerendert werden. Diese eigenständige Scheitelpunkt Verarbeitung erfolgt immer in Software auf dem Host Prozessor. Aus diesem Grund müssen Vertex-Puffer, die als Quellen verwendet werden, die mit [**IDirect3DDevice9:: SetStreamSource**](/windows/desktop/api) verwendet werden, mit dem D3DUSAGE \_ softwareprocessing-Flag erstellt werden. Die von **IDirect3DDevice9::P rocessvertices** bereitgestellten Funktionen sind identisch mit denen der [**IDirect3DDevice9::D rawprimiprimitiv**](/windows/desktop/api) -und [**IDirect3DDevice9::D rawindexedprimitionsmethoden**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) bei der Verarbeitung von Software Scheitel Punkten.

Wenn Ihre Anwendung ihre eigene Scheitelpunkt Verarbeitung ausführt und transformierte, beleuchtete und abgeschnittene Scheitel Punkte an Renderingmethoden übergibt, kann die Anwendung Scheitel Punkte direkt in einen Vertex-Puffer schreiben, der im Treiber optimalen Arbeitsspeicher zugeordnet ist. Dieses Verfahren verhindert einen redundanten Kopiervorgang zu einem späteren Zeitpunkt. Beachten Sie, dass diese Technik nicht gut funktioniert, wenn Ihre Anwendung Daten aus einem Vertex-Puffer zurück liest, da Lesevorgänge, die vom Host aus dem Treiber optimalen Arbeitsspeicher durchgeführt werden, sehr langsam sein können. Wenn Ihre Anwendung während der Verarbeitung lesen oder Daten in den Puffer schreiben muss, ist ein System-Memory-Vertex-Puffer eine bessere Wahl.

Bei Verwendung der Direct3D Vertex-Verarbeitungsfunktionen (durch Übergeben von nicht transformierten Scheitel Punkten an Scheitelpunkt-Puffer-Renderingmethoden) kann die Verarbeitung abhängig vom Gerätetyp und den geräteerstellungsflags in Hardware oder Software erfolgen. Es wird empfohlen, Vertex-Puffer im Pool zu zuordnen D3DPOOL \_ standardmäßig für die optimale Leistung in nahezu allen Fällen. Wenn ein Gerät die Verarbeitung von Hardware Scheitel Punkten verwendet, gibt es eine Reihe zusätzlicher Optimierungen, die basierend auf den Flags D3DUSAGE \_ Dynamic und D3DUSAGE Write ausgeführt werden können \_ . Weitere Informationen zur Verwendung dieser Flags finden Sie unter IDirect3DDevice9:: featevertexbuffer.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Puffer](vertex-buffers.md)
</dt> </dl>

 

 
