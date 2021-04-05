---
title: Type-Conversion und Marshalling von ACF-Attributen
description: Verwenden Sie diese Attribute, um zu steuern, wie Ihre Daten über das Netzwerk übertragen werden.
ms.assetid: 6af635f6-eeee-4fa6-85db-5d60434a1235
keywords:
- ACF-Mittell, Attribute, Typkonvertierung und Marshalling
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14367be3df97cc1185fca64e46aafe1d342f3526
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947963"
---
# <a name="type-conversion-and-marshaling-acf-attributes"></a>Type-Conversion und Marshalling von ACF-Attributen

Verwenden Sie diese Attribute, um zu steuern, wie Ihre Daten über das Netzwerk übertragen werden.



| Attribut                                        | Verbrauch                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [](encode.md)[**decodieren**](decode.md) | Weist die Mittell an, die Routinen für den Typ oder die Prozedur-Serialisierung (Pickup) verfügbar zu machen, die für die stubräume generiert werden Die Client Anwendung kann diese Routinen aufrufen, um Daten nach Wert zu Mars Hallen.                                                                                                                                                                                                                                                                                  |
| [**Darstellung \_ als**](represent-as.md)            | Gibt an, wie ein Datentyp bei der Übertragung dargestellt wird, wenn die genaue Natur eines Client Datentyps für den Server unerheblich ist (weil er nur die Daten selbst und nicht die tatsächliche Struktur benötigt), oder wenn der tatsächliche Clienttyp zur Kompilierzeit nicht der Mitte unbekannt ist. Wenn Ihre Client Anwendung z. b. eine verknüpfte Liste von Gleit Komma Zahlen verwendet, können Sie angeben, dass die Wire-Darstellung dieser Liste ein Array vom Typ " [**float**](float.md)" sein soll. |
| [**Benutzer \_ Mars Hall**](user-marshal.md)            | Steuert, wie Daten über das Netzwerk übertragen werden, indem ihre eigenen Marshallingroutinen implementiert werden. Dieses Attribut ist nützlich, wenn Sie einen Datentyp haben, der in der mittleren l unbekannt ist, oder wenn Sie Informationen zwischen Big-Endian-und Little-Endian-Plattformen übergeben.                                                                                                                                                                                                                 |



 

Das DCE-Marshalling von Attributen [**in \_ Zeile**](in-line.md) und [**außerhalb \_ der \_ Zeile**](out-of-line.md) ist nicht in Microsoft RPC implementiert. Der mittlerer l-Compiler marshaut komplexe Datentypen automatisch out-of-Line.

 

 




