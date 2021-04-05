---
title: Bestimmen der Schnittstelle, die ein Objekt unterstützt
description: Bestimmen der Schnittstelle, die ein Objekt unterstützt
ms.assetid: cf2aacb7-5315-4907-a49b-3eb3bbfd13d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 066523503232926f5c031efa2cee5ad7a2b05d24
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713793"
---
# <a name="determining-which-interface-an-object-supports"></a>Bestimmen der Schnittstelle, die ein Objekt unterstützt

Mit der **QueryInterface** -Methode kann eine Anwendung ein Objekt Abfragen, um zu bestimmen, welche Schnittstellen es unterstützt. In der Beispielanwendung wird der *PPV* -Zeiger auf die aktuelle-Schnittstelle festgelegt.


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



 

 




