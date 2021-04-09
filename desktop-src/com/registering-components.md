---
title: Registrieren von Komponenten
description: Registrieren von Komponenten
ms.assetid: d7fd231b-17ec-42ad-9144-df7ed5ffb17b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d683ae419466d62d764283cfa8706981de402a9
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039647"
---
# <a name="registering-components"></a>Registrieren von Komponenten

Wenn die folgenden Anwendungs Typen installiert sind, müssen die Installationsinformationen der Registrierung hinzugefügt werden, in der Regel über ein Setup Programm:

-   Server Anwendungen
-   Container-/Server-Anwendungen
-   Container Anwendungen, die das Verknüpfen mit eingebetteten Objekten ermöglichen

Registrieren Sie für alle drei Instanzen com library (dll)-Informationen und anwendungsspezifische Informationen.

Die dll registriert die Informationen für alle Ihre Komponenten, indem Sie [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) und [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver)exportiert. Verwenden Sie die folgenden Funktionen, um eine Komponente zu registrieren und die Registrierung aufzuheben:

-   [**Fehler bei RegOpenKeyEx**](/windows/desktop/api/winreg/nf-winreg-regopenkeyexa)
-   [**Regkreatekeyex**](/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa)
-   [**Fehler bei RegSetValueEx**](/windows/desktop/api/winreg/nf-winreg-regsetvalueexa)
-   [**Regenum keyex**](/windows/desktop/api/winreg/nf-winreg-regenumkeyexa)
-   [**Regdeletekey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya)
-   [**Fehler bei RegCloseKey**](/windows/desktop/api/winreg/nf-winreg-regclosekey)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrieren von com-Anwendungen](registering-com-applications.md)
</dt> </dl>

 

 