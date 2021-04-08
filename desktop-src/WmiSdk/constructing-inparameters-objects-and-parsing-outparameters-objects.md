---
description: Normalerweise ist der direkte Zugriff ausreichend, um eine WMI-Anbieter Methode aufzurufen.
ms.assetid: be9332b5-8094-44a2-8632-af9957ecf36b
ms.tgt_platform: multiple
title: Erstellen von InParameters-Objekten und übernehmen von outparameter-Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a291d4fd44e69e87572684856bba587685e1f07b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960221"
---
# <a name="constructing-inparameters-objects-and-parsing-outparameters-objects"></a>Erstellen von InParameters-Objekten und übernehmen von outparameter-Objekten

Normalerweise ist der direkte Zugriff ausreichend, um eine WMI- [*Anbieter Methode*](gloss-p.md)aufzurufen. Direkter Zugriff bedeutet, dass eine Methode mithilfe der *Object. Method* -Syntax ausgeführt wird. In einigen Fällen kann der direkte Zugriff jedoch nicht verwendet werden. Außerdem erfordert der asynchrone Aufruf einer Anbieter Methode aus einem Skript einen [**ExecMethodAsync**](swbemobject-execmethodasync-.md) -Aufgabentyp.

> [!Note]  
> Da der Rückruf für die Senke möglicherweise nicht auf derselben Authentifizierungs Ebene wie der Client zurückgegeben wird, wird empfohlen, semisynchrone anstelle der asynchronen Kommunikation zu verwenden. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

 

Die Reihenfolge der Eingabe-und Ausgabeparameter der Methode wird im MOF-Schema (Managed Object Format) für die Methode definiert. WMI verhindert nicht, dass die Parameterreihenfolge geändert wird, wenn die Klasse von " [MUF Comp](mofcomp.md)" neu kompiliert wird. Mit einem [**InParameters**](swbemmethod-inparameters.md) -Objekt können Sie Probleme vermeiden, die sich aus dem geänderten Schema ergeben, da die Eingabeparameter anhand des Namens identifiziert werden. Der richtige Parameter kann angezeigt werden, indem Sie den **ID** -Qualifizierer der einzelnen Eingabeparameter untersuchen. Der erste Parameter weist den **ID** -Wert 0 (null) auf.

[**Die Methoden SWbemObject.Exe\_ cmethod**](swbemobject-execmethod-.md), [**SWbemObject.Execmethodasync \_**](swbemobject-execmethodasync-.md), [**SWbemServices.Execmethod**](swbemservices-execmethod.md)und [**SWbemServices.Execmethodasync**](swbemservices-execmethodasync.md) bieten eine alternative Möglichkeit, eine Anbieter Methode auszuführen, wenn es nicht möglich ist, eine Methode direkt auszuführen. Weitere Informationen finden Sie unter Bearbeiten von [Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md).

Weitere Informationen zu Parametern finden Sie unter [Erstellen von inparameter-Objekten](constructing-inparameters-objects.md) und Auswerten von [outparameter-Objekten](parsing-outparameters-objects.md).

 

 



