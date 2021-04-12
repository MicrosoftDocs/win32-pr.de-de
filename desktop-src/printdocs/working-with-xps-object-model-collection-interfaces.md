---
description: Beschreibt, wie die allgemeinen Methoden der Auflistungs Schnittstellen verwendet werden.
ms.assetid: 6ea311c0-a155-47de-ad40-62b0cbeb6e8f
title: Arbeiten mit XPS OM-Sammlungs Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7cda84243347680d91a6f3a5255f7ebf4e66932
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216630"
---
# <a name="working-with-xps-om-collection-interfaces"></a>Arbeiten mit XPS OM-Sammlungs Schnittstellen

Beschreibt, wie die allgemeinen Methoden der Auflistungs Schnittstellen verwendet werden.

## <a name="contents"></a>Inhalte

Die in diesem Abschnitt beschriebenen Methoden werden in der folgenden Liste angezeigt. Nicht alle Sammlungs Schnittstellen unterstützen diese Methoden, und einige Schnittstellen unterstützen auch Methoden, die nicht auf dieser Seite beschrieben werden. Eine Liste der Methoden, die von einer bestimmten Schnittstelle unterstützt werden, finden Sie in der Beschreibung der Beschreibung der Schnittstelle.

<dl>

[Append-Methode](#append-method)  
[GetAt-Methode](#getat-method)  
[GetCount-Methode](#getcount-method)  
[InsertAt-Methode](#insertat-method)  
[RemoveAt-Methode](#removeat-method)  
[Methode "-Methode"](#setat-method)  
</dl>

[Weitere Informationen](#see-also)

## <a name="append-method"></a>Append-Methode

Fügt ein Objekt an das Ende der Auflistung an.

**Generische Syntax**


```C++
HRESULT Append(
  [in]  Object *object
);
```



**Beschreibung**

Am Ende der Auflistung fügt diese Methode ein Objekt an, das in der Parameterliste übergeben wird, wie im folgenden Diagramm dargestellt.

![eine Abbildung, die zeigt, wie Anfügen der Auflistung einen Eintrag hinzufügt.](images/generic-append.png)

## <a name="getat-method"></a>GetAt-Methode

Ruft ein-Objekt von einer angegebenen Position in der Auflistung ab.

**Generische Syntax**


```C++
HRESULT GetAt(
  [in]           UINT32 index,
  [out, retval]  Object **object
);
```



**Beschreibung**

Schreibt das-Objekt, das am durch *Index* angegebenen Speicherort der Auflistung gespeichert ist, in die Variable, auf die vom- *Objekt* verwiesen wird. Durch diese Aktion wird der Inhalt der Sammlung nicht geändert. Dieser Prozess wird anhand des folgenden Diagramms veranschaulicht.

![eine Abbildung, die zeigt, wie GetAt einen Eintrag aus der Auflistung abruft.](images/generic-getat.png)

## <a name="getcount-method"></a>GetCount-Methode

Ruft die Anzahl der-Objekte ab, die in der Auflistung gespeichert sind.

**Generische Syntax**


```C++
HRESULT GetCount(
  [out, retval]  UINT32 *count
);
```



**Beschreibung**

Schreibt die Anzahl der-Objekte, die zurzeit in der Auflistung gespeichert sind, in die Variable, auf die von *count* verwiesen wird. Durch diese Aktion wird der Inhalt der Sammlung nicht geändert. Dieser Prozess wird anhand des folgenden Diagramms veranschaulicht.

![eine Abbildung, die zeigt, wie GetCount die Anzahl der Einträge in der Auflistung abruft.](images/generic-getcount.png)

## <a name="insertat-method"></a>InsertAt-Methode

Fügt ein-Objekt an einer angegebenen Position der Auflistung ein.

**Generische Syntax**


```C++
HRESULT InsertAt(
  [in]  UINT32 index,
  [in]  Object *object
);
```



**Beschreibung**

Das Objekt, das in das- *Objekt* übermittelt wird, wird in die-Auflistung an der durch den *Index* angegebenen Position eingefügt. Bevor das neue- *Objekt* eingefügt wird, verschiebt diese Methode um 1 das Objekt, das die Position zuvor am *Index* belegt hat, und verschiebt alle Schnittstellen Zeiger nach dem *Index*. Dieser Prozess wird anhand des folgenden Diagramms veranschaulicht.

![eine Abbildung, die zeigt, wie InsertAt der Auflistung einen Eintrag hinzufügt.](images/generic-insertat.png)

## <a name="removeat-method"></a>RemoveAt-Methode

Entfernt das-Objekt aus einer angegebenen Position in der Auflistung.

**Generische Syntax**


```C++
HRESULT RemoveAt(
  [in]  UINT32 index
);
```



**Beschreibung**

Diese Methode gibt das Objekt aus der durch den *Index* angegebenen Position frei und komprimiert dann die Auflistung, indem Sie um 1 den Index jedes Zeigers nach dem *Index* reduziert. Dieser Prozess wird anhand des folgenden Diagramms veranschaulicht.

![eine Abbildung, die zeigt, wie RemoveAt einen Eintrag aus der Sammlung entfernt](images/generic-removeat.png)

## <a name="setat-method"></a>Methode "-Methode"

Ersetzt das-Objekt an einer angegebenen Position in der Auflistung.

**Generische Syntax**


```C++
HRESULT SetAt(
  [in]  UINT32 index,
  [in]  Object *object
);
```



**Beschreibung**

Diese Methode gibt zuerst das Objekt an dem Speicherort aus, auf den der *Index* verweist, und ersetzt dieses Objekt dann durch das Objekt, das im- *Objekt* weitergegeben wird. Dieser Prozess wird anhand des folgenden Diagramms veranschaulicht.

![eine Abbildung, die zeigt, wie das-enumerationszeichen einen Eintrag in der Auflistung ersetzt](images/generic-setat.png)

## <a name="see-also"></a>Weitere Informationen

<dl>

[**Ixpsomcolorprofileresourcecollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcolorprofileresourcecollection)  
[**Ixpsomdashcollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdashcollection)  
[**Ixpsomdocumentcollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)  
[**Ixpsomfontresourcecollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresourcecollection)  
[**Ixpsomgeometryfigurückruf**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigurecollection)  
[**Ixpsomgradientstopcollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstopcollection)  
[**Ixpsomimageresourcecollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresourcecollection)  
[**Ixpsomnamecollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)  
[**Ixpsompagereferencecollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection)  
[**Ixpsomparamecollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomparturicollection)  
[**Ixpsomremotediktattionaryresourcecollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresourcecollection)  
[**Ixpsomsignatureblockresourcecollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsignatureblockresourcecollection)  
[**Ixpsomvisualcollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)  
[**Ixpssignatureblockcollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblockcollection)  
[**Ixpssignaturückruf**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection)  
[**Ixpssignaturerequestcollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequestcollection)  
</dl>

 

 



