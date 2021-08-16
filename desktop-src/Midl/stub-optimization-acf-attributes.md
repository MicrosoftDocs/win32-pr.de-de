---
title: ACF-Attribute für die Stuboptimierung
description: Mit diesen Attributen können Sie die Größe und Geschwindigkeit Ihres Stubcodes optimieren.
ms.assetid: 8c98b9ff-d91c-4a17-90c9-298f588e46c5
keywords:
- ACF MIDL , Attribute, Stuboptimierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f8386eb6a6077a994b6f9800ff237a9966e97bff5eb0d6d865ea313634790f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118383192"
---
# <a name="stub-optimization-acf-attributes"></a>ACF-Attribute für die Stuboptimierung

Mit diesen Attributen können Sie die Größe und Geschwindigkeit Ihres Stubcodes optimieren.



| attribute                                    | Verbrauch                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**code**](code.md)[**nocode**](nocode.md) | Verwenden Sie die [**Attribute code**](code.md) und [**nocode**](nocode.md) zusammen, um das Generieren von Stubcode für nicht genutzte Funktionen zu vermeiden. Wenden Sie das **Nocode-Attribut** auf den Schnittstellenheader und das **Codeattribut** auf die Prozeduren an, die die Clientanwendung implementiert. Clientstubcode wird nur für die ausgewählten Prozeduren generiert.                                                                |
| [**Optimieren**](optimize.md)                 | Hiermit können Sie den Optimierungsgrad optimieren, den der MIDL-Compiler beim Generieren von Stubcode ausführt, indem Sie angeben, dass Die Daten entweder im gemischten Modus oder mit der interpretierten Methode gemarshallt werden sollen. Sie können das [**Optimize-Attribut**](optimize.md) auf eine Schnittstelle oder auf ausgewählte Funktionen innerhalb der Schnittstelle anwenden. In beiden Fällen überschreibt die Verwendung die Befehlszeilenoptimierungen und alle bereits vorhandenen Standardwerte. |



 

 

 




