---
title: Aliasing-und Marshallingattribute
description: Verteilte Anwendungen übergeben fast immer Daten zwischen Client-und Serverprogrammen, wenn Sie Schnittstellen Prozeduren aufzurufen.
ms.assetid: 64895c64-f16b-47c4-928d-5149808b0476
keywords:
- IDL-Mittell, Attribute-Mittell, Aliasing und Marshalling
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ac66aa04210a878c67ee6bcf1a50ff21fa1d1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037543"
---
# <a name="aliasing-and-marshaling-attributes"></a>Aliasing-und Marshallingattribute

Verteilte Anwendungen übergeben fast immer Daten zwischen Client-und Serverprogrammen, wenn Sie Schnittstellen Prozeduren aufzurufen. Entwickler verwenden die Mittel l, um die Daten zu beschreiben, die von Client-und Serverprogrammen standardmäßig bestanden werden. Der mittlerer l-Compiler erstellt anwendungstub-oder Proxy Programme für den Client und den Server, die die Daten in eine standardisierte Form konvertieren, die über ein Netzwerk gesendet werden kann. Dieses Format, das Format der Netzwerkdaten Darstellung (Network Data Darstellung, NDR), wird häufig als Wire-Format der Daten bezeichnet. Die Stubdateien müssen Daten aus ihrem systemeigenen Format im Speicherbereich des Programms in den NDR konvertieren. Diese Konvertierung wird als Marshalling der Daten bezeichnet. Wenn ein Client-oder Serverprogramm Daten empfängt, muss es die Daten von der NDR in das systemeigene Format für dieses Programm konvertieren. Dies wird als "Unmarshalling der Daten" bezeichnet.

Verwenden Sie Aliasing-und Marshallingattribute, um zu steuern, wie Ihre Daten in das NDR-Format gepackt und über das Netzwerk übertragen werden.



| Attribut                             | Verbrauch                                                                                                                         |
|---------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**aufzurufen \_ als**](call-as.md)           | Ordnet einem Remote Prozedur aufzurufen eine nicht Remote fähige Funktion zu.                                                                      |
| [**IID \_ ist**](iid-is.md)             | Stellt den Schnittstellen Bezeichner der COM-Schnittstelle bereit, die das-Objekt des Zeigers ist.                                     |
| [**übertragen \_ als**](transmit-as.md)   | Konvertiert einen Datentyp in einen einfacheren Typ für die Übertragung über ein Netzwerk.                                                       |
| [**Wire \_ Marshal**](wire-marshal.md) | Ähnlich wie bei der über [**Tragung \_ als**](transmit-as.md) , aber implementieren Sie die Routinen, um die Daten zu verkleinern, zu Mars Hallen, zu entsperren und freizugeben. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Typkonvertierung und Marshalling von ACF-Attributen](type-conversion-and-marshaling-acf-attributes.md)
</dt> </dl>

 

 




