---
description: Stellt Informationen über den Pixel Verlauf dar.
MS-HAID: vspixengine.PixelHistoryOperation
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Pixelhistoryoperation-Struktur
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 59DC72FC-3865-48D3-9F92-9BE93DCA093B
api_name:
- PixelHistoryOperation
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c02a6725f588aaa4c7d72c48d03d921503d4e6a6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346402"
---
# <a name="span-idvspixenginepixelhistoryoperationspanpixelhistoryoperation-structure"></a><span id="vspixengine.pixelhistoryoperation"></span>Pixelhistoryoperation-Struktur

Stellt Informationen über den Pixel Verlauf dar.

## <a name="syntax"></a>Syntax


```C++
} PixelHistoryOperation;
```

## <a name="members"></a>Member

**VEI**  
Die ID des Grafik Ereignisses, das diesem Vorgang zugeordnet ist.

**PCP**  
Diesem Vorgang zugeordnete gepackte Aufrufe.

**rendertargetptr**  
Das Renderziel, das ursprünglich (innerhalb der erfassten Anwendung) mit diesem Vorgang zugeordnet wurde.

**iprim**  
Der Index des eigentlichen primitiven, dem der Vorgang zugeordnet ist.

**numprims**  
Die Gesamtanzahl der diesem Vorgang zugeordneten primitiver.

**numvertsperprim**  
Die Anzahl der Vertices pro primitiver.

**iinstance**  
Beim Rendern von Instanzen die Instanznummer der eigentlichen Instanz, die diesem Vorgang zugeordnet ist.

**iinstancecount**  
Beim Rendern von Instanzen die Gesamtzahl der diesem Vorgang zugeordneten Instanzen.

**bassemblerstagegeneratesinstanceid**  
true, wenn der Eingabe Assembler Instanz-IDs generiert. andernfalls false.

**flags**  
Eine Kombination von pixelhistoryflags-Werten. Weitere Informationen finden Sie unter der pixelhistoryflags-Enumeration.

**pvsfile**  
Ein "fleptr" für den Pixel-Shader-Bytestream. Dies wird zurückgegeben, um zu debuggen.

**pgsfile**  
Ein "fleptr" für den Geometry-Shader-Bytestream. Dies wird zurückgegeben, um zu debuggen.

**ppsfile**  
Ein "fleptr" für den Pixel-Shader-Bytestream. Dies wird zurückgegeben, um zu debuggen.

**phsfile**  
Ein "fleptr" für den Hull-Shader-Bytestream. Dies wird zurückgegeben, um zu debuggen.

**pdsfile**  
Ein "fleptr" für den Domänen-Shader-Bytestream. Dies wird zurückgegeben, um zu debuggen.

**pcsfile**  
Ein "fleptr" für den Compute-Shader-Bytestream. Dies wird zurückgegeben, um zu debuggen.

**Vertexshaderfile**  
Eine com-Zeichenfolge, die den filePath der Vertex-Shader-Quelldatei enthält.

**Pixelshaderfile**  
Eine com-Zeichenfolge, die den filePath der Pixelshader-Quelldatei enthält.

**Geometryshaderfile**  
Eine com-Zeichenfolge, die den filePath der Geometry-Shader-Quelldatei enthält.

**Hullshaderfile**  
Eine com-Zeichenfolge, die den filePath der Hull-Shader-Quelldatei enthält.

**Domainshaderfile**  
Eine com-Zeichenfolge, die den filePath der Domänen-Shader-Quelldatei enthält.

**psred**  
Pixel-Shader-Ausgabe: Wert der roten Farbkomponente.

**psgrün**  
Pixel-Shader-Ausgabe: Wert der grünen Farbkomponente.

**psblue**  
Pixel-Shader-Ausgabe: Wert der blauen Farbkomponente

**psalpha**  
Pixel-Shader-Ausgabe: Wert der Alpha Farbkomponente

**Labelpsred**  
Eine com-Zeichenfolge mit dem Namen der Bezeichnung, die der Komponente der roten Farbe der Pixel-Shader-Ausgabe zugeordnet ist.

**Labelpsgreen**  
Eine com-Zeichenfolge mit dem Namen der Bezeichnung, die der grünen Farbkomponente der Pixel-Shader-Ausgabe zugeordnet ist.

**Labelpsblue**  
Eine com-Zeichenfolge mit dem Namen der Bezeichnung, die der blauen Farbkomponente der Pixel-Shader-Ausgabe zugeordnet ist.

**Labelpsalpha**  
Eine com-Zeichenfolge mit dem Namen der Bezeichnung, die der Alpha Farbkomponente der Pixel-Shader-Ausgabe zugeordnet ist.

**pixelkillreason**  
Pixel-Shader-Ausgabe: Grund, warum die Pixel Ausgabe abgebrochen wurde.

**Pixel-okkluded**  
true, wenn das Pixel ausgeblendet ist. andernfalls false.

**mit dem Namen**  
Frame Puffer: Wert der roten Farbkomponente von Frame Puffer, bevor die Pixel-Shader-Ausgabe zusammengeführt wird.

**bgrün**  
Frame Puffer: Wert der grünen Farbkomponente von Frame Puffer, bevor die Pixel-Shader-Ausgabe zusammengeführt wird.

**"f"**  
Frame Puffer: Wert der blauen Farbkomponente von Frame Puffer, bevor die Pixel-Shader-Ausgabe zusammengeführt wird.

**"f"**  
Frame Puffer: Wert der Alpha Farbkomponente von Frame Puffer, bevor die Pixel-Shader-Ausgabe zusammengeführt wird.

**Labelfgezüchtet**  
Eine com-Zeichenfolge mit dem Namen der Bezeichnung, die der roten Farbkomponente des Framebuffer zugeordnet ist.

**Labelfbgrün**  
Eine com-Zeichenfolge mit dem Namen der Bezeichnung, die der grünen Farbkomponente des Framebuffer zugeordnet ist.

**Labelfbblue**  
Eine com-Zeichenfolge mit dem Namen der Bezeichnung, die der blauen Farbkomponente des Framebuffer zugeordnet ist.

**Labelfbalpha**  
Eine com-Zeichenfolge mit dem Namen der Bezeichnung, die der Alpha Farbkomponente des Framebuffer zugeordnet ist.

**Topologie**  
Die Vertex-Topologie der Draw-Aufrufe (Dreiecks Liste, Dreiecks Streifen usw.).

**Vertices**  
Eine com-Zeichenfolge, die den Scheitelpunkt Puffer enthält, beginnend bei diesem primitiven. Der Vertex-Puffer folgt dem Eingabe Layout-Format, das in der Pipeline Stufe angegeben wurde.

**vertexsize**  
Die Größe eines einzelnen Scheitel Punkts in Bytes.

**Input Layout**  
Eine com-Zeichenfolge, die eine Sequenz von inputlayoutstruct-Strukturen enthält, die dem Draw-Befehl zugeordnet sind.

**HRESULT**  
Das DirectX HRESULT. Im Fall eines Problems kann dies zum Anzeigen des Fehlers verwendet werden.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



