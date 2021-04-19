---
title: So entwickeln Sie eine OEM-APP, die eine benutzerdefinierte Datei verwendet
description: Erfahren Sie, wie Sie eine App entwickeln, die eine benutzerdefinierte Datei verwendet, um Informationen vom OEM an die APP zu übergeben.
ms.assetid: BCDB4B13-3644-44E4-9A70-04D8E90500EE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cf60364138a80317e6db8ac4c5d028c36ff540f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "106339474"
---
# <a name="how-to-develop-an-oem-app-that-uses-a-custom-file"></a>So entwickeln Sie eine OEM-APP, die eine benutzerdefinierte Datei verwendet

Weitere Informationen zum Erstellen und Verwenden von benutzerdefinierten Datendateien finden Sie unter [(. AppX-oder appxbundle)-Wartungs Command-Line Optionen](/windows-hardware/manufacture/desktop/dism-app-package--appx-or-appxbundle--servicing-command-line-options).

Erfahren Sie, wie Sie eine App entwickeln, die eine benutzerdefinierte Datei verwendet, um Informationen vom OEM an die APP zu übergeben.

Für apps, die Sie für die OEM-Bereitstellung erstellen, können Sie eine benutzerdefinierte Datei verwenden, um Informationen vom OEM an die apps zu übergeben. Um OEM-Informationen an eine APP zu übergeben, erstellen Sie eine benutzerdefinierte Datendatei im Ordner microsoft.system. Package. Metadata. Der Dateiname ist für das betriebssystemspezifisch und wird bei Betriebssystemupdates automatisch weitergeführt. OEMs können diese Datei verwenden, um benutzerdefinierte Bezeichner zu übergeben, damit apps wissen, wann Sie von OEMs bereitgestellt wurden. Sie können nur eine benutzerdefinierte Datendatei pro APP haben. Apps müssen in der Lage sein, diese Datei ordnungsgemäß zu suchen und zu lesen. Entwickler behandeln die Datei als nicht vertrauenswürdige Daten.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Schnellstart: Abfragen von Informationen zum App-Paket Manifest](how-to-query-package-identity-information.md)

### <a name="prerequisites"></a>Voraussetzungen

-   Sie benötigen das Tool zur [Abbild Verwaltung für die Bereitstellung (Mage)](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) , um das App-Paket mit der benutzerdefinierten Datendatei hinzuzufügen.

## <a name="instructions"></a>Anweisungen

### <a name="step-1-create-custom-file-and-add-it-to-the-package-metadata-folder"></a>Schritt 1: Erstellen Sie eine benutzerdefinierte Datei und fügen Sie Sie dem paketmetadatenordner hinzu

Sie können Ihre APP so entwerfen, dass Sie ein beliebiges Format verwendet, das Sie für benutzerdefinierte Daten auswählen. Beispielsweise können Sie XML, eine Textdatei oder einen anderen Dateityp verwenden, um Ihre Daten zu organisieren. Es wird empfohlen, zu überprüfen, wie Sie die Datei testen und validieren können. Beispielsweise können Sie ein XML-Schema erstellen, um eine XML-Datei zu validieren.

Sie können einen beliebigen Dateityp mit einem beliebigen Dateinamen für die benutzerdefinierten Daten angeben. Wenn Sie das App-Paket mit der benutzerdefinierten Datendatei mithilfe des [Tools zum](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) renderingtool hinzufügen, benennt das-Objekt die benutzerdefinierte Datei in "Custom. Data" um und speichert die Datei im Ordner "microsoft.system. Package. Metadata".

> [!Note]  
> Die benutzerdefinierte Datendatei kann nicht von der APP geändert werden. Es handelt sich um eine schreibgeschützte Ressource.

 

### <a name="step-2-access-the-custom-data-file-for-an-app"></a>Schritt 2: Zugreifen auf die benutzerdefinierte Datendatei für eine APP

Sie können auf die benutzerdefinierte. Data-Datei für eine APP aus Ihrem Code zugreifen, indem Sie Windows-APIs verwenden, um Informationen für das aktuelle Paket zu erhalten. Beispiel:

``` syntax
Windows.ApplicationModel.Package.current.installedLocation.getFileAsync(
"microsoft.system.package.metadata\\custom.data")
```

Weitere Informationen zum Entwickeln mit der " [**Package. Current**](/uwp/api/windows.applicationmodel.package.current) "-Eigenschaft finden Sie unter [Schnellstart: Abfragen von App-Paket Manifest-Informationen](how-to-query-package-identity-information.md).

Weitere Informationen über den Zugriff auf die benutzerdefinierte Datendatei über [**istoragefolder. getfileasync**](/uwp/api/windows.storage.istoragefolder.getfileasync) und die Verwendung von [**storagefile**](/uwp/api/Windows.Storage.StorageFile) -Objekten finden Sie unter [zugreifen auf Daten und Dateien](/previous-versions/windows/apps/hh464959(v=win.10)).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schnellstart: Abfragen von Informationen zum App-Paket Manifest](how-to-query-package-identity-information.md)
</dt> </dl>

 

 