---
title: Zeigertypattribute
description: Die folgenden Attribute geben die Merkmale von Zeigern an.
ms.assetid: 310d0dfe-eef3-447e-89fb-40f620976d00
keywords:
- IDL MIDL , Attribute, Zeigertyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cb8355a71428c957804596531ea428fb99a779478b677eaa2094cc4db323c45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013728"
---
# <a name="pointer-type-attributes"></a>Zeigertypattribute

Die folgenden Attribute geben die Merkmale von Zeigern an.



| attribute                                   | Verbrauch                                                                                                                                                                                                |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ptr**](ptr.md)                          | Bezeichnet einen Zeiger als vollständigen Zeiger mit allen Funktionen eines C-Sprachzeigers, einschließlich Aliasing.                                                                                       |
| [**ref**](ref.md)                          | Legt den einfachsten Zeigertyp in MIDL fest– einen Zeiger, der einfach die Adresse einiger Daten bereitstellt. Verweiszeiger dürfen nie NULL sein.                                                             |
| [**Einzigartige**](unique.md)                    | Lässt zu, dass ein Zeiger NULL ist, unterstützt jedoch kein Aliasing.                                                                                                                                               |
| [**\_Zeigerstandard**](pointer-default.md) | Wird auf eine Schnittstelle angewendet, um den Standardzeigertyp für alle Zeiger in dieser Schnittstelle anzugeben, mit Ausnahme von Parameterzeigern der obersten Ebene, die automatisch [**auf Verweiszeiger festgelegt**](ref.md) sind. |
| [**iid \_ ist**](iid-is.md)                   | Stellt den Schnittstellenbezeichner der COM-Schnittstelle bereit, die das Objekt des Zeigers ist.                                                                                                            |
| [**Schnur**](string.md)                    | Gibt an, dass der Zeiger auf eine Zeichenfolge zeigt.                                                                                                                                                       |



 

 

 




