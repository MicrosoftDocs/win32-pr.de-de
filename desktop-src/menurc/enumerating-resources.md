---
title: Aufzählen von Ressourcen
description: In diesem Thema werden die Funktionen erläutert, die zum Abrufen von Ressourcenlisten verwendet werden.
ms.assetid: 388deaa1-3b04-43fa-aad2-8b52376d570c
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: b978636303f3fc5bcae8c1d854289dde42ae0247
ms.sourcegitcommit: 78ce1d1e3f12ee3e08390868e5b93c034f437657
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/10/2021
ms.locfileid: "111910269"
---
# <a name="enumerating-resources"></a>Aufzählen von Ressourcen

In bestimmten Situationen sollten Sie den Ressourceninhalt eines unbekannten PE-Moduls (Portable Executable) ermitteln. Der Windows SDK stellt Ressourcenenumerationsfunktionen bereit, mit denen Ihre Anwendung Listen von Ressourcentypen, Namen und Sprachen in einem angegebenen Modul abrufen kann.

* Die Funktionen [**EnumResourceTypeW**](/windows/win32/api/Winbase/nf-winbase-enumresourcetypesw) und [**EnumResourceTypesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcetypesexw) stellen eine Liste der Ressourcentypen im Modul bereit.
* Die Funktionen [**EnumResourceNamesW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesw) und [**EnumResourceNamesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesexw) geben den Namen jeder Ressource innerhalb eines bestimmten Typs an.
* Die Funktionen [**EnumResourceLanguagesW**](/windows/win32/api/Winbase/nf-winbase-enumresourcelanguagesw) und [**EnumResourceLanguagesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcelanguagesexw) stellen die Sprache jeder Ressource mit einem bestimmten Namen und Typ bereit. 

Diese Funktionen und die zugehörigen Rückruffunktionen ermöglichen Es Ihrer Anwendung, eine Liste aller Ressourcen in einem Modul zu erstellen. Dieser Prozess wird unter [Erstellen einer Ressourcenliste](using-resources.md)beschrieben.

## <a name="-see-also"></a>-see-also

[Msistuff.exe Beispiel-App](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/sysmgmt/msi/msistuff)
