---
description: Eine benutzerdefinierte Aktion kann eine Funktion aufrufen, die in einer DLL (Dynamic Link Library) definiert ist, die in C oder C++ geschrieben wurde.
ms.assetid: 605c7b97-70bd-467a-9438-47b05d8b6b5d
title: Dynamic-Link-Bibliotheken (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bcd2548851dcef4dcf08c53f168ec0f6b43ee036a1c250f9f65f072427a19e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378262"
---
# <a name="dynamic-link-libraries-windows-installer"></a>Dynamic-Link-Bibliotheken (Windows Installer)

Eine benutzerdefinierte Aktion kann eine Funktion aufrufen, die in einer DLL (Dynamic Link Library) definiert ist, die in C oder C++ geschrieben wurde. Die DLL kann als Datei vorhanden sein, die während der aktuellen Installation installiert wurde, oder als temporärer binärer Datenstrom, der aus der [Binärtabelle](binary-table.md) der Installationsdatenbank stammt.

Beachten Sie, dass alle aufgerufenen Funktionen, einschließlich benutzerdefinierter Aktionen in DLLs, die \_ \_ Stdcall-Aufrufkonvention angeben müssen. Verwenden Sie beispielsweise Folgendes, um CustomAction aufzurufen.


```C++
#include <windows.h>
#include <msi.h>
#include <Msiquery.h>
#pragma comment(lib, "msi.lib")

UINT __stdcall CustomAction(MSIHANDLE hInstall)
```



Weitere Informationen finden Sie unter [Zugreifen auf die aktuelle Installersitzung über eine benutzerdefinierte Aktion.](accessing-the-current-installer-session-from-inside-a-custom-action.md)

Die folgenden Arten von benutzerdefinierten Aktionen rufen eine Dynamic Link Library auf.



| Benutzerdefinierter Aktionstyp                                 | BESCHREIBUNG                               |
|----------------------------------------------------|-------------------------------------------|
| [Benutzerdefinierter Aktionstyp 1](custom-action-type-1.md)   | DLL-Datei, die in einem Binärtabellenstream gespeichert ist. |
| [Benutzerdefinierter Aktionstyp 17](custom-action-type-17.md) | DLL-Datei, die mit einem Produkt installiert ist.        |



 

> [!Note]  
> Um COM verwenden zu können, müssen Sie [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) in der benutzerdefinierten Aktion aufrufen. Beenden Sie nicht, wenn Sie feststellen, dass der Thread bereits initialisiert wurde. Beispielsweise wird der Thread in einer Computerinstallation initialisiert, jedoch nicht in einer Benutzerinstallation.

 

Unter [Summary List of All Custom Action Types (Zusammenfassungsliste aller benutzerdefinierten Aktionstypen)](summary-list-of-all-custom-action-types.md) finden Sie eine Zusammenfassung aller Typen von benutzerdefinierten Aktionen und deren Codierung in der [Tabelle CustomAction.](customaction-table.md)

 

 
