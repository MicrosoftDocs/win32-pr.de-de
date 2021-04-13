---
description: Verwenden einer Objektkonstruktorzeichenfolge zum Erstellen einer Komponente
ms.assetid: 57d66988-2a65-4309-957a-36a5972233b5
title: Verwenden einer Objektkonstruktorzeichenfolge zum Erstellen einer Komponente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8cbbb1c156fd7ee675b6c21c8ae097494da59ab
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483411"
---
# <a name="using-an-object-constructor-string-to-construct-a-component"></a>Verwenden einer Objektkonstruktorzeichenfolge zum Erstellen einer Komponente

Im folgenden Beispiel wird veranschaulicht, wie eine Objektkonstruktorzeichenfolge Programm gesteuert abgerufen und verwendet wird, wenn eine Komponente instanziiert wird. Es zeigt eine Implementierung der [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct) -Schnittstelle, die eine Objektkonstruktorzeichenfolge abruft. Die Zeichenfolge kann dann analysiert werden, um Anfangswerte festzulegen oder das Verhalten der Komponente zu beeinflussen.

## <a name="visual-basic"></a>Visual Basic


```VB
Implements IObjectConstruct
Private Sub IObjectConstruct_Construct( ByVal pCtorObj As Object )
    Dim strConstructorString As String
    strConstructorString = pCtorObj.ConstructString
     Parse and use strConstructorString here. 
End Sub
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konzepte der com+-objektkonstruktorzeichenfolgen](com--object-constructor-strings-concepts.md)
</dt> <dt>

[Angeben einer Objektkonstruktorzeichenfolge für eine Komponente](specifying-an-object-constructor-string-for-a-component.md)
</dt> </dl>

 

 



