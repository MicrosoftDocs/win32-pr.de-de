---
description: Der Positionstyp eines Inhaltsverzeichnisses
ms.assetid: cc2fbadc-43f7-470c-873b-de2dc9d84e5d
title: Der Positionstyp eines Inhaltsverzeichnisses
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f0f94f23e185b46f52123a80a0d27f7fefffcaff7e711a5e9718e07dab7da40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118237894"
---
# <a name="the-position-type-of-a-table-of-contents"></a>Der Positionstyp eines Inhaltsverzeichnisses

Einige Methoden der [**ITocParser-Schnittstelle**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) verfügen über einen Parameter mit dem Namen *enumTocPosType,* der über den Typ [**enum TOC \_ POS TYPE \_ verfügt.**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-toc_pos_type) Dieser Parameter gibt die Position in einer Mediendatei an, an der ein Inhaltsverzeichnis gespeichert wird. Die Absicht war, dass das Inhaltsverzeichnis entweder im Dateiheader oder im Textkörper der Datei als Objekt der obersten Ebene gespeichert werden konnte. Diese Funktionalität wurde noch nicht implementiert.

Derzeit können Inhaltstabellen nur als Objekte der obersten Ebene gespeichert werden. Daher müssen Sie den *Parameter enumTocPosType* immer auf **TOC \_ POS \_ TOPLEVELOBJECT** festlegen. Wenn Sie *enumTocPosType* auf **TOC \_ POS \_ INHEADER** festlegen, gibt die Methode **E \_ NOTIMPL** zurück.

Die folgenden Methoden verfügen über einen *enumTocPosType-Parameter.*

-   [**GetTocCount**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettoccount)
-   [**GetTocByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbyindex)
-   [**GetTocByType**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbytype)
-   [**AddToc**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-addtoc)
-   [**RemoveTocByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-removetocbyindex)
-   [**RemoveTocByType**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-removetocbytype)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmierhandbuch für den Inhaltsparser](toc-parser-programming-guide.md)
</dt> </dl>

 

 



