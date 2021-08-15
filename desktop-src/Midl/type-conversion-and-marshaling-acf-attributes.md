---
title: Type-Conversion und Marshalling von ACF-Attributen
description: Verwenden Sie diese Attribute, um zu steuern, wie Ihre Daten über das Netzwerk übertragen werden.
ms.assetid: 6af635f6-eeee-4fa6-85db-5d60434a1235
keywords:
- ACF MIDL , Attribute, Typkonvertierung und Marshalling
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 286de08a56aba5ffc7b73fc52791238a6af62b3f0545e95aedabcf79d5623464
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382736"
---
# <a name="type-conversion-and-marshaling-acf-attributes"></a>Type-Conversion und Marshalling von ACF-Attributen

Verwenden Sie diese Attribute, um zu steuern, wie Ihre Daten über das Netzwerk übertragen werden.



| attribute                                        | Verbrauch                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Codieren der**](encode.md)[**Decodierung**](decode.md) | Weist MIDL an, die Typ- oder Prozedurserialisierungsroutinen (Pickling) verfügbar zu machen, die für die Stubs generiert werden. Ihre Clientanwendung kann diese Routinen aufrufen, um Daten nach Wert zu marshallen.                                                                                                                                                                                                                                                                                  |
| [**darstellen \_ als**](represent-as.md)            | Gibt an, wie ein Datentyp im Netzwerk dargestellt wird, wenn die genaue Art des Datentyps eines Clients für den Server unwichtig ist (da er nur die Daten selbst und nicht die tatsächliche Struktur benötigt), oder der tatsächliche Clienttyp midl zur Kompilierzeit unbekannt ist. Wenn Ihre Clientanwendung beispielsweise eine verknüpfte Liste von Gleitkommazahlen verwendet, können Sie angeben, dass die Wire-Darstellung dieser Liste ein Array vom Typ [**float ist.**](float.md) |
| [**\_Benutzer-Marshalling**](user-marshal.md)            | Steuert, wie Daten über das Netzwerk übertragen werden, indem eigene Marshallingroutinen implementieren werden. Dieses Attribut ist nützlich, wenn Sie über einen Datentyp verfügen, der MIDL unbekannt ist, oder wenn Sie Informationen zwischen Big-Endian- und Little-Endian-Plattformen übergeben.                                                                                                                                                                                                                 |



 

Die DCE-Marshallingattribute [**in \_ Line und**](in-line.md) [**\_ Out-of-Line \_**](out-of-line.md) werden in Microsoft RPC nicht implementiert. Der MIDL-Compiler marshallt komplexe Datentypen automatisch out-of-line.

 

 




