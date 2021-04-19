---
description: Die folgenden Datenbankfunktionen müssen nie von einer benutzerdefinierten Aktion aufgerufen werden.
ms.assetid: 55fdd82b-9f34-4c2c-a837-8a09f21f568a
title: Funktionen, die nicht für benutzerdefinierte Aktionen verwendet werden können
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c77c4714ca65614200cf77d6b207b6eebcaf179
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349504"
---
# <a name="functions-not-for-use-in-custom-actions"></a>Funktionen, die nicht für benutzerdefinierte Aktionen verwendet werden können

Die folgenden [Datenbankfunktionen](database-functions.md) müssen nie von einer benutzerdefinierten Aktion aufgerufen werden.

-   [**Msikonfigurireproduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)
-   [**Msikonfigurireproduktions-ctex**](/windows/desktop/api/Msi/nf-msi-msiconfigureproductexa)
-   [**Msikreatetransformsummaryinfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)
-   [**Msidatabaseapplytransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma)
-   [**Msidatabasecommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)
-   [**Msidatabaseexport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)
-   [**Msidatabasegeneratetransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)
-   [**Msidatabaseimport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)
-   [**Msidatabasemerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea)
-   [**Msienablelog**](/windows/desktop/api/Msi/nf-msi-msienableloga)
-   [**Msienableuipreview**](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview)
-   [**Msigetdatabasestate**](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate)
-   [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea)
-   [**Msipreviewbillboard**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewbillboarda)
-   [**Msipreviewdialog**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewdialoga)
-   [**Msireinstallproduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)
-   [**Msiseeltexternalui**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
-   [**Msiseeltexternaluirecord**](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord)
-   [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)

Die folgenden [Installer-Funktionen](installer-function-reference.md) müssen nie von einer benutzerdefinierten Aktion aufgerufen werden.

-   [**Msiapplypatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)
-   [**Msicollectuserinfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa)
-   [**Msikonfigurierfeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea)
-   [**Msikonfigurireproduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)
-   [**Msikonfigurireproduktions-ctex**](/windows/desktop/api/Msi/nf-msi-msiconfigureproductexa)
-   [**Msienablelog**](/windows/desktop/api/Msi/nf-msi-msienableloga)
-   [**Msigetfeatureinfo**](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa)
-   [**Msigetproductcode**](/windows/desktop/api/Msi/nf-msi-msigetproductcodea)
-   [**Msigetproductproperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya)
-   [**Msiinstallmissingcomponent**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta)
-   [**Msiinstallmissingfile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea)
-   [**Msiinstallproduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)
-   [**Msiopenpackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea)
-   [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta)
-   [**Msireinstallfeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)
-   [**Msireinstallproduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)
-   [**Msiseeltexternalui**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
-   [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)
-   [**Msiusefeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea)
-   [**Msiusefeatureex**](/windows/desktop/api/Msi/nf-msi-msiusefeatureexa)
-   [**Msiverifypackage**](/windows/desktop/api/Msi/nf-msi-msiverifypackagea)

Die folgenden [Installer-Funktionen](installer-function-reference.md) müssen nie von einer benutzerdefinierten Aktion aufgerufen werden, wenn eine andere Installation gestartet wird. Sie können von einer benutzerdefinierten Aktion aufgerufen werden, die keine andere Installation startet.

-   [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)
-   [**Msiprovidequalifiedcomponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta)
-   [**Msiprovide qualifiedcomponumtex**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa)

Eine benutzerdefinierte Aktion sollte nie einen neuen Thread erzeugen, der Windows Installer Funktionen verwendet, um den Funktionsstatus, den Komponenten Status oder das Senden von Nachrichten von einem Steuerungs Ereignis zu ändern. Wenn Sie versuchen, dies zu tun, schlägt die Installation fehl.

 

 



