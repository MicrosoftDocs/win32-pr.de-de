---
description: Windows Vista führt neue Speicherszenarien und einen neuen Benutzerprofilnamespace ein.
title: Bekannte Ordner
ms.topic: article
ms.date: 05/31/2018
ms.assetid: d0c25eef-53ac-4dad-805a-b9ba4cd86be9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: cd44bfe1090f25cb93d8a6fa8162901eb730a53cfb9dfec7ae3f1986fa65e1db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118720409"
---
# <a name="known-folders"></a>Bekannte Ordner

Windows Vista führt neue Speicherszenarien und einen neuen Benutzerprofilnamespace ein. Um diese neuen Faktoren zu berücksichtigen, wurde das ältere System des Verweises auf Standardordner durch einen [**CSIDL-Wert**](csidl.md) ersetzt. Ab Windows Vista wird auf diese Ordner durch einen neuen Satz von GUID-Werten verwiesen, die als Bekannte Ordner-IDs bezeichnet werden.

Das System für bekannte Ordner bietet die folgenden Vorteile:

-   Unabhängige Softwarehersteller (Independent Software Vendors, ISVs) können den Satz bekannter Ordner-IDs um ihre eigenen erweitern. Sie können Ordner definieren, ihnen IDs geben und sie beim System registrieren. CSIDL-Werte konnten nicht erweitert werden.
-   Alle bekannten Ordner in einem System können aufzählt werden. Diese Funktionalität für CSIDL-Werte wurde nicht von der API bereitgestellt. Weitere Informationen finden Sie unter [**IKnownFolderManager::GetFolderIds.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids)
-   Ein bekannter Ordner, der von einem ISV hinzugefügt wird, kann benutzerdefinierte Eigenschaften hinzufügen, mit denen der Zweck und die beabsichtigte Verwendung erläutert werden können.
-   Viele bekannte Ordner können an neue Speicherorte umgeleitet werden, einschließlich Netzwerkadressen. Unter dem CSIDL-System konnte nur der **ordner Eigene Dokumente** umgeleitet werden.
-   Bekannte Ordner können benutzerdefinierte Handler für die Verwendung während der Erstellung oder Löschung aufweisen.

Das CSIDL-System und die APIs, die CSIDL-Werte verwenden, werden aus Kompatibilitätsgründen weiterhin unterstützt. Es wird jedoch nicht empfohlen, sie in einer neuen Entwicklung zu verwenden.


In den folgenden Themen werden die Besonderheiten des Systems für bekannte Ordner erörtert.

-   [Arbeiten mit bekannten Ordnern in Anwendungen](working-with-known-folders.md)
-   [Erweitern bekannter Ordner mit benutzerdefinierten Ordnern](how-to-extend-known-folders-with-custom-folders.md)
-   [**KNOWNFOLDERID**](knownfolderid.md)

Auf den folgenden Referenzseiten werden die Win32-Funktionen für bekannte Ordner erläutert, die verwendet werden können, um den Speicherort bekannter Ordner abzurufen oder sie an einen neuen Speicherort umzuleiten. Diese Funktionen ersetzen ältere Win32-Funktionen. Die neuen Funktionen werden bereitgestellt, um den alten Funktionen ein gleichwertiges Verhalten zu bieten, aber jede neue Funktion wird auch von einer Component Object Model-API (COM) dupliziert.



| Neue Funktion                                             | Ersetzt                                           | COM-Entsprechung                                            |
|----------------------------------------------------------|----------------------------------------------------|-----------------------------------------------------------|
| [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath)     | [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha)         | [**IKnownFolder::GetPath**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getpath)     |
| [**SHGetKnownFolderIDList**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist) | [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) | [**IKnownFolder::GetIDList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getidlist) |
| [**SHSetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetknownfolderpath)     | [**SHSetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetfolderpatha)         | [**IKnownFolder::SetPath**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-setpath)     |



 

Auf den folgenden Referenzseiten werden die COM-APIs für bekannte Ordner erläutert, die alle Funktionen der oben aufgeführten Win32-APIs bereitstellen, sowie die Möglichkeit hinzufügen, alle bekannten Ordner aufzuzählen, auf Eigenschaften von bekannten Ordnern zuzugreifen und den Standardsatz bekannter Ordner zu erweitern.

-   [**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder)
-   [**IKnownFolderManager**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager)

Ein C++-Beispiel, das die APIs für bekannte Ordner veranschaulicht, ist im Windows Software Development Kit (SDK) enthalten. Nachdem Sie das Windows SDK auf Ihrem Computer installiert haben, finden Sie das Beispiel unter %ProgramFiles% \\ Microsoft SDKs \\ Windows \\ v6.0 \\ Samples \\ WinUI Shell \\ \\ AppPlatform \\ KnownFolders.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bekannte Ordner (Beispiel)](/windows/win32/shell/samples-knownfolders)
</dt> </dl>
