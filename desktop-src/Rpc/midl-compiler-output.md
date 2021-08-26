---
title: MIDL-Compilerausgabe
description: Mit den IDL- und ACF-Dateien als Eingabe generiert der MIDL-Compiler bis zu fünf C-Sprachquelldateien.
ms.assetid: 151bd643-1da0-4b33-b8a3-3d7037e63319
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aea74b77d8e709d8a71d3c84f457d301bb38d8c35bdccaa77e9e3033d08ed70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019690"
---
# <a name="midl-compiler-output"></a>MIDL-Compilerausgabe

Mit den IDL- und ACF-Dateien als Eingabe generiert der MIDL-Compiler bis zu fünf C-Sprachquelldateien. Standardmäßig verwendet der MIDL-Compiler den Basisdateinamen der IDL-Datei als Teil der generierten Stubdateien. Wenn mehr als sechs Zeichen im Basisdateinamen vorhanden sind, akzeptieren einige Dateisysteme möglicherweise nicht den vollständigen Stubnamen. Die folgende Tabelle zeigt Konventionen, die für Dateinamen verwendet werden.



| Datei        | Standardteil des Basisdateinamens | Beispiel      |
|-------------|-----------------------------------|--------------|
| IDL-Datei    | ---                               | Abcdefgh.idl |
| Header      | .h                                | Abcdef.h     |
| Clientstub | \_Cc                             | Abcdef \_ c.c  |
| Serverstub | \_Nk                             | Abcdef \_ s.c  |



 

 

 




