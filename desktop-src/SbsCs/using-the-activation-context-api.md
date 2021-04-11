---
description: Anwendungen können einen Aktivierungs Kontext verwalten, indem Sie die Aktivierungs Kontextfunktionen direkt aufrufen.
ms.assetid: 606147a8-435d-43d4-8fb5-79d2d1a8d870
title: Verwenden der Aktivierungs Kontext-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62b3aec5b7840e70e8fae93575e65c2f06668936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128809"
---
# <a name="using-the-activation-context-api"></a>Verwenden der Aktivierungs Kontext-API

Anwendungen können einen [Aktivierungs Kontext](activation-contexts.md) verwalten, indem Sie die Aktivierungs Kontextfunktionen direkt aufrufen. Aktivierungs Kontexte sind Datenstrukturen im Arbeitsspeicher. Das System kann die Informationen im Aktivierungs Kontext verwenden, um eine Anwendung so umzuleiten, dass Sie eine bestimmte dll-Version, com-Objektinstanz oder eine benutzerdefinierte Fensterversion lädt. Weitere Informationen finden Sie unter [Aktivierungs Kontext Referenz](activation-context-reference.md).

Die API (Application Programming Interface) kann verwendet werden, um den Aktivierungs Kontext zu verwalten und Versions benannte Objekte mit [Manifesten](manifests.md)zu erstellen. Die folgenden beiden Szenarien veranschaulichen, wie eine Anwendung einen Aktivierungs Kontext verwalten kann, indem die Aktivierungs Kontextfunktionen direkt aufgerufen werden. In den meisten Fällen wird der Aktivierungs Kontext jedoch vom System verwaltet. Anwendungsentwickler und Assemblyanbieter müssen häufig keine Aufrufe an den Stapel vornehmen, um den Aktivierungs Kontext zu verwalten.

-   Prozesse und Anwendungen, die Dereferenzierungs-oder Dispatch-Ebenen implementieren.

    Beispielsweise ein Benutzer, der Aktivierungs Kontexte in der Ereignisschleife verwaltet. Jedes Mal, wenn auf das Fenster zugegriffen wird, z. b. durch Bewegen des Mauszeigers über das Fenster, wird [**activateactctx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) aufgerufen, das den aktuellen Aktivierungs Kontext für die Ressource aktiviert, wie im folgenden Code Fragment dargestellt.

    <dl> Handle von hactctx;  
    "Kreatewindow ();"  
    ...  
    Getcurrentactctx (&ActCtx);  
    ...  
    Releaseactctx (&ActCtx);  
    </dl>

    Im folgenden Code Fragment werden die entsprechenden Aktivierungs Kontexte von der API-Funktion aktiviert, bevor [**callwindowproc**](/windows/win32/api/winuser/nf-winuser-callwindowproca)aufgerufen wird. Wenn **callwindowproc** aufgerufen wird, wird dieser Kontext verwendet, um eine Nachricht an Windows zu übergeben. Wenn alle Ressourcen Vorgänge abgeschlossen sind, deaktiviert die Funktion den Kontext.

    <dl> ULONG \_ ptr ulpcookie;  
    Handle von hactctx;  
    if (activateactctx (hactctx, &ulpcookie))  
    {  
    ...  
    Callwindowproc (...);  
    ...  
    Deactivateactctx (0, ulpcookie);  
    }  
    </dl>

-   Delegatschutzschicht.

    Dieses Szenario gilt für Manager, die mehrere Entitäten mit einer gemeinsamen API-Schicht verwalten, z. b. Treiber-Manager. Obwohl es noch nicht implementiert wurde, wäre dies ein Beispiel für den ODBC-Treiber.

    In diesem Szenario kann die mittlere Ebene Assemblybindungen verarbeiten. Um den Versions spezifischen Bindungs Treiber zu erhalten, müssen die Verleger ein Manifest bereitstellen und Abhängigkeiten für bestimmte Komponenten in diesem Manifest angeben. Die Basisanwendung bindet nicht dynamisch an die-Komponenten. zur Laufzeit verwaltet der Treiber-Manager die Aufrufe. Wenn der ODBC-Treiber auf der Grundlage der Verbindungs Zeichenfolge aufgerufen wird, wird der entsprechende Treiber geladen. Anschließend wird der Aktivierungs Kontext mithilfe der Informationen in der Assembly Manifest-Datei erstellt.

    Ohne das Manifest ist die Standardaktion für den Treiber die Verwendung desselben Kontexts, der von der Anwendung angegeben wird – in diesem Beispiel Version 2 von msvcrt. Da ein Manifest vorhanden ist, wird ein separater Aktivierungs Kontext eingerichtet. Wenn der ODBC-Treiber ausgeführt wird, wird er an Version 1 der msvcrt-Assembly gebunden.

    Jedes Mal, wenn der Treiber-Manager die Dispatch-Schicht aufruft – beispielsweise, um den nächsten Satz von Daten zu erhalten – verwendet er die entsprechenden Assemblys basierend auf dem Aktivierungs Kontext. Dies wird im folgenden Code Fragment veranschaulicht.

    <dl> Handle von hactctx;  
    ULONG \_ ptr ulpcookie;  
    ActCtx actctxdecreate = {...};  
    hactctx = kreateactctx (&actctxdecreate);  
    ...;  
    if (activateactctx (hactctx, &ulpcookie))  
    {  
    ...  
    ConnectDB (...);  
    Deactivateactctx (0, ulpcookie);  
    }  
    ...  
    Releaseactctx (hactctx);  
    </dl>

 

 
