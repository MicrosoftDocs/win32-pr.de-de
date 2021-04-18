---
description: Sie können ganze Produkte mit Windows Installer Funktionen installieren. In den folgenden Schritten wird beschrieben, wie Sie ein Produkt installieren.
ms.assetid: 03cc7abc-63bd-4a01-a05c-9f7928de8827
title: Installieren einer Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cf312e7394c4fcbca699f6e032e315a42356c1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352273"
---
# <a name="installing-an-application"></a>Installieren einer Anwendung

Sie können ganze Produkte mit Windows Installer Funktionen installieren. In den folgenden Schritten wird beschrieben, wie Sie ein Produkt installieren.

**So installieren Sie ein Produkt**

1.  Führen Sie ein Produkt durch die Installation oder die Deinstallier Sequenz aus, indem Sie die [**msiinstallproduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) -Funktion aufrufen.
2.  Geben Sie die Installations Ebene an, indem Sie die [**msikonfigurireproduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta) -Funktion aufrufen.

    Sie können die Parameter der [**msikonfigurireproduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta) -Funktion verwenden, um den Installationsstatus festzulegen. Beispielsweise können Sie den Status für die lokale Installation festlegen oder die Installation über die Quelle durchsetzen. Sie können den Bereich von Produktfunktionen festlegen, die eingeschlossen werden sollen, indem Sie die Ebene festlegen.

Weitere Informationen zum Installieren einer Anwendung finden Sie unter [Resilienz](resiliency.md) und [Installationsmechanismus](installation-mechanism.md).

 

 



