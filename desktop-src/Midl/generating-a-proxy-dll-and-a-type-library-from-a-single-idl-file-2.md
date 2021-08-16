---
title: Generieren einer Proxy-DLL und einer Typbibliothek aus einer einzelnen IDL-Datei
description: Sie können eine einzelne IDL-Datei verwenden, um sowohl die Proxystubs als auch Headerdateien zum Marshallen von Code und eine Typbibliothek zu generieren.
ms.assetid: faa647ac-765a-45bd-8193-b6ea90d064ff
keywords:
- Microsoft Interface Definition Language MIDL , Tasks, Generieren einer Proxy-DLL und einer Typbibliothek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92e7bf2694b791007b0f1da303525217cf55d75d574e083c6d1756bc2784d0ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384236"
---
# <a name="generating-a-proxy-dll-and-a-type-library-from-a-single-idl-file"></a>Generieren einer Proxy-DLL und einer Typbibliothek aus einer einzelnen IDL-Datei

Sie können eine einzelne IDL-Datei verwenden, um sowohl die Proxystubs als auch Headerdateien zum Marshallen von Code und eine Typbibliothek zu generieren. Hierzu definieren Sie eine Schnittstelle außerhalb des Bibliotheksblocks und verweisen dann innerhalb des Bibliotheksblocks auf diese Schnittstelle, wie in diesem Beispiel gezeigt:

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

Weitere Informationen finden Sie unter [Marshallen von OLE-Datentypen](marshaling-ole-data-types.md) und [zusätzlichen Dateien, die zum Generieren einer Typbibliothek erforderlich sind.](additional-files-required-to-generate-a-type-library-2.md)

 

 




