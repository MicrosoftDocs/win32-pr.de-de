---
description: 'Textur Argument Konstanten werden als Werte für die folgenden Member des D3DTEXTURESTAGESTATETYPE-enumerierten Typs verwendet:'
ms.assetid: 36b2b715-5ced-4246-840e-8ea343521ef4
title: D3DTA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf58d4d5665b1a098b84eaa95294e69220d6ea4b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106341153"
---
# <a name="d3dta"></a>D3DTA

Textur Argument Konstanten werden als Werte für die folgenden Member des [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) -enumerierten Typs verwendet:

-   D3DTSS \_ ALPHAARG0
-   D3DTSS \_ ALPHAARG1
-   D3DTSS \_ ALPHAARG2
-   D3DTSS \_ COLORARG0
-   D3DTSS \_ COLORARG1
-   D3DTSS \_ COLORARG2
-   D3DTSS \_ resultarg

Sie sollten Textur Argumente festlegen und abrufen, indem Sie die Methoden [**settexturestagestate**](/windows/desktop/api) und [**gettexturestagestate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate) aufrufen.

Argumentflags

Sie können ein Argumentflag mit einem Modifizierer kombinieren, aber zwei Argumentflags können nicht kombiniert werden.



|                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \#definieren          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| D3DTA- \_ Konstante   | Wählen Sie eine Konstante aus einer Textur Phase aus. Der Standardwert ist 0xFFFFFFFF.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| D3DTA \_ aktuell    | Das Textur Argument ist das Ergebnis der vorherigen Mischungs Phase. In der ersten Textur Phase (Phase 0) entspricht dieses Argument D3DTA \_ diffdiff. Wenn in der vorherigen Mischungs Stufe eine Bump-Map-Textur (der D3DTOP \_ bumpenvmap-Vorgang) verwendet wird, wählt das System die Textur aus der Phase vor der Bild-und Bildtextur Struktur aus. Wenn s die aktuelle Textur Phase darstellt und s-1 eine Bump-Map-Textur enthält, wird dieses Argument zur Ergebnis Ausgabe der Textur Phase s-2. Berechtigungen sind Lese-/Schreibzugriff. |
| D3DTA \_ diffuses    | Das Textur Argument ist die diffuse Farbe, die von Scheitelpunkt Komponenten während der Schattierung von Gouraud interpoliert wird. Wenn der Scheitelpunkt keine diffuse Farbe enthält, ist die Standardfarbe 0xFFFFFFFF. Berechtigungen sind schreibgeschützt.                                                                                                                                                                                                                                                                                          |
| D3DTA \_ selectmask | Maskenwert für alle Argumente; wird beim Festlegen von Textur Argumenten nicht verwendet.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| D3DTA \_ Glanz   | Das Textur Argument ist die Glanz Farbe, die von Scheitelpunkt Komponenten während der Schattierung von Gouraud interpoliert wird. Wenn der Scheitelpunkt keine Glanz Farbe enthält, ist die Standardfarbe 0xFFFFFFFF. Berechtigungen sind schreibgeschützt.                                                                                                                                                                                                                                                                                        |
| D3DTA \_ Temp       | Das Textur Argument ist eine temporäre Register Farbe für Lese-oder Schreibvorgänge. D3DTA \_ Temp wird unterstützt, wenn die [D3DPMISCCAPS \_ tssargtemp](d3dpmisccaps.md) -Geräte Funktion vorhanden ist. Der Standardwert für das Register ist (0,0, 0,0, 0,0, 0,0). Berechtigungen sind Lese-/Schreibzugriff.                                                                                                                                                                                                                                   |
| D3DTA- \_ Textur    | Das Textur Argument ist die Textur Farbe für diese Textur Phase. Berechtigungen sind schreibgeschützt.                                                                                                                                                                                                                                                                                                                                                                                                               |
| D3DTA \_ Tfactor    | Das Textur Argument ist der Textur Faktor, der in einem vorherigen Aufrufen von [**setrenderstate**](/windows/desktop/api) mit dem Wert des [**D3DRS \_ TextureFactor**](./d3drenderstatetype.md) -renderzustands festgelegt wurde. Berechtigungen sind schreibgeschützt.                                                                                                                                                                                                                                                       |



 

Modifiziererflags

Ein Argumentflag kann mit einem der folgenden Modifiziererflags kombiniert werden.



|                       |                                                                                                                |
|-----------------------|----------------------------------------------------------------------------------------------------------------|
| \#definieren              | BESCHREIBUNG                                                                                                    |
| D3DTA \_ alphareplicate | Replizieren Sie die Alpha Informationen in alle farbchannels, bevor der Vorgang abgeschlossen ist. Dies ist ein Read-Modifizierer. |
| D3DTA- \_ Ergänzung     | Nehmen Sie das Komplement des Arguments x, (1,0-x) vor. Dies ist ein Read-Modifizierer.                                     |



 

## <a name="constant-information"></a>Konstante Informationen



|                          |             |
|--------------------------|-------------|
| Header                   | d3d9types. h |
| Mindestens Betriebssystem | Windows 98  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
