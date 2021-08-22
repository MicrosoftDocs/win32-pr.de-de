---
title: Aufzählen von Ressourcen
description: In diesem Thema werden die Funktionen erläutert, die zum Abrufen von Ressourcenlisten verwendet werden.
ms.assetid: 388deaa1-3b04-43fa-aad2-8b52376d570c
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 6d3fbe60e3013fbeabdb21d74999040b51c42be2a1bb4521cda28a976bfe7aa5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034338"
---
# <a name="enumerating-resources"></a>Aufzählen von Ressourcen

In bestimmten Situationen sollten Sie den Ressourceninhalt eines unbekannten PE-Moduls (Portable Executable) entdecken. Das Windows SDK stellt Ressourcenenumerationsfunktionen bereit, mit denen Ihre Anwendung Listen mit Ressourcentypen, Namen und Sprachen in einem angegebenen Modul abrufen kann.

* Die [**Funktionen EnumResourceTypeW**](/windows/win32/api/Winbase/nf-winbase-enumresourcetypesw) und [**EnumResourceTypesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcetypesexw) stellen eine Liste der Ressourcentypen im Modul zur Verfügung.
* Die [**Funktionen EnumResourceNamesW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesw) und [**EnumResourceNamesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesexw) geben den Namen jeder Ressource innerhalb eines bestimmten Typs an.
* Die [**Funktionen EnumResourceLanguagesW**](/windows/win32/api/Winbase/nf-winbase-enumresourcelanguagesw) und [**EnumResourceLanguagesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcelanguagesexw) stellen die Sprache jeder Ressource mit einem bestimmten Namen und Typ zur Verfügung. 

Mit diesen Funktionen und den zugehörigen Rückruffunktionen kann Ihre Anwendung eine Liste aller Ressourcen in einem Modul erstellen. Dieser Prozess wird unter [Erstellen einer Ressourcenliste beschrieben.](using-resources.md)

## <a name="-see-also"></a>-see-also

[Msistuff.exe-Beispiel-App](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/sysmgmt/msi/msistuff)
