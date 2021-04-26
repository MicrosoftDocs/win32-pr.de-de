---
description: 'Texturargumentkonst constants werden als Werte für die folgenden Member des aufzählten D3DTEXTURESTAGESTATETYPE-Typs verwendet:'
ms.assetid: 36b2b715-5ced-4246-840e-8ea343521ef4
title: D3DTA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 898e1bb66f74a1087a9da186599469bb195734ce
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995287"
---
# <a name="d3dta"></a>D3DTA

Texturargumentkonst constants werden als Werte für die folgenden Member des [**aufzählten D3DTEXTURESTAGESTATETYPE-Typs**](./d3dtexturestagestatetype.md) verwendet:

-   D3DTSS \_ ALPHAARG0
-   D3DTSS \_ ALPHAARG1
-   D3DTSS \_ ALPHAARG2
-   D3DTSS \_ COLORARG0
-   D3DTSS \_ COLORARG1
-   D3DTSS \_ COLORARG2
-   D3DTSS \_ RESULTARG

Legen Sie Texturargumente fest, und rufen Sie sie ab, indem Sie die [**Methoden SetTextureStageState**](/windows/desktop/api) und [**GetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate) aufrufen.

Argumentflags

Sie können ein Argumentflag mit einem Modifizierer kombinieren, aber zwei Argumentflags können nicht kombiniert werden.



| \#Definieren          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DTA-KONSTANTE \_   | Wählen Sie eine Konstante aus einer Texturphase aus. Der Standardwert ist 0xffffffff.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| D3DTA \_ CURRENT    | Das Texturargument ist das Ergebnis der vorherigen Mischungsphase. In der ersten Texturphase (Phase 0) entspricht dieses Argument D3DTA \_ DIFFUSE. Wenn in der vorherigen Mischungsphase eine Bumpmaptextur verwendet wird (D3DTOP \_ BUMPENVMAP-Vorgang), wählt das System die Textur aus der Stufe vor der Bumpmaptextur aus. Wenn s die aktuelle Texturphase darstellt und s - 1 eine Bumpmaptextur enthält, wird dieses Argument zur Ergebnisausgabe von textur stage s - 2. Berechtigungen sind Lese-/Schreibzugriff. |
| D3DTA \_ DIFFUSE    | Das Texturargument ist die diffuse Farbe, die während der Gouraud-Schattierung von Scheitelpunktkomponenten interpoliert wird. Wenn der Scheitelpunkt keine diffuse Farbe enthält, wird die Standardfarbe 0xffffffff. Berechtigungen sind schreibgeschützt.                                                                                                                                                                                                                                                                                          |
| D3DTA \_ SELECTMASK | Maskierungswert für alle Argumente; wird beim Festlegen von Texturargumenten nicht verwendet.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| D3DTA \_ SPECULAR   | Das Texturargument ist die Glanzfarbe, die während der Gouraud-Schattierung von Scheitelpunktkomponenten interpoliert wird. Wenn der Scheitelpunkt keine Glanzfarbe enthält, wird die Standardfarbe 0xffffffff. Berechtigungen sind schreibgeschützt.                                                                                                                                                                                                                                                                                        |
| D3DTA \_ TEMP       | Das Texturargument ist eine temporäre Registerfarbe für Lese- oder Schreibzugriff. D3DTA \_ TEMP wird unterstützt, wenn die [D3DPMISCCAPS \_ TSSARGTEMP-Gerätefunktion](d3dpmisccaps.md) vorhanden ist. Der Standardwert für das Register ist (0,0, 0,0, 0,0, 0,0). Berechtigungen sind Lese-/Schreibzugriff.                                                                                                                                                                                                                                   |
| D3DTA \_ TEXTURE    | Das Texturargument ist die Texturfarbe für diese Texturphase. Berechtigungen sind schreibgeschützt.                                                                                                                                                                                                                                                                                                                                                                                                               |
| \_D3DTA-TFACTOR    | Das Texturargument ist der Texturfaktor, der in einem vorherigen Aufruf von [**SetRenderState**](/windows/desktop/api) mit dem [**D3DRS \_ TEXTUREFACTOR-Renderzustandswert**](./d3drenderstatetype.md) festgelegt wurde. Berechtigungen sind schreibgeschützt.                                                                                                                                                                                                                                                       |



 

Modifiziererflags

Ein Argumentflag kann mit einem der folgenden Modifiziererflags kombiniert werden.



| \#Definieren              | BESCHREIBUNG                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------|
| D3DTA \_ ALPHAREPLICATE | Replizieren Sie die Alphainformationen in alle Farbkanäle, bevor der Vorgang abgeschlossen wird. Dies ist ein Lesemodifizierer. |
| \_D3DTA-KOMPLEMENT     | Nehmen Sie das Komplement des Arguments x, (1.0 - x). Dies ist ein Lesemodifizierer.                                     |



 

## <a name="constant-information"></a>Konstante Informationen



|                          |             |
|--------------------------|-------------|
| Header                   | d3d9types.h |
| Mindestbetriebssystem | Windows 98  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
