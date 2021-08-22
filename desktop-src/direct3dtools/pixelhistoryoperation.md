---
description: Stellt Informationen zum Pixelverlauf dar.
MS-HAID: vspixengine.PixelHistoryOperation
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PixelHistoryOperation-Struktur
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
ms.openlocfilehash: 15cae4986b7dc109c08011d2cc23e1b6133de9e5
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625186"
---
# <a name="span-idvspixenginepixelhistoryoperationspanpixelhistoryoperation-structure"></a><span id="vspixengine.pixelhistoryoperation"></span>PixelHistoryOperation-Struktur

Stellt Informationen zum Pixelverlauf dar.

## <a name="syntax"></a>Syntax


```C++
} PixelHistoryOperation;
```

## <a name="members"></a>Member

**eid**  
Die ID des Grafikereignis, das diesem Vorgang zugeordnet ist.

**PCP**  
Gepackte Aufrufe, die diesem Vorgang zugeordnet sind.

**renderTargetPtr**  
Das Renderziel, das ursprünglich (innerhalb der erfassten Anwendung) diesem Vorgang zugeordnet wurde.

**iPrim**  
Der Index des tatsächlichen Primitiven, der seiner Operation zugeordnet ist.

**numPrims**  
Die Gesamtzahl der primitiven Typen, die diesem Vorgang zugeordnet sind.

**numVertsPerPrim**  
Die Anzahl der Scheitelzeichen pro Primitiv.

**iInstance**  
Beim Rendern von -Instanzen die Instanznummer der tatsächlichen Instanz, die diesem Vorgang zugeordnet ist.

**iInstanceCount**  
Beim Rendern von -Instanzen die Gesamtzahl der Instanzen, die diesem Vorgang zugeordnet sind.

**bAssemblerStageGenerratesInstanceID**  
TRUE, wenn der Eingabe-Assembler Instanz-IDs generiert; andernfalls FALSE.

**flags**  
Eine Kombination aus PIXELHISTORYFLAGS-Werten. Weitere Informationen finden Sie unter der PIXELHISTORYFLAGS-Enumeration.

**pVSFile**  
Eine FILEPTR für den Bytestream des Pixels shader. Dies wird zum Debuggen zurück übergeben.

**pGSFile**  
Eine FILEPTR für den Bytestream des Geometrie-Shaders. Dies wird zum Debuggen zurück übergeben.

**pPSFile**  
Eine FILEPTR für den Bytestream des Pixels shader. Dies wird zum Debuggen zurück übergeben.

**pHSFile**  
Eine FILEPTR für den Hüllen-Shader-Bytestream. Dies wird zum Debuggen zurück übergeben.

**pDSFile**  
Eine FILEPTR für den Domänen-Shader-Bytestream. Dies wird zum Debuggen zurück übergeben.

**pCSFile**  
Eine FILEPTR für den Compute-Shader-Bytestream. Dies wird zum Debuggen zurück übergeben.

**VertexShaderFile**  
Eine COM-Zeichenfolge, die den Dateipfad der Vertex-Shader-Quelldatei enthält.

**PixelShaderFile**  
Eine COM-Zeichenfolge, die den Dateipfad der Pixel-Shader-Quelldatei enthält.

**GeometryShaderFile**  
Eine COM-Zeichenfolge, die den Dateipfad der Quelldatei des Geometrie-Shaders enthält.

**HullShaderFile**  
Eine COM-Zeichenfolge, die den Dateipfad der Quelldatei des Hüllen-Shaders enthält.

**DomainShaderFile**  
Eine COM-Zeichenfolge, die den Dateipfad der Domänen-Shader-Quelldatei enthält.

**psRed**  
Pixel-Shaderausgabe: Der Wert der Komponente roter Farbe.

**psGreen**  
Pixel-Shaderausgabe: Wert der Komponente für grüne Farbe.

**psBlue**  
Pixel-Shaderausgabe: Wert der Blaufarbkomponente

**psAlpha**  
Pixel-Shaderausgabe: Wert der Alphafarbkomponente

**LabelPSRed**  
Eine COM-Zeichenfolge, die den Namen der Bezeichnung enthält, die der roten Farbkomponente der Pixel-Shaderausgabe zugeordnet ist.

**LabelPSGreen**  
Eine COM-Zeichenfolge, die den Namen der Bezeichnung enthält, die der grünen Farbkomponente der Pixel-Shaderausgabe zugeordnet ist.

**LabelPSBlue**  
Eine COM-Zeichenfolge, die den Namen der Bezeichnung enthält, die der Blaufarbkomponente der Pixel-Shaderausgabe zugeordnet ist.

**LabelPSAlpha**  
Eine COM-Zeichenfolge, die den Namen der Bezeichnung enthält, die der Alphafarbkomponente der Pixel-Shaderausgabe zugeordnet ist.

**pixelKillReason**  
Pixel-Shaderausgabe: Grund für den Abbruch der Pixelausgabe.

**pixelOccluded**  
TRUE, wenn das Pixel okcluded ist; andernfalls FALSE.

**fbRed**  
Framebuffer: Der Wert der roten Farbkomponente von framebuffer, bevor die Pixel-Shaderausgabe zusammengeführt wird.

**fbGreen**  
Framebuffer: Der Wert der grünen Farbkomponente von framebuffer, bevor die Pixel-Shaderausgabe zusammengeführt wird.

**fbBlue**  
Framebuffer: Der Wert der Blaufarbkomponente von framebuffer, bevor die Pixel-Shaderausgabe zusammengeführt wird.

**fbAlpha**  
Framebuffer: Der Wert der Alphafarbkomponente von framebuffer, bevor die Pixel-Shaderausgabe zusammengeführt wird.

**LabelFBRed**  
Eine COM-Zeichenfolge, die den Namen der Bezeichnung enthält, die der roten Farbkomponente des Framepuffers zugeordnet ist.

**LabelFBGreen**  
Eine COM-Zeichenfolge, die den Namen der Bezeichnung enthält, die der grünen Farbkomponente des Framepuffers zugeordnet ist.

**LabelFBBlue**  
Eine COM-Zeichenfolge, die den Namen der Bezeichnung enthält, die der Blaufarbkomponente des Framepuffers zugeordnet ist.

**LabelFBAlpha**  
Eine COM-Zeichenfolge, die den Namen der Bezeichnung enthält, die der Alphafarbkomponente des Framepuffers zugeordnet ist.

**Topologie**  
Die Vertextopologie der Zeichnen-Aufrufe (Dreiecksliste, Dreiecksstreifen usw.).

**Scheitelpunkte**  
Eine COM-Zeichenfolge, die den Scheitelpunktpuffer enthält, der bei diesem Primitiven beginnt. Der Scheitelpunktpuffer folgt dem in der Pipelinephase angegebenen Eingabelayoutformat.

**vertexSize**  
Die Größe eines einzelnen Scheitelpunkts in Bytes.

**InputLayout**  
Eine COM-Zeichenfolge, die eine Sequenz von InputLayoutStruct-Strukturen enthält, die dem Zeichnen-Aufruf zugeordnet sind.

**Hresult**  
Das DirectX Hresult. Im Falle eines Problems kann dies verwendet werden, um den Fehler anzuzeigen.

## <a name="requirements"></a>Requirements (Anforderungen)

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



