---
description: Anwendungen können einen Aktivierungskontext verwalten, indem sie die Aktivierungskontextfunktionen direkt aufrufen.
ms.assetid: 606147a8-435d-43d4-8fb5-79d2d1a8d870
title: Verwenden der Aktivierungskontext-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5c2f3d1c1a6b6202619b9e39df6ee4dc60b9134ebefa9cfe7dea4db9a344bd7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073300"
---
# <a name="using-the-activation-context-api"></a>Verwenden der Aktivierungskontext-API

Anwendungen können einen [Aktivierungskontext](activation-contexts.md) verwalten, indem sie die Aktivierungskontextfunktionen direkt aufrufen. Aktivierungskontexte sind Datenstrukturen im Arbeitsspeicher. Das System kann die Informationen im Aktivierungskontext verwenden, um eine Anwendung umzuleiten, um eine bestimmte DLL-Version, EINE COM-Objektinstanz oder eine benutzerdefinierte Fensterversion zu laden. Weitere Informationen finden Sie unter [Referenz zum Aktivierungskontext.](activation-context-reference.md)

Die Anwendungsprogrammierschnittstelle (APPLICATION PROGRAMMING Interface, API) kann verwendet werden, um den [Aktivierungskontext](manifests.md)zu verwalten und Versionsobjekte mit Manifesten zu erstellen. Die folgenden beiden Szenarien veranschaulichen, wie eine Anwendung einen Aktivierungskontext verwalten kann, indem sie die Aktivierungskontextfunktionen direkt aufruft. In den meisten Fällen wird der Aktivierungskontext jedoch vom System verwaltet. Anwendungsentwickler und Assemblyanbieter müssen den Stapel häufig nicht aufrufen, um den Aktivierungskontext zu verwalten.

-   Prozesse und Anwendungen, die Dekonstruktions- oder Verteilungsebenen implementieren.

    Beispielsweise ein Benutzer, der Aktivierungskontexte in der Ereignisschleife verwaltet. Bei jedem Zugriff auf das Fenster, z. B. durch Bewegen des Mauszeigers über das Fenster, wird [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) aufgerufen, wodurch der aktuelle Aktivierungskontext für die Ressource aktiviert wird, wie im folgenden Codefragment gezeigt.

    <dl> HANDLE hActCtx;  
    CreateWindow();  
    ...  
    GetCurrentActCtx(&ActCtx);  
    ...  
    ReleaseActCtx(&ActCtx);  
    </dl>

    Im folgenden Codefragment aktiviert die API-Funktion die entsprechenden Aktivierungskontexte, bevor [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca)aufgerufen wird. Wenn **CallWindowProc** aufgerufen wird, wird dieser Kontext verwendet, um eine Nachricht an Windows zu übergeben. Wenn alle Ressourcenvorgänge abgeschlossen sind, deaktiviert die Funktion den Kontext.

    <dl> ULONG \_ PTR ulpCookie;  
    HANDLE hActCtx;  
    if(ActivateActCtx(hActCtx, &ulpCookie))  
    {  
    ...  
    CallWindowProc(...);  
    ...  
    DeactivateActCtx(0, ulpCookie);  
    }  
    </dl>

-   Delegator-Verteilungsebene.

    Dieses Szenario gilt für Manager, die mehrere Entitäten mit einer gemeinsamen API-Ebene verwalten, z. B. einem Treiber-Manager. Obwohl es noch nicht implementiert wurde, wäre ein Beispiel dafür der ODBC-Treiber.

    In diesem Szenario kann die mittlere Ebene Assemblybindungen verarbeiten. Um den versionsspezifischen Bindungstreiber abzurufen, müssen Herausgeber ein Manifest bereitstellen und Abhängigkeiten von bestimmten Komponenten in diesem Manifest angeben. Die Basisanwendung wird nicht dynamisch an die Komponenten gebunden. Zur Laufzeit verwaltet der Treiber-Manager die Aufrufe. Wenn der ODBC-Treiber basierend auf der Verbindungszeichenfolge aufgerufen wird, lädt er den entsprechenden Treiber. Anschließend wird der Aktivierungskontext mithilfe der Informationen in der Assemblymanifestdatei erstellt.

    Ohne das Manifest besteht die Standardaktion für den Treiber darin, denselben Kontext zu verwenden, der von der Anwendung angegeben wird – in diesem Beispiel Version 2 von MSVCRT. Da ein Manifest vorhanden ist, wird ein separater Aktivierungskontext eingerichtet. Wenn der ODBC-Treiber ausgeführt wird, wird er an Version 1 der MSVCRT-Assembly gebunden.

    Jedes Mal, wenn der Treiber-Manager die Verteilungsebene aufruft, z. B. um den nächsten Satz von Daten abzurufen, verwendet er die entsprechenden Assemblys basierend auf dem Aktivierungskontext. Dies wird im folgenden Codefragment veranschaulicht.

    <dl> HANDLE hActCtx;  
    ULONG \_ PTR ulpCookie;  
    ACTCTX ActCtxToCreate = {...};  
    hActCtx = CreateActCtx(&ActCtxToCreate);  
    ...;  
    if (ActivateActCtx(hActCtx, &ulpCookie))  
    {  
    ...  
    ConnectDb(...);  
    DeactivateActCtx(0, ulpCookie);  
    }  
    ...  
    ReleaseActCtx(hActCtx);  
    </dl>

 

 
