---
title: Erstellen einer Proxy-dll und einer Typbibliothek aus einer einzelnen IDL-Datei
description: Sie können eine einzelne IDL-Datei verwenden, um sowohl die proxystubdateien als auch die Header Dateien für das Mars Hallen von Code und eine Typbibliothek zu generieren.
ms.assetid: faa647ac-765a-45bd-8193-b6ea90d064ff
keywords:
- Microsoft Interface Definition Language mittlerer l, Tasks, Erstellen einer Proxy-dll und einer Typbibliothek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a81001bba7aeff416e765291d3e6660b705919a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037336"
---
# <a name="generating-a-proxy-dll-and-a-type-library-from-a-single-idl-file"></a>Erstellen einer Proxy-dll und einer Typbibliothek aus einer einzelnen IDL-Datei

Sie können eine einzelne IDL-Datei verwenden, um sowohl die proxystubdateien als auch die Header Dateien für das Mars Hallen von Code und eine Typbibliothek zu generieren. Hierzu definieren Sie eine Schnittstelle außerhalb des Bibliotheks Blocks und verweisen dann innerhalb des Bibliotheks Blocks auf diese Schnittstelle, wie im folgenden Beispiel gezeigt:

``` syntax
//file: AllKnown.idl

[
    object, uuid(. . .), <other interface attributes>
]
interface IKnown : IUnknown 
{
    import "unknwn.idl";
    <declarations, etc. for IKnown interface go here>
};

[
    <library attributes>
]
library KnownLibrary 
{

    //reference interface IKnown:
    interface IKnown;

    //or create a new class:
    [
        <coclass attributes>
    ] 
    coclass KnowMore 
    {
       interface IKnown;
    };
};
```

Weitere Informationen finden Sie unter [Mars Hallen von OLE-Datentypen](marshaling-ole-data-types.md) und [zusätzlichen Dateien, die zum Generieren einer Typbibliothek erforderlich](additional-files-required-to-generate-a-type-library-2.md)sind.

 

 




