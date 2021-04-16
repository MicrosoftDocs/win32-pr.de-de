---
description: Handles bieten eine effiziente Möglichkeit zum Verweisen auf Techniken, Durchgänge, Anmerkungen und Parameter mit ID3DXEffectCompiler oder ID3DXEffect.
ms.assetid: 2494ecf9-88a7-43dc-a75b-ed743b11993a
title: Handles (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9e0dbbcbbc38685cae7c89b334bfb5458bc8386
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521427"
---
# <a name="handles-direct3d-9"></a>Handles (Direct3D 9)

Handles bieten eine effiziente Möglichkeit zum Verweisen auf Techniken, Durchgänge, Anmerkungen und Parameter mit [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) oder [**ID3DXEffect**](id3dxeffect.md). Sie werden dynamisch generiert, wenn Sie Funktionen des Formulars get \[ Parameter \| Annotation \| Function \| Technique \| Pass \] \[ Name \| bysemantic Element aufrufen \| \] .

Wenn Sie ein Programm ausführen und gleichzeitig ein Handle für ein Objekt erstellen, wird jedes Mal dasselbe Handle zurückgegeben. Verlassen Sie sich jedoch nicht darauf, dass das Handle konstant bleibt, wenn Sie das Programm mehrmals ausführen. Beachten Sie auch, dass Handles, die von verschiedenen Instanzen von [**ID3DXEffect**](id3dxeffect.md) und [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) generiert werden, unterschiedlich sind.

Wenn Sie die Header Dateien anzeigen, bemerken Sie, dass Handles (D3DXHANDLEs) technische Zeichen folgen Zeiger sind.

Die Handles, die Sie in Funktionen übergeben, wie z. b. GetParameter \[ byname- \| Element \| bysemantic \] oder GetAnnotation \[ byname, \] können wie folgt in drei Formen vorliegen:

1.  Handles, die von Funktionen zurückgegeben wurden, wie z. b. GetParameter \[ byname- \| Element \| bysemantic \] .
2.  Zeichen folgen, wie z. b. MyVariableName, mytechniquename oder myArray \[ 0 \] .
3.  Handle = **null**. Es gibt vier Fälle.
    -   Wenn es sich um einen Methodenrückgabewert handelt, konnte die Methode das Handle nicht finden.
    -   Wenn ein **null** -Handle als erster Parameter der GetParameter \[ byname-Element- \| bysemantic übergeben wird \| \] , gibt die Funktion einen Parameter der obersten Ebene zurück. Wenn das Handle hingegen nicht **null** ist, gibt die Funktion ein Strukturmember oder Element zurück, das durch das Handle identifiziert wird.
    -   Wenn ein **null** -Handle als erstes Argument von validatetechnique oder das zweite Argument von isparameterused übergangen wird, wird die aktuelle Technik überprüft.
    -   Wenn ein **null** -Handle als erstes Argument von findnextvalidtechnique übergeben wird, beginnt die Suche nach einer gültigen Technik bei der ersten Technik in der Wirkung.

Leistungs Tipp zum Start der Anwendung führen Sie einen Initialisierungs Durchlauf aus, um Handles aus den Zeichen folgen zu generieren. Verwenden Sie ab diesem Zeitpunkt nur Handles. Das übergeben von Zeichen folgen anstelle von generierten Handles ist langsamer.

## <a name="examples"></a>Beispiele

Im folgenden finden Sie einige Beispiele für die Funktionsweise der Funktion "get \[ Parameter \| Annotation \| Function Function \| \| Pass \] \[ Name \| bysemantic \| Element" \] , um Handles zu generieren.


```
// Gets handle of second top-level parameter handle in the effect file
h1 = GetParameter(NULL, 1);    

// Gets handle of the third struct member of MyStruct
h2 = GetParameter("MyStruct", 2); 

// Gets handle of the third array element handle of MyArray
h3 = GetParameterElement("MyArray", 2); 

// Gets handle of first member of h1 (that is, the second top-level param)
h4 = GetParameter(h1, 0);    

// Gets handle of MyStruct.Data
h5 = GetParameterByName("MyStruct", "Data");    
// or 
h6 = GetParameterByName(NULL, "MyStruct.Data");    

// Gets handle of MyStruct.Data.SubData
h7 = GetParameterByName("MyStruct.Data", "SubData"); 
// or 
h8 = GetParameterByName(NULL, "MyStruct.Data.SubData");

// Gets handle of fifth annotation of h1 (that is, second top-level param)
h9 = GetAnnotation(h1, 4);    

// Gets handle of MyStruct's annotation, called Author
h10 = GetAnnotationByName("MyStruct", "Author");  
// or
h11 = GetParameterByName(NULL, "MyStruct@Author"); 
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effekt Format](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



