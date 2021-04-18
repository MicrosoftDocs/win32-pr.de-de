---
description: Eine weitere Möglichkeit zum Erstellen eines Namespace ist die Verwendung von Managed Object Format (MOF)-Code zum Erstellen eines gleich geordneten Namespace. Ein gleich geordneter Namespace ist ein Namespace, der nicht als untergeordnetes Element des aktuellen Namespace vorhanden ist.
ms.assetid: 1a3f8569-e725-4158-9a2b-b440b9247925
ms.tgt_platform: multiple
title: Erstellen eines gleich geordneten Namespace mit MOF-Code
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4fcbf6e16ad51ab9a0df63e3497735b07cd6afc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352694"
---
# <a name="creating-a-sibling-namespace-with-mof-code"></a>Erstellen eines gleich geordneten Namespace mit MOF-Code

Eine weitere Möglichkeit zum Erstellen eines Namespace ist die Verwendung von Managed Object Format (MOF)-Code zum Erstellen eines gleich geordneten Namespace. Ein gleich geordneter Namespace ist ein Namespace, der nicht als untergeordnetes Element des aktuellen Namespace vorhanden ist.

Im folgenden Verfahren wird beschrieben, wie ein gleich geordneter Namespace mit MOF-Code erstellt wird.

**So erstellen Sie einen gleich geordneten Namespace mit MOF-Code**

1.  Fügen Sie den [**\# pragma-Namespace**](pragma-namespace.md) -Befehl in den MOF-Code vor der Namespace Deklaration ein.

    Der [**\# pragma-Namespace**](pragma-namespace.md) Befehl weist WMI an, wo die Instanzen nach der-Direktive erstellt werden.

2.  Erstellen Sie eine Instanz der [**\_ \_ Namespace**](--namespace.md) -Klasse.
3.  Kompilieren Sie den Code mit dem Hilfsprogramm [Mofcomp](mofcomp.md) oder der [**imofcompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) -Schnittstelle.

    Weitere Informationen finden Sie unter [Kompilieren von MOF-Dateien](compiling-mof-files.md).

Im folgenden MOF-Codebeispiel wird beschrieben, wie ein Namespace als gleich geordnetes Element des \\ Namespace "root CIMv2" erstellt wird.

``` syntax
#pragma namespace("\\\\.\\Root")

instance of __Namespace 
{
    Name = "MyNamespace";
};
```

 

 



