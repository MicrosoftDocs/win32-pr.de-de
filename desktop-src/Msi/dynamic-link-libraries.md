---
description: Eine benutzerdefinierte Aktion kann eine Funktion aufzurufen, die in einer DLL (Dynamic Link Library) definiert ist, die in C oder C++ geschrieben ist.
ms.assetid: 605c7b97-70bd-467a-9438-47b05d8b6b5d
title: Dynamic-Link-Bibliotheken (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5f9ff0113d97d219220a4f42030c1563f16ce7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042391"
---
# <a name="dynamic-link-libraries-windows-installer"></a>Dynamic-Link-Bibliotheken (Windows Installer)

Eine benutzerdefinierte Aktion kann eine Funktion aufzurufen, die in einer DLL (Dynamic Link Library) definiert ist, die in C oder C++ geschrieben ist. Die dll kann als Datei vorhanden sein, die während der aktuellen Installation installiert wird, oder als temporärer binärer Stream, der aus der [binären Tabelle](binary-table.md) der Installations Datenbank stammt.

Beachten Sie, dass alle aufgerufenen Funktionen, einschließlich benutzerdefinierter Aktionen in DLLs, die \_ \_ StdCall-Aufruf Konvention angeben müssen. Um z. b. CustomAction aufzurufen, verwenden Sie Folgendes:


```C++
#include <windows.h>
#include <msi.h>
#include <Msiquery.h>
#pragma comment(lib, "msi.lib")

UINT __stdcall CustomAction(MSIHANDLE hInstall)
```



Weitere Informationen finden Sie unter [zugreifen auf die aktuelle Installer-Sitzung von innerhalb einer benutzerdefinierten Aktion](accessing-the-current-installer-session-from-inside-a-custom-action.md) .

Die folgenden Typen von benutzerdefinierten Aktionen erfordern eine Dynamic Link Library.



| Benutzerdefinierter Aktionstyp                                 | BESCHREIBUNG                               |
|----------------------------------------------------|-------------------------------------------|
| [Benutzerdefinierter Aktionstyp 1](custom-action-type-1.md)   | DLL-Datei, die in einem binären Tabellenstream gespeichert ist. |
| [Benutzerdefinierter Aktionstyp 17](custom-action-type-17.md) | DLL-Datei, die mit einem Produkt installiert wird.        |



 

> [!Note]  
> Um com verwenden zu können, müssen Sie [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) in der benutzerdefinierten Aktion aufrufen. Beenden Sie nicht, wenn Sie feststellen, dass der Thread bereits initialisiert wurde. Der Thread wird z. b. in einer computerspezifischen Installation initialisiert, aber nicht in einer pro-Benutzer-Installation.

 

In der [Zusammenfassungs Liste aller benutzerdefinierten Aktions Typen](summary-list-of-all-custom-action-types.md) finden Sie eine Zusammenfassung aller Typen von benutzerdefinierten Aktionen und deren Codierung in die [CustomAction-Tabelle](customaction-table.md).

 

 
