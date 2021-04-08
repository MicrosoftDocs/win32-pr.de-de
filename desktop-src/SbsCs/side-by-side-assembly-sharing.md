---
description: In der folgenden Abbildung wird veranschaulicht, wie zwei Anwendungen eine Assembly mit der herkömmlichen Methode der assemblyfreigabe gemeinsam verwenden können.
ms.assetid: 2b9c6511-ae79-498f-a20c-ccb32a623d42
title: Parallele assemblyfreigabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a94295baf2c29733c0ec366f9476a4dbf5cc3f40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960551"
---
# <a name="side-by-side-assembly-sharing"></a>Parallele assemblyfreigabe

In der folgenden Abbildung wird veranschaulicht, wie zwei Anwendungen eine Assembly mit der herkömmlichen Methode der assemblyfreigabe gemeinsam verwenden können. Ein Problem mit der herkömmlichen assemblyfreigabe tritt auf, wenn eine Anwendung eine Version einer Assembly installiert – üblicherweise eine DLL –, die nicht abwärts kompatibel ist. Die soeben installierte Anwendung funktioniert, aber Anwendungen, die von der vorherigen dll-Version abhängen, funktionieren möglicherweise nicht mehr.

![Darstellung von zwei Anwendungen, die eine Assembly gemeinsam nutzen](images/sxs1.png)

Mit der isolierten Anwendung und der parallelen Assemblylösung können unterschiedliche Versionen der gleichen Win32-Assembly gleichzeitig auf demselben System ausgeführt werden, ohne dass es zu einem Konflikt kommt. Durch Angeben der parallelen Assemblyversion, die von der Anwendung verwendet werden soll, können Entwickler sicherstellen, dass die von Ihnen getestete Konfiguration immer auf dem Computer des Benutzers dupliziert wird. Die parallele Freigabe wird in der folgenden Abbildung veranschaulicht.

![Implementierung der parallelen assemblyfreigabe](images/sxs2.png)

Weitere Informationen finden Sie unter Informationen [zu isolierten Anwendungen und](about-isolated-applications-and-side-by-side-assemblies.md)parallelen Assemblys.

 

 



