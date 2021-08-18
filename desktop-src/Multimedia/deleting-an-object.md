---
title: Löschen eines Objekts
description: Löschen eines Objekts
ms.assetid: 54ea1e7d-75b5-461f-b0d6-a976c33d66fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e94e55c025d3358f50170b83042b6e888622e14897d02607b9fc24ed0dea1c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144533"
---
# <a name="deleting-an-object"></a>Löschen eines Objekts

Die **Release-Methode** löscht das Objekt, wenn der Verweiszähler 0 (null) ist.


```C++
STDMETHODIMP_(ULONG) CAVIFileCF::Release() 
{ 
    if (!--m_refs) 
    { 
        delete this;   // If O, delete this instance. 
        return 0; 
    } 
    return m_refs; 
} 

```



 

 




