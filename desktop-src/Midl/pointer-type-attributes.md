---
title: Zeiger-Typattribute
description: Die folgenden Attribute geben die Merkmale von Zeigern an.
ms.assetid: 310d0dfe-eef3-447e-89fb-40f620976d00
keywords:
- IDL-Mittell, Attribute, Zeigertyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71371fff80d541242fcdc41d6c8adcc93dcdb754
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714357"
---
# <a name="pointer-type-attributes"></a>Zeiger-Typattribute

Die folgenden Attribute geben die Merkmale von Zeigern an.



| Attribut                                   | Verbrauch                                                                                                                                                                                                |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ptr**](ptr.md)                          | Legt einen Zeiger als vollständigen Zeiger fest, der alle Funktionen eines C-sprach Zeigers enthält, einschließlich Aliasing.                                                                                       |
| [**ref**](ref.md)                          | Legt den einfachsten Zeigertyp in der mittleren l fest – einen, der einfach die Adresse einiger Daten bereitstellt. Verweis Zeiger können niemals NULL sein.                                                             |
| [**gem**](unique.md)                    | Ermöglicht, dass ein Zeiger NULL ist, aber keine Aliasing unterstützt.                                                                                                                                               |
| [**Zeiger \_ Standard**](pointer-default.md) | Wird auf eine Schnittstelle angewendet, um den Standard Zeigertyp für alle Zeiger in dieser Schnittstelle anzugeben, außer für Parameter Zeiger der obersten Ebene, die [**automatisch auf Verweis**](ref.md) Zeiger festgelegt werden. |
| [**IID \_ ist**](iid-is.md)                   | Stellt den Schnittstellen Bezeichner der COM-Schnittstelle bereit, die das-Objekt des Zeigers ist.                                                                                                            |
| [**Zeichenfolge**](string.md)                    | Gibt an, dass der Zeiger auf eine Zeichenfolge zeigt.                                                                                                                                                       |



 

 

 




