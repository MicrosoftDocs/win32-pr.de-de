---
description: Die folgende Abbildung veranschaulicht, wie zwei Anwendungen eine Assembly mithilfe der herkömmlichen Methode der Assemblyfreigabe gemeinsam nutzen können.
ms.assetid: 2b9c6511-ae79-498f-a20c-ccb32a623d42
title: Gemeinsames Freigeben von Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59dcfbb40040b51fc2e17d3707d4a76c7ea5ddadf1806e41b7a7fbd81860ae15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141813"
---
# <a name="side-by-side-assembly-sharing"></a>Gemeinsames Freigeben von Assemblys

Die folgende Abbildung veranschaulicht, wie zwei Anwendungen eine Assembly mithilfe der herkömmlichen Methode der Assemblyfreigabe gemeinsam nutzen können. Ein Problem bei der herkömmlichen Assemblyfreigabe tritt auf, wenn eine Anwendung eine Version einer Assembly installiert , häufig eine DLL, die nicht abwärtskompatibel ist. Die soeben installierte Anwendung funktioniert, aber Anwendungen, die von der vorherigen DLL-Version abhängig waren, funktionieren möglicherweise nicht mehr.

![Darstellung von zwei Anwendungen, die eine Assembly gemeinsam nutzen](images/sxs1.png)

Die isolierte Anwendung und die projektmappe für die gleichzeitige Assembly ermöglichen es, dass verschiedene Versionen derselben Win32-Assembly ohne Konflikte gleichzeitig auf demselben System ausgeführt werden. Durch Die Angabe der von der Anwendung zu verwendenden version der nebenseitigen Assembly können Entwickler garantieren, dass die konfiguration, die sie testen, immer auf dem Computer des Benutzers dupliziert wird. Die gemeinsame Nutzung wird in der folgenden Abbildung veranschaulicht.

![Implementierung der gemeinsamen Assemblyfreigabe](images/sxs2.png)

Weitere Informationen finden Sie unter [Informationen zu isolierten Anwendungen und nebenseitigen Assemblys.](about-isolated-applications-and-side-by-side-assemblies.md)

 

 



