---
title: Entwickeln einer OEM-App, die eine benutzerdefinierte Datei verwendet
description: Erfahren Sie, wie Sie eine App entwickeln, die eine benutzerdefinierte Datei verwendet, um Informationen vom OEM an die App zu übergeben.
ms.assetid: BCDB4B13-3644-44E4-9A70-04D8E90500EE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4780e930d057c325038c94dc86fc375c70bdb1cc8dca34ac6169436bc0f0e323
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855320"
---
# <a name="how-to-develop-an-oem-app-that-uses-a-custom-file"></a>Entwickeln einer OEM-App, die eine benutzerdefinierte Datei verwendet

Weitere Informationen zum Erstellen und Verwenden benutzerdefinierter Datendateien finden Sie unter [DISM App Package (.appx or .appxbundle) Servicing Command-Line Options (Dism-App-Paket (.appx oder .appxbundle)) Servicing Command-Line Options](/windows-hardware/manufacture/desktop/dism-app-package--appx-or-appxbundle--servicing-command-line-options)( .

Erfahren Sie, wie Sie eine App entwickeln, die eine benutzerdefinierte Datei verwendet, um Informationen vom OEM an die App zu übergeben.

Für Apps, die Sie für die OEM-Bereitstellung erstellen, können Sie eine benutzerdefinierte Datei verwenden, um Informationen vom OEM an die Apps zu übergeben. Um OEM-Informationen an eine App zu übergeben, erstellen Sie eine Custom.data-Datei im ordner microsoft.system.package.metadata. Dieser Dateiname gilt speziell für das Betriebssystem und wird automatisch während Betriebssystemupdates weiter ausgeführt. OEMs können diese Datei verwenden, um benutzerdefinierte Bezeichner zu übergeben, damit Apps wissen, wann OEMs sie bereitgestellt haben. Sie können nur eine Custom.data-Datei pro App verwenden. Apps müssen in der Lage sein, diese Datei ordnungsgemäß zu suchen und zu lesen. Entwickler behandeln die Datei als nicht vertrauenswürdige Daten.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Schnellstart: Abfragen von App-Paketmanifestinformationen](how-to-query-package-identity-information.md)

### <a name="prerequisites"></a>Voraussetzungen

-   Sie benötigen das [Abbildverwaltung für die Bereitstellung (DISM),](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) um das App-Paket mit der benutzerdefinierten Datendatei hinzuzufügen.

## <a name="instructions"></a>Anweisungen

### <a name="step-1-create-custom-file-and-add-it-to-the-package-metadata-folder"></a>Schritt 1: Erstellen einer benutzerdefinierten Datei und Hinzufügen zum Paketmetadatenordner

Sie können Ihre App so entwerfen, dass sie ein beliebiges Format verwendet, das Sie für die benutzerdefinierten Daten auswählen. Beispielsweise können Sie XML, eine Textdatei oder einen anderen Dateityp verwenden, um Ihre Daten zu organisieren. Es wird empfohlen, zu überlegen, wie Sie die Datei testen und überprüfen können. Beispielsweise können Sie ein XML-Schema erstellen, um eine XML-Datei zu überprüfen.

Sie können einen beliebigen Dateityp mit einem beliebigen Dateinamen für die benutzerdefinierten Daten angeben. Wenn Sie das App-Paket mit der benutzerdefinierten Datendatei mithilfe des [DISM-Tools](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) hinzufügen, benennt DISM die benutzerdefinierte Datei in Custom.data um und speichert die Datei im Ordner microsoft.system.package.metadata.

> [!Note]  
> Die benutzerdefinierte Datendatei kann von der App nicht geändert werden. Es ist eine schreibgeschützte Ressource.

 

### <a name="step-2-access-the-custom-data-file-for-an-app"></a>Schritt 2: Zugreifen auf die benutzerdefinierte Datendatei für eine App

Sie können über Ihren Code auf die Datei Custom.data für eine App zugreifen, indem Sie Windows-APIs verwenden, um Informationen für das aktuelle Paket zu erhalten. Beispiel:

``` syntax
Windows.ApplicationModel.Package.current.installedLocation.getFileAsync(
"microsoft.system.package.metadata\\custom.data")
```

Weitere Informationen zum Entwickeln mit der [**Package.Current-Eigenschaft finden**](/uwp/api/windows.applicationmodel.package.current) Sie unter [Schnellstart: Abfragen von App-Paketmanifestinformationen.](how-to-query-package-identity-information.md)

Weitere Informationen zum Zugreifen auf die Datei custom.data über [**IStorageFolder.GetFileAsync**](/uwp/api/windows.storage.istoragefolder.getfileasync) und mithilfe von [**StorageFile-Objekten**](/uwp/api/Windows.Storage.StorageFile) finden Sie unter [Zugreifen auf Daten und Dateien.](/previous-versions/windows/apps/hh464959(v=win.10))

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schnellstart: Abfragen von App-Paketmanifestinformationen](how-to-query-package-identity-information.md)
</dt> </dl>

 

 