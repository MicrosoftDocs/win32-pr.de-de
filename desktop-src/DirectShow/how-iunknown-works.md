---
description: Funktionsweise von IUnknown
ms.assetid: 926778a5-e941-4424-8bc0-b50c925fd08b
title: Funktionsweise von IUnknown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a7549ce892e9c0dd3c82f1229a2440f1b930190
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123457"
---
# <a name="how-iunknown-works"></a>Funktionsweise von IUnknown

Die Methoden in **IUnknown** ermöglichen einer Anwendung das Abfragen von Schnittstellen für die Komponente und das Verwalten des Verweis Zählers der Komponente.

**Verweisanzahl**

Der Verweis Zähler ist eine interne Variable, die in der **adressf** -Methode inkrementiert und in der **releasemethode** dekrementiert wird. Die Basisklassen verwalten den Verweis Zähler und synchronisieren den Zugriff auf den Verweis Zähler zwischen mehreren Threads.

**Schnittstellen Abfragen**

Das Abfragen für eine Schnittstelle ist ebenfalls unkompliziert. Der Aufrufer übergibt zwei Parameter: einen Schnittstellen Bezeichner (IID) und die Adresse eines Zeigers. Wenn die Komponente die angeforderte Schnittstelle unterstützt, legt Sie den Zeiger auf die Schnittstelle fest, erhöht Ihren eigenen Verweis Zähler und gibt S \_ OK zurück. Andernfalls wird der Zeiger auf **null** festgelegt und E \_ nointerface zurückgegeben. Der folgende Pseudo Code zeigt die allgemeine Gliederung der **QueryInterface** -Methode. Die Komponenten Aggregation, die im nächsten Abschnitt beschrieben wird, führt zu einer zusätzlichen Komplexität.


```C++
if (IID == IID_IUnknown)
    set pointer to (IUnknown *)this
    AddRef
    return S_OK

else if (IID == IID_ISomeInterface)
    set pointer to (ISomeInterface *)this
    AddRef
    return S_OK

else if ... 

else
    set pointer to NULL
    return E_NOINTERFACE
```



Der einzige Unterschied zwischen der **QueryInterface** -Methode einer Komponente und der **QueryInterface** -Methode eines anderen ist die Liste der IIDs, die von den einzelnen Komponenten getestet werden. Für jede Schnittstelle, die von der Komponente unterstützt wird, muss die Komponente die IID der Schnittstelle testen.

**Aggregation und Delegierung**

Die Komponenten Aggregation muss für den Aufrufer transparent sein. Daher muss das Aggregat eine einzelne **IUnknown** -Schnittstelle verfügbar machen, wobei die aggregierte Komponente auf die Implementierung der äußeren Komponente zurückschiebt. Andernfalls würde der Aufrufer zwei verschiedene **IUnknown** -Schnittstellen im selben Aggregat sehen. Wenn die Komponente nicht aggregiert wird, verwendet Sie eine eigene Implementierung.

Um dieses Verhalten zu unterstützen, muss die Komponente eine Dereferenzierungsebene hinzufügen. Ein *delegier ender IUnknown* delegiert die Arbeit an die entsprechende Stelle: an die äußere Komponente, sofern vorhanden, oder an die interne Version der Komponente. Ein nicht *delegier Endes IUnknown* führt die Arbeit aus, wie im vorherigen Abschnitt beschrieben.

Die delegier Ende Version ist öffentlich und behält den Namen " **IUnknown**" bei. Die nicht delegier Ende Version wurde in [**inondelegatingunknown**](inondelegatingunknown.md)umbenannt. Dieser Name ist nicht Teil der com-Spezifikation, da es sich nicht um eine öffentliche Schnittstelle handelt.

Wenn der Client eine Instanz der Komponente erstellt, wird die **IClassFactory::** -Methode aufgerufen. Ein Parameter ist ein Zeiger auf die **IUnknown** -Schnittstelle der aggregatkomponente oder **null** , wenn die neue Instanz nicht aggregiert wird. Die Komponente speichert mithilfe dieses Parameters eine Member-Variable, die angibt, welche **IUnknown** -Schnittstelle verwendet werden soll, wie im folgenden Beispiel gezeigt:


```C++
CMyComponent::CMyComponent(IUnknown *pOuterUnkown)
{
    if (pOuterUnknown == NULL)
        m_pUnknown = (IUnknown *)(INonDelegatingUnknown *)this;
    else
        m_pUnknown = pOuterUnknown;

    [ ... more constructor code ... ]
}
```



Jede Methode in der delegierenden **IUnknown** -Methode ruft ihren nicht delegierenden Gegenstück auf, wie im folgenden Beispiel gezeigt:


```C++
HRESULT QueryInterface(REFIID iid, void **ppv) 
{
    return m_pUnknown->QueryInterface(iid, ppv);
}
```



Aufgrund der Art der Delegierung sehen die delegatenmethoden in jeder Komponente identisch aus. Nur die nicht delegierenden Versionen werden geändert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Implementieren von IUnknown](how-to-implement-iunknown.md)
</dt> </dl>

 

 



