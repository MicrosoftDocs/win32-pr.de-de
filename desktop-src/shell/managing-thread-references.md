---
description: Dieser Artikel enthält Informationen zur Verwaltung von Threadverweisen mithilfe von Funktionen aus den einfachen Shell-Hilfsfunktionen.
ms.assetid: d8d479fd-c45a-4dfa-b496-76abc7c09a42
title: Verwalten von Threadverweisen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6380957f5f8ef9be62e291820fe12d715f31a5f5bb5ba81b80aa1c8606478e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968919"
---
# <a name="managing-thread-references"></a>Verwalten von Threadverweisen

Dieser Artikel enthält Informationen zur Verwaltung von Threadverweisen mithilfe von Funktionen aus den einfachen Shell-Hilfsfunktionen.


Situationen treten auf, wenn ein übergeordneter Thread während der Lebensdauer eines untergeordneten Threads aktiv bleiben muss. Wenn beispielsweise ein Component Object Model -Objekt (COM) im übergeordneten Thread erstellt und an den untergeordneten Thread gemarshallt wird, kann dieser übergeordnete Thread nicht vor dem untergeordneten Thread beendet werden. Zu diesem Zweck stellt die Shell diese Funktionen bereit.

-   [**SHCreateThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadref)
-   [**SHSetThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shsetthreadref)
-   [**SHGetThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetthreadref)

Verwenden Sie diese Funktionen in Ihrem übergeordneten Thread, wie hier beschrieben.

1.  Deklarieren Sie eine anwendungsdefinierte Threadprozedur gemäß der Form der [*ThreadProc-Funktion.*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85))

    ``` syntax
    DWORD WINAPI ThreadProc(LPVOID lpParameter);
    ```

2.  Rufen [*Sie in ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) [**SHCreateThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadref) auf, um einen Verweis auf den Thread zu erstellen. Dies stellt einen Zeiger auf eine Instanz von [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)bereit. Dieser **IUnknown** verwendet den Wert, auf den *pcRef* zeigt, um einen Verweiszähler beizubehalten. Solange diese Anzahl größer als 0 ist, bleibt der Thread aktiv.
3.  Rufen Sie mit diesem Zeiger auf [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) [**SHSetThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shsetthreadref) in [*Ihrem ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85))auf. Dadurch wird der Verweis so festgelegt, dass nachfolgende Aufrufe von [**SHGetThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetthreadref) etwas abrufen können.
4.  Wenn [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) einen anderen Thread erstellt, kann *ThreadProc* dieses Threads [**SHGetThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetthreadref) mit dem Zeiger auf [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) aufrufen, der von [**SHCreateThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadref)abgerufen wurde. Dadurch wird der Verweiszähler erhöht, auf den der *pcRef-Parameter* in **SHCreateThreadRef** zeigt.
5.  Erstellen Sie den Thread. Dies erfolgt in der Regel durch Aufrufen von [**SHCreateThread,**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread)wobei ein Zeiger auf [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) im *pfnThreadProc-Parameter* übergeben wird. Übergeben Sie außerdem das CTF \_ THREAD \_ REF-Flag im *dwFlags-Parameter.* Der Thread ist aktiv, solange *ThreadProc* ausgeführt wird.
6.  Wenn ein untergeordneter Thread erstellt wird, übergeben Sie das **CTF \_ \_ REF-COUNTED-Flag** im *dwFlags-Parameter* im Aufruf des [**SHCreateThread-**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread).
7.  Wenn untergeordnete Threads abgeschlossen und freigegeben werden, verringert sich der Wert, auf den *pcRef* des übergeordneten Threads zeigt. Sobald alle untergeordneten Threads abgeschlossen sind, kann die ursprüngliche [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) abgeschlossen sein und den endgültigen Threadverweis freigeben, wobei der Verweiszähler auf 0 (0) fällt. An diesem Punkt wird der Verweis auf den ursprünglichen Thread freigegeben, der von [**SHCreateThread**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread) geöffnet wurde, und der Thread wurde abgeschlossen.

Eine weitere verwandte Funktion ist [**SHReleaseThreadRef.**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreleasethreadref) Diese Funktion wird von [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) aufgerufen, wenn der Thread mithilfe von [**SHCreateThread**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread) mit dem **CTF \_ THREAD \_ REF-Flag** erstellt wurde. *ThreadProc* ist jedoch nicht erforderlich, um dies implizit zu tun. Das Aufrufen von [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) für den Zeiger auf [**IUnknown,**](/windows/win32/api/unknwn/nn-unknwn-iunknown) der über [**SHCreateThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadref) abgerufen wurde, ist alles, was erledigt werden muss.

 

 
