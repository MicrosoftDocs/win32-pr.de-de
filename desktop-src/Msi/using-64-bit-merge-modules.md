---
description: Befolgen Sie diese Richtlinien, wenn Sie ein 64-Bit-Mergemodul erstellen.
ms.assetid: 326c274b-981e-4b21-a4fb-0060c178a01e
title: Verwenden von 64-Bit-Mergemodulen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2bfeec3f77e497fac0686cd6aeb44b69e987655
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757806"
---
# <a name="using-64-bit-merge-modules"></a>Verwenden von 64-Bit-Mergemodulen

Ein 64-Bit-Mergemodul hat eine der in diesem Thema identifizierten Merkmale.

-   Das Mergemodul enthält mindestens eine Komponente, die für 64-Bit-Betriebssysteme kompiliert wurde.
-   Das Mergemodul enthält keine 64-Bit-Komponenten, sondern ist nur für die Verwendung mit [64-Bit-Windows Installer](64-bit-windows-installer-packages.md) Paketen vorgesehen.

Mergemodule können wie folgt verwendet werden:

-   Ein 64-Bit-Mergemodul kann in ein [64-Bit-Windows Installer](64-bit-windows-installer-packages.md) Paket zusammengeführt werden. Die [**Vorlagen Zusammenfassungs**](template-summary.md) Eigenschaften im Mergemodul und im Windows Installer Paket müssen auf denselben Typ von 64-Bit-Prozessor festgelegt werden. Ein x64-Mergemodul kann nur in x64-Paketen zusammengeführt werden, und ein Intel64 Merge-Modul kann nur in Intel64-Paketen zusammengeführt werden.
-   Ein 32-Bit-Mergemodul kann mit 32-Bit-oder [64-Bit-Windows Installer](64-bit-windows-installer-packages.md) Paketen zusammengeführt werden.
-   Ein 64-Bit-Mergemodul kann in einem 64-Bit-Paket unter einem 32-Bit-Betriebssystem zusammengeführt werden.

Beachten Sie beim Erstellen eines 64-Bit-Mergemoduls Folgendes:

-   Verwenden Sie das gleiche allgemeine Verfahren wie beim Erstellen von 32-Bit-Mergemodulen. Weitere Informationen finden Sie unter Informationen [zu Mergemodulen](about-merge-modules.md) und zum [Erstellen von Mergemodulen](authoring-merge-modules.md).
-   Wenn ein Intel64-System ausgeführt wird, müssen Sie die Eigenschaft [**Vorlagen Zusammenfassung**](template-summary.md) mit dem Wert Intel64 festlegen. Wenn Sie ein x64-System ausführen, müssen Sie die Eigenschaft **Vorlagen Zusammenfassung** mit dem x64-Wert festlegen. Weitere Informationen finden Sie unter [Zusammenfassungs Datenstrom Referenz für Zusammenfassungs Modul](merge-module-summary-information-stream-reference.md).
-   Wenn sowohl 32-Bit-als auch 64-Bit-Mergemodule für dieselbe Komponente vorhanden sind, wird empfohlen, dass die Module unterschiedliche Signaturen aufweisen. Dadurch kann ein Paket beide Versionen der Komponente enthalten.

Weitere Informationen finden Sie unter [Windows Installer auf 64-Bit-Betriebssystemen](windows-installer-on-64-bit-operating-systems.md).

 

 



