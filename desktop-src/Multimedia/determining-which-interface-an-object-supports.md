---
title: Bestimmen, welche Schnittstelle ein Objekt unterstützt
description: Bestimmen, welche Schnittstelle ein Objekt unterstützt
ms.assetid: cf2aacb7-5315-4907-a49b-3eb3bbfd13d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e5afffd2818c7a8f204363180e52fe9f94f16157aacd027582ce377b2f5211c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497256"
---
# <a name="determining-which-interface-an-object-supports"></a>Bestimmen, welche Schnittstelle ein Objekt unterstützt

Mit **der QueryInterface-Methode** kann eine Anwendung ein Objekt abfragen, um zu bestimmen, welche Schnittstellen sie unterstützt. Die Beispielanwendung legt den *ppv-Zeiger* auf die aktuelle Schnittstelle fest.


```C++
STDMETHODIMP CAVIFileCF::QueryInterface( 
    const IID FAR& iid, 
    void FAR* FAR* ppv) 
{ 
    if (iid == IID_IUnknown) 
        *ppv = this;                     // set the interface pointer 
                                         // to this instance 
    else if (iid == IID_IClassFactory) 
        *ppv = this;                     // second chance to set the 
                                         // interface pointer to this 
                                         // instance 
    else 
        return ResultFromScode(E_NOINTERFACE); 
    AddRef();  //Increment the reference count 
    return NULL; 
} 

```



 

 




