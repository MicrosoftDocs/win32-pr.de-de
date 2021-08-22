---
description: Der ViewSpaces-Qualifizierer definiert die Namen und den Speicherort der Namespaces, in denen sich die Quellinstanzen befinden. Sie können eine beliebige Kombination von Namespaces auf lokalen computern oder Remotecomputern angeben.
ms.assetid: 15d71bb6-842d-4f5a-b2e3-e9f60f0aea3b
ms.tgt_platform: multiple
title: ViewSpaces-Qualifizierer
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
ms.openlocfilehash: edaec0328d67ad540a12e3393aabf5b973112bbf00f64f735d6a5f64cf338365
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049898"
---
# <a name="viewspaces-qualifier"></a>ViewSpaces-Qualifizierer

Der **ViewSpaces-Qualifizierer** definiert die Namen und den Speicherort der Namespaces, in denen sich die Quellinstanzen befinden. Sie können eine beliebige Kombination von Namespaces auf lokalen computern oder Remotecomputern angeben.

Im folgenden Beispiel werden zwei Namespaces auf dem lokalen Computer aufgelistet.


```mof
ViewSpaces{"\\\\.\\root\\LocalNamespace",
     "\\\\.\\root\\RemoteNamespace"}
```



Der [View-Anbieter](view-provider.md) gleicht die Quellabfragen im [ViewSources-Qualifizierer](viewsources-qualifier.md) mit den Namespaces ab, die im **ViewSpaces-Qualifizierer** in der Reihenfolge aufgeführt sind, in der die Abfragen und Namespaces aufgeführt sind. Normalerweise besteht eine 1:1-Beziehung zwischen der Anzahl der Namespaces, die im **ViewSpaces-Qualifizierer** aufgeführt sind, und den Abfragen, die im **ViewSources-Qualifizierer** aufgeführt sind. In einigen Fällen möchten Sie möglicherweise, dass die im ViewSources-Qualifizierer aufgeführten Abfragen für zwei oder mehr Namespaces ausgeführt werden. Sie können einen doppelten Doppelpunkt "::" verwenden, um mehrere Namespaces zu trennen, die von einer der Abfragen im **ViewSources-Array** ausgewertet werden.

Im folgenden Beispiel wird die erste Abfrage im [**ViewSources-Array**](viewsources-qualifier.md) für den Namespace im ersten Anführungszeichenpaar ausgeführt, die zweite Abfrage für die drei Namespaces im zweiten Anführungszeichenpaar und die dritte Abfrage für die beiden Namespaces im dritten Anführungszeichenpaar.


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

[**Qualifizierer, die für den Ansichtsanbieter spezifisch sind**](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

 




