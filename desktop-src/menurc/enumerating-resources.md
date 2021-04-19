---
title: Auflisten von Ressourcen
description: In diesem Thema werden die Funktionen erläutert, die zum Abrufen von Listen mit Ressourcen verwendet werden.
ms.assetid: 388deaa1-3b04-43fa-aad2-8b52376d570c
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: ea7f2600f6da98cff6f16853092004a542b0f206
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/20/2021
ms.locfileid: "106367509"
---
# <a name="enumerating-resources"></a>Auflisten von Ressourcen

In bestimmten Situationen möchten Sie möglicherweise den Ressourcen Inhalt eines unbekannten PE-Moduls (Portable portable ausführbare Datei) ermitteln. Der Windows SDK stellt ressourcenenumerationsfunktionen bereit, mit denen Ihre Anwendung Listen mit Ressourcentypen, Namen und Sprachen in einem angegebenen Modul abrufen kann.

* Die Funktionen [**enumresourcetypew**](/windows/win32/api/Winbase/nf-winbase-enumresourcetypesw) und [**enumresourcetypesexw**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcetypesexw) stellen eine Liste von Ressourcentypen bereit, die im Modul enthalten sind.
* Die Funktionen " [**enumresourcenamesw**](/windows/win32/api/Winbase/nf-winbase-enumresourcenamesw) " und " [**enumresourcenamesexw**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesexw) " geben den Namen der einzelnen Ressourcen innerhalb eines bestimmten Typs an.
* Die Funktionen " [**enumresourcelanguagesw**](/windows/win32/api/Winbase/nf-winbase-enumresourcelanguagesw) " und " [**enumresourcelanguagesexw**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcelanguagesexw) " stellen die Sprache der einzelnen Ressourcen eines bestimmten Namens und Typs bereit. 

Diese Funktionen und die zugehörigen Rückruf Funktionen ermöglichen es Ihrer Anwendung, eine Liste aller Ressourcen in einem Modul zu erstellen. Dieser Vorgang wird unter [Erstellen einer Ressourcen Liste](using-resources.md)beschrieben.

## <a name="-see-also"></a>-Siehe auch

[Msistuff.exe Beispiel-App](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/sysmgmt/msi/msistuff)
