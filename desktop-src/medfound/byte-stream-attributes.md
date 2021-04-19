---
description: Byte Datenstrom Attribute
ms.assetid: d57a57e9-87e4-4f7f-943a-63fd2ad1d1a6
title: Byte Datenstrom Attribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0471905925b397f4f83ad457384b5e9b4790b54c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346053"
---
# <a name="byte-stream-attributes"></a>Byte Datenstrom Attribute

Die folgenden Attribute gelten für einige Byte Datenströme. Um herauszufinden, ob ein Bytestream Attribute unterstützt, Fragen Sie das bytestreamobjekt nach der [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle ab.



| Attribut                                                                                  | BESCHREIBUNG                                                       |
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [**MF- \_ Bytestream- \_ \_ Inhaltstyp**](mf-bytestream-content-type-attribute.md)              | Gibt den MIME-Typ eines Bytestreams an.                         |
| [**MF- \_ \_ bytestreamdauer**](mf-bytestream-duration-attribute.md)                       | Gibt die Dauer eines Bytestreams in 100-Nanosecond-Einheiten an. |
| [MF- \_ Bytestream- \_ IFO-Datei- \_ \_ URI](mf-bytestream-ifo-file-uri.md)                           | Gibt die URL einer zugeordneten IFO-Datei an.                      |
| [**\_Zeitpunkt der \_ letzten Änderung des \_ MF-Bytestreams \_**](mf-bytestream-last-modified-time-attribute.md) | Gibt an, wann ein Bytestream zuletzt geändert wurde.                   |
| [**Name des MF- \_ Bytestream- \_ Ursprungs \_**](mf-bytestream-origin-name-attribute.md)                | Gibt die ursprüngliche URL für einen Byte Datenstrom an.                     |



 

Die folgenden Attribute gelten für Byte Datenstrom Handler.



| Attribut                                                                                    | BESCHREIBUNG                                                                                                |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [MF \_ bytestreamhandler \_ akzeptiert \_ Freigabe \_ Schreibvorgänge](mf-bytestreamhandler-accepts-share-write.md) | Gibt an, ob ein Byte Strom Handler einen Bytestream verwenden kann, der zum Schreiben durch einen anderen Thread geöffnet ist. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> <dt>

[Media Foundation Attribute](media-foundation-attributes.md)
</dt> </dl>

 

 



