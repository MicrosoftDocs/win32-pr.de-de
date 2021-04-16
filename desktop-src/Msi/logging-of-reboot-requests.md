---
description: Wenn die InstallValidate-Aktion die Installation einer verwendeten Datei erkennt, wird das Dialog Feld FilesInUse angezeigt, und die folgenden Informationen werden protokolliert.
ms.assetid: 59237d2c-6dda-4edc-bbaf-39c6b4c221b9
title: Protokollierung von Neustart Anforderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a256f9042dc40633932a36e288ad18d8194f4739
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530233"
---
# <a name="logging-of-reboot-requests"></a>Protokollierung von Neustart Anforderungen

Wenn die [InstallValidate-Aktion](installvalidate-action.md) die Installation einer verwendeten Datei erkennt, wird das [Dialog Feld FilesInUse](filesinuse-dialog.md) angezeigt, und die folgenden Informationen werden protokolliert.

``` syntax
Info 1603. The file E:\testdb\Test\CustAct1.dll is being held in use
by the following process: Name: test, Id: 137, Window Title: 'Test'.
```

Wenn das Installationsprogramm erkennt, dass es im Begriff ist, eine Datei zu überschreiben, die verwendet wird, werden die folgenden Informationen protokolliert.

``` syntax
Info 1603. The file E:\testdb\Test\CustAct2.dll is being held in use.

Info 1903.Scheduling reboot operation: Deleting file [filename]. Must 
reboot to complete operation.
```

Das \[ filename- \] Token kann tatsächlich einen Pfad zu einer Datei mit der Erweiterung RBF enthalten. In diesem Fall handelt es sich bei der RBF-Datei tatsächlich um die ursprüngliche Datei, die von der 1603-Nachricht protokolliert wurde, die in die RBF-Datei umbenannt wurde. Die verwendete Datei wird zuerst mit der Erweiterung RBF umbenannt und dann gelöscht.

Wenn Sie weitere Informationen dazu erhalten möchten, warum das Installationsprogramm versucht, diese Datei zu überschreiben, können Sie die Option ausführliche Protokollierung verwenden. Verwenden Sie den ausführlichen installlogmode- \_ Wert in einem [**msienablelog**](/windows/desktop/api/Msi/nf-msi-msienableloga) -aufrufswert, oder verwenden Sie die Option "ausführliche Output" der [Befehlszeilenoptionen](command-line-options.md). Hierdurch werden die folgenden Informationen protokolliert.

``` syntax
MSI (s) (D0:F0): File: E:\testdb\Test\CustAct2.dll;  Overwrite;  
REINSTALLMODE specifies all files to be overwritten
```

Das Protokoll enthält eine Nachricht, z. b. "vorhandene Datei ist eine niedrigere Version" oder "vorhandene Datei ist beschädigt (ungültige Prüfsumme)".

 

 



