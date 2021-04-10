---
title: ACF-Attribute der Stub-Optimierung
description: Diese Attribute ermöglichen es Ihnen, die Größe und Geschwindigkeit Ihres stubcodes zu optimieren.
ms.assetid: 8c98b9ff-d91c-4a17-90c9-298f588e46c5
keywords:
- ACF-Mittell, Attribute, Stub-Optimierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209490d6064d134a51492afee39c501059879bab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855883"
---
# <a name="stub-optimization-acf-attributes"></a>ACF-Attribute der Stub-Optimierung

Diese Attribute ermöglichen es Ihnen, die Größe und Geschwindigkeit Ihres stubcodes zu optimieren.



| Attribut                                    | Verbrauch                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [](code.md)[**codenocode**](nocode.md) | Verwenden Sie die Attribute [**Code**](code.md) und [**NoCode**](nocode.md) , um zu vermeiden, dass Stub-Code für nicht verwendete Funktionen erzeugt wird. Wenden Sie das **NoCode** -Attribut auf den Schnittstellen Header an, und wenden Sie das **Code** Attribut auf die Prozeduren an, die von der Client Anwendung implementiert werden. Client-Stub-Code wird nur für die ausgewählten Prozeduren generiert.                                                                |
| [**optimiert**](optimize.md)                 | Mit können Sie den Optimierungsgrad optimieren, den der-Mittell-Compiler beim Erzeugen von Stub-Code ausführt, indem Sie angeben, dass die Daten entweder von der gemischten oder interpretierten Methode gemarshallt werden sollen. Sie können das [**Optimierungs**](optimize.md) Attribut auf eine Schnittstelle oder auf ausgewählte Funktionen innerhalb der Schnittstelle anwenden. In beiden Fällen werden die Befehlszeilen Optimierungen und alle bereits vorhandenen Standardeinstellungen von der Verwendung überschrieben. |



 

 

 




