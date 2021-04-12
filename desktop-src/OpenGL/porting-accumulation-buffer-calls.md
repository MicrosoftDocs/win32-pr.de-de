---
title: Portieren von Akkumulations Puffer aufrufen
description: Sie müssen ihren Akkumulations Puffer zuordnen, indem Sie das entsprechende Pixel Format mit der OpenGL-Funktion "-"
ms.assetid: 523728ce-4aae-4247-a3dc-23864231cad1
keywords:
- IRIS GL portieren, Akkumulations Puffer
- Portieren von IRIS GL, Akkumulations Puffer
- Portieren auf OpenGL von IRIS GL, Akkumulations Puffer
- OpenGL-Portierung von IRIS GL, Akkumulations Puffer
- Akkumulations Puffer OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ca91cb3ba35535ba2470297070dffc932a1c33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207411"
---
# <a name="porting-accumulation-buffer-calls"></a>Portieren von Akkumulations Puffer aufrufen

Sie müssen ihren Akkumulations Puffer zuordnen, indem Sie das entsprechende Pixel Format mit **der OpenGL-** [**Funktion "**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) -" In der folgenden Tabelle sind IRIS GL-Funktionen aufgelistet, die sich auf den Akkumulations Puffer und ihre entsprechenden OpenGL-Funktionen auswirken



| IRIS GL-Funktion       | OpenGL-Funktion                                       | Bedeutung                                                                       |
|------------------------|-------------------------------------------------------|-------------------------------------------------------------------------------|
| **acsize**             |  "" "" "" "  " "" "" "" ""       | Gibt die Anzahl der bitplane pro Farbkomponente im Akkumulations Puffer an. |
| **acbuf**              | [**glaccum**](glaccum.md)                            | Arbeitet auf dem Akkumulations Puffer.                                          |
|                        | [**glclearaccum**](glclearaccum.md)                  | Legt eindeutige Werte für den Akkumulations Puffer fest.                                    |
| **acbuf**(AC \_ Clear) | [**glClear**](glclear.md) (GL- \_ Accum- \_ Puffer \_ Bit) | Löscht den Akkumulations Puffer.                                               |



 

In der folgenden Tabelle werden die Iris GL- **acbuf** -Parameter zusammen mit den entsprechenden OpenGL- [**glaccum**](glaccum.md) -Parametern aufgelistet.



| IRIS GL-Parameter     | OpenGL-Parameter |
|-----------------------|------------------|
| \_Akkumulierung        | GL- \_ Accum        |
| Wechsel \_ Stromversorgung \_ | GL \_ Laden         |
| AC- \_ Rückgabe            | GL- \_ Rückgabe       |
| AC- \_ mult              | GL \_ .         |
| AC \_ Hinzufügen               | GL \_ Hinzufügen          |



 

 

 




