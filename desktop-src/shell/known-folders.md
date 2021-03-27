---
description: Mit Windows Vista werden neue Speicher Szenarien und ein neuer Namespace für Benutzerprofile eingeführt.
title: Bekannte Ordner
ms.topic: article
ms.date: 05/31/2018
ms.assetid: d0c25eef-53ac-4dad-805a-b9ba4cd86be9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7527b7242c68f0d6c78cd0fae427626c182302f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980241"
---
# <a name="known-folders"></a>Bekannte Ordner

Mit Windows Vista werden neue Speicher Szenarien und ein neuer Namespace für Benutzerprofile eingeführt. Um diese neuen Faktoren zu beheben, wurde das ältere System, das über einen [**CSIDL**](csidl.md) -Wert auf Standardordner verweist, ersetzt. Ab Windows Vista wird auf diese Ordner durch einen neuen Satz von GUID-Werten verwiesen, die als bekannte Ordner-IDs bezeichnet werden.

Das bekannte Ordnersystem bietet folgende Vorteile:

-   Unabhängige Softwarehersteller (ISVs) können den Satz bekannter Ordner-IDs mit eigenen Erweiterungen erweitern. Sie können Ordner definieren, Ihnen IDs zuordnen und Sie beim System registrieren. CSIDL-Werte konnten nicht erweitert werden.
-   Alle bekannten Ordner auf einem System können aufgelistet werden. Diese Funktionalität für CSIDL-Werte wurde von keiner API bereitgestellt. Weitere Informationen finden Sie unter [**iknownfoldermanager:: getfolderids**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids) .
-   Ein bekannter Ordner, der von einem ISV hinzugefügt wird, kann benutzerdefinierte Eigenschaften hinzufügen, mit denen er den Zweck und die beabsichtigte Verwendung erläutern kann.
-   Viele bekannte Ordner können an neue Speicherorte umgeleitet werden, einschließlich Netzwerkadressen. Unter dem CSIDL-System konnte nur der Ordner " **Eigene Dokumente** " umgeleitet werden.
-   Bekannte Ordner können benutzerdefinierte Handler für die Verwendung während der Erstellung oder Löschung enthalten.

Das CSIDL-System und APIs, die CSIDL-Werte verwenden, werden weiterhin aus Kompatibilitätsgründen unterstützt. Es wird jedoch nicht empfohlen, diese in einer neuen Entwicklung zu verwenden.


In den folgenden Themen werden die Besonderheiten des Systems "bekannte Ordner" erläutert.

-   [Arbeiten mit bekannten Ordnern in Anwendungen](working-with-known-folders.md)
-   [Erweitern bekannter Ordner mit benutzerdefinierten Ordnern](how-to-extend-known-folders-with-custom-folders.md)
-   [**KNOWNFOLDERID**](knownfolderid.md)

Auf den folgenden Referenzseiten werden die Funktionen von Win32-Funktionen für bekannte Ordner erläutert, die zum Abrufen des Speicher Orts bekannter Ordner oder zum Umleiten an einen neuen Speicherort verwendet werden können. Diese Funktionen ersetzen ältere Win32-Funktionen. Die neuen Funktionen werden bereitgestellt, um den alten Funktionen ein entsprechendes Verhalten zu bieten, aber jede neue Funktion wird auch durch eine Component Object Model (com)-API dupliziert.



| Neue Funktion                                             | Arbeits                                           | COM-Äquivalent                                            |
|----------------------------------------------------------|----------------------------------------------------|-----------------------------------------------------------|
| [**Shgetknownfolderpath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath)     | [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha)         | [**Iknownfolder:: getpath**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getpath)     |
| [**Shgetknownfolderidlist**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist) | [**Shgetfolderlocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) | [**Iknownfolder:: getidlist**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getidlist) |
| [**Shsetknownfolderpath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetknownfolderpath)     | [**Shsetfolderpath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetfolderpatha)         | [**Iknownfolder:: setpath**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-setpath)     |



 

Die folgenden Referenzseiten erläutern die COM-APIs für bekannte Ordner, die die gesamte Funktionalität der oben aufgeführten Win32-APIs bereitstellen, sowie die Möglichkeit, alle bekannten Ordner aufzulisten, auf bekannte Ordnereigenschaften zuzugreifen und den Standardsatz bekannter Ordner zu erweitern.

-   [**Iknownfolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder)
-   [**Iknownfoldermanager**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager)

Im Windows Software Development Kit (SDK) ist ein C++-Beispiel enthalten, das die APIs bekannter Ordner veranschaulicht. Nachdem Sie die Windows SDK auf Ihrem Computer installiert haben, finden Sie das Beispiel unter% Program Files% \\ Microsoft \\ \\ sdgs Windows v 6.0 \\ Samples \\ WinUI \\ Shell \\ appplatform \\ KnownFolders.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bekannte Ordner (Beispiel)](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))
</dt> </dl>

 

 
