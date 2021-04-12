---
description: Sie können das kleine Update auf eine lokale Installation von MNP2000 mit dem Beispiel Patch mnppatch. msp anwenden, der beim Erstellen eines Patchpakets erstellt wurde.
ms.assetid: 928182ae-5ddb-446f-a9b8-e8b3aa4ce49c
title: Anwenden eines Patchpakets auf eine lokale Installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a09ca0372870d46db67b49c0571045aadabf54c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215721"
---
# <a name="applying-a-patch-package-to-a-local-installation"></a>Anwenden eines Patchpakets auf eine lokale Installation

Sie können das kleine Update auf eine lokale Installation von MNP2000 mit dem Beispiel Patch mnppatch. msp anwenden, der beim [Erstellen eines Patchpakets](generating-a-patch-package.md)erstellt wurde. Das allgemeine Verfahren wird im Abschnitt Anwenden von [kleinen Updates durch Patchen der lokalen Installation des Produkts](applying-small-updates-by-patching-the-local-installation-of-the-product.md)erläutert.

Installieren Sie das ursprüngliche MNP2000-Produkt lokal auf Ihrem Computer. Vergewissern Sie sich, dass die Fehlermeldung Concert.txt, die durch das kleine Update behoben werden muss. Starten Sie als nächstes die Installation, indem Sie die folgende Befehlszeile eingeben.

**msiexec/p MNP2000. msp REINSTALL = ALL REINSTALLMODE = omus**

Überprüfen Sie die Concert.txt zu "MNP2000", um sicherzustellen, dass das Installationsprogramm das kleine Update angewendet hat, um diese Datei zu korrigieren.

Informationen zum Anwenden des kleinen Updates auf ein administratives Image finden Sie unter [Anwenden eines Patchpakets auf eine administrative Installation](applying-a-patch-package-to-an-administrative-installation.md).

[Fortsetzen](applying-a-patch-package-to-an-administrative-installation.md)

 

 



