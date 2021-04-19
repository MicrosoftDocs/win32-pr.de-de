---
description: Der Positionstyp eines Inhaltsverzeichnisses.
ms.assetid: cc2fbadc-43f7-470c-873b-de2dc9d84e5d
title: Der Positionstyp eines Inhaltsverzeichnisses.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e1b6782a3722a6ce5a36117694f35442f8e4d43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348904"
---
# <a name="the-position-type-of-a-table-of-contents"></a>Der Positionstyp eines Inhaltsverzeichnisses.

Einige Methoden der [**idecparser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) -Schnittstelle verfügen über einen Parameter mit dem Namen *enumerationstype* , der den Typ des [**\_ \_ Enumerationstyps**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-toc_pos_type)Enumerationstyp hat. Dieser Parameter gibt die Position in einer Mediendatei an, in der ein Inhaltsverzeichnis gespeichert wird. Die Absicht war, dass das Inhaltsverzeichnis entweder im Dateiheader oder im Text der Datei als Objekt der obersten Ebene gespeichert werden konnte. Diese Funktionalität wurde noch nicht implementiert.

Tabellen mit Inhalten können derzeit nur als Objekte der obersten Ebene gespeichert werden. Daher müssen Sie den Enumerations Parameter " *enumcpostype* " immer auf " **TC \_ POS \_ toplevelobject**" festlegen. Wenn Sie " *enumercpostype* " auf " **Dec \_ POS \_ inheader**" festlegen, gibt die Methode " **E \_ notimpl**" zurück.

Die folgenden Methoden verfügen über einen *enumycpostype* -Parameter.

-   [**Getdeccount**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettoccount)
-   [**Getdecbyindex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbyindex)
-   [**Getdecbytype**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbytype)
-   [**Addinhalts Verzeichnis**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-addtoc)
-   [**Removedecbyindex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-removetocbyindex)
-   [**Removedecbytype**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-removetocbytype)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmier Handbuch für das Inhaltsverzeichnis des Parsers](toc-parser-programming-guide.md)
</dt> </dl>

 

 



