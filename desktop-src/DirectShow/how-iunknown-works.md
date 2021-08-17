---
description: Funktionsweise von IUnknown
ms.assetid: 926778a5-e941-4424-8bc0-b50c925fd08b
title: Funktionsweise von IUnknown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1523a8de5d9b99df60ebaff540d4bf9468799e3be1361a4be111f15a142bbea9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015588"
---
# <a name="how-iunknown-works"></a>Funktionsweise von IUnknown

Die Methoden in **IUnknown** ermöglichen einer Anwendung, Schnittstellen für die Komponente abzufragen und den Verweiszähler der Komponente zu verwalten.

**Verweisanzahl**

Der Verweiszähler ist eine interne Variable, die in der **AddRef-Methode** erhöht und in der **Release-Methode** dekrementiert wird. Die Basisklassen verwalten den Verweiszähler und synchronisieren den Zugriff auf die Verweisanzahl zwischen mehreren Threads.

**Schnittstellenabfragen**

Das Abfragen einer Schnittstelle ist ebenfalls unkompliziert. Der Aufrufer übergibt zwei Parameter: einen Schnittstellenbezeichner (IID) und die Adresse eines Zeigers. Wenn die Komponente die angeforderte Schnittstelle unterstützt, legt sie den Zeiger auf die Schnittstelle fest, erhöht ihren eigenen Verweiszähler und gibt S \_ OK zurück. Andernfalls wird der Zeiger auf **NULL** festgelegt und E \_ NOINTERFACE zurückgegeben. Der folgende Pseudocode zeigt die allgemeine Gliederung der **QueryInterface-Methode.** Die im nächsten Abschnitt beschriebene Komponentenaggregation führt zu einer zusätzlichen Komplexität.


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



Der einzige Unterschied zwischen der **QueryInterface-Methode** einer Komponente und der **QueryInterface-Methode** einer anderen Komponente ist die Liste der IIDs, die jede Komponente testet. Für jede Schnittstelle, die von der Komponente unterstützt wird, muss die Komponente auf die IID dieser Schnittstelle testen.

**Aggregation und Delegierung**

Die Komponentenaggregation muss für den Aufrufer transparent sein. Daher muss das Aggregat eine einzelne **IUnknown-Schnittstelle** verfügbar machen, wobei die aggregierte Komponente auf die Implementierung der äußeren Komponente zurückstellung. Andernfalls würde der Aufrufer zwei verschiedene **IUnknown-Schnittstellen** im selben Aggregat sehen. Wenn die Komponente nicht aggregiert wird, verwendet sie ihre eigene Implementierung.

Um dieses Verhalten zu unterstützen, muss die Komponente eine Dekonstruktionsebene hinzufügen. Eine *delegierende IUnknown* delegiert die Arbeit an die entsprechende Stelle: an die äußere Komponente, sofern vorhanden, oder an die interne Version der Komponente. Ein *nicht delegierender IUnknown* übernimmt die Arbeit, wie im vorherigen Abschnitt beschrieben.

Die delegierende Version ist öffentlich und behält den Namen **IUnknown** bei. Die nicht delegierende Version wird in [**INonDelegatingUnknown**](inondelegatingunknown.md)umbenannt. Dieser Name ist nicht Teil der COM-Spezifikation, da er keine öffentliche Schnittstelle ist.

Wenn der Client eine Instanz der Komponente erstellt, ruft er die **IClassFactory::CreateInstance-Methode** auf. Ein Parameter ist ein Zeiger auf die **IUnknown-Schnittstelle** der aggregierenden Komponente oder **NULL,** wenn die neue Instanz nicht aggregiert wird. Die Komponente verwendet diesen Parameter, um eine Membervariable zu speichern, die angibt, welche **IUnknown-Schnittstelle** verwendet werden soll, wie im folgenden Beispiel gezeigt:


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



Jede Methode im delegierenden **IUnknown** ruft ihre nicht delegierende Entsprechung auf, wie im folgenden Beispiel gezeigt:


```C++
HRESULT QueryInterface(REFIID iid, void **ppv) 
{
    return m_pUnknown->QueryInterface(iid, ppv);
}
```



Aufgrund der Art der Delegierung sehen die delegierenden Methoden in jeder Komponente identisch aus. Nur die nicht delegierenden Versionen ändern sich.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Implementieren von IUnknown](how-to-implement-iunknown.md)
</dt> </dl>

 

 



