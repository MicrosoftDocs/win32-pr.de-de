---
description: Die Produktdatenbank enthält Informationen zu einem Produkt. Weitere Informationen zum Abrufen von Produktinformationen mit Enumerationsfunktionen finden Sie unter Initialisieren einer Anwendung.
ms.assetid: 528c915c-296c-4620-8105-0b5d543e56a5
title: Anwendungsinformationen werden erhalten.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2dce842f057efb65b6d0db3ad0407a19bf08435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959269"
---
# <a name="getting-application-information"></a>Anwendungsinformationen werden erhalten.

Die Produktdatenbank enthält Informationen zu einem Produkt. Weitere Informationen zum Abrufen von Produktinformationen mit Enumerationsfunktionen finden Sie unter [Initialisieren einer Anwendung](initializing-an-application.md).

**So erhalten Sie Produktinformationen**

1.  Überprüfen Sie, ob ein Produkt installiert ist, indem Sie die [**msiqueryproductstate**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea) -Funktion aufrufen.
2.  Öffnen Sie die Datenbank, und rufen Sie ein Handle dafür ab, indem Sie die [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) -Funktion aufrufen.

    Wenn die Datenbank in einem Installationspaket enthalten ist, müssen Sie die Funktion [**msiopenpackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea) aufzurufen.

3.  Verwenden Sie das offene Handle zum Abrufen von Produkteigenschaften mit der [**msigetproductproperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya) -Funktion und zum Abrufen beschreibender Funktions Informationen mit der [**msigetfeatureinfo**](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa) -Funktion.

    Wenn Sie Produktinformationen mithilfe des Produktcodes abrufen möchten, anstatt das geöffnete Daten Bank Handle zu verwenden, rufen Sie die [**msigetproductinfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa) -Funktion anstelle von " [**msigetproductproperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya)" auf.

4.  Schließen Sie ein geöffnetes Installations handle, indem Sie die [**msiclosehandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle) -Funktion aufrufen.

    Die [**msicloseallhandles**](/windows/desktop/api/Msi/nf-msi-msicloseallhandles) -Funktion ist eine Diagnosefunktion und sollte nicht verwendet werden, um die zu öffnenden Handles zu schließen. Es ist zulässig, die **msicloseallhandles** -Funktion aufzurufen, wenn die Anwendung geschlossen wird, um sicherzustellen, dass alle Handles geschlossen wurden.

 

 



