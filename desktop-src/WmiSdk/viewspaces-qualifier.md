---
description: Der viewspaces-Qualifizierer definiert die Namen und den Speicherort der Namespaces, in denen sich die Quell Instanzen befinden. Sie können eine beliebige Kombination von Namespaces auf lokalen Computern oder Remote Computern angeben.
ms.assetid: 15d71bb6-842d-4f5a-b2e3-e9f60f0aea3b
ms.tgt_platform: multiple
title: Viewspaces Qualifizierer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ViewSpaces
api_type:
- NA
api_location: ''
ms.openlocfilehash: 683f5596497f3c1e1ad0f2b85eaaa1460177a0ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218290"
---
# <a name="viewspaces-qualifier"></a>Viewspaces Qualifizierer

Der **viewspaces-Qualifizierer** definiert die Namen und den Speicherort der Namespaces, in denen sich die Quell Instanzen befinden. Sie können eine beliebige Kombination von Namespaces auf lokalen Computern oder Remote Computern angeben.

Im folgenden Beispiel werden zwei Namespaces auf dem lokalen Computer aufgelistet.


```mof
ViewSpaces{"\\\\.\\root\\LocalNamespace",
     "\\\\.\\root\\RemoteNamespace"}
```



Der [Ansichts Anbieter](view-provider.md) entspricht den Quell Abfragen im Ansichts [Quellen-Qualifizierer](viewsources-qualifier.md) mit den Namespaces, die im **viewspaces** -Qualifizierer in der Reihenfolge aufgeführt sind, in der die Abfragen und Namespaces aufgelistet Normalerweise besteht eine eins-zu-eins-Beziehung zwischen der Anzahl der Namespaces **, die im** Ansichts Bereichs Qualifizierer aufgelistet sind, und den Abfragen, die im **viewsources** -Qualifizierer aufgelistet sind. In einigen Fällen möchten Sie möglicherweise, dass die im viewsources-Qualifizierer aufgelisteten Abfragen für zwei oder mehr Namespaces ausgeführt werden. Sie können einen doppelten Doppelpunkt "::" verwenden, um mehrere Namespaces zu trennen, die von einer der Abfragen im **viewsources** -Array ausgewertet werden.

Im folgenden Beispiel wird die erste Abfrage im [**viewsources**](viewsources-qualifier.md) -Array für den Namespace im ersten paar von Anführungszeichen, die zweite Abfrage für die drei Namespaces im zweiten paar von Anführungszeichen und die dritte Abfrage für die beiden Namespaces im dritten paar von Anführungszeichen ausgeführt.


```mof
ViewSpaces
    {
    "\\\\.\\root\\LocalNamespace",

    "\\\\.\\root\\RemoteNamespace1::
        \\\\.\\root\\RemoteNamespace2::
        \\\\.\\root\\RemoteNamespace3",

    "\\\\.\\root\\RemoteNamespace1::
        \\\\.\\root\\RemoteNamespace3"
    }
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Spezifische Qualifizierer für den Ansichts Anbieter**](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

 




