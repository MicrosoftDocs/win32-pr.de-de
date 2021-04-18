---
description: Dieser Artikel enthält Informationen zur Verwaltung von Thread verweisen mithilfe von Funktionen aus den shelllightweight-Hilfsprogrammfunktionen.
ms.assetid: d8d479fd-c45a-4dfa-b496-76abc7c09a42
title: Verwalten von Thread verweisen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b629cd97c99e3b30e66810b5f54720d0dbb1c87d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979992"
---
# <a name="managing-thread-references"></a>Verwalten von Thread verweisen

Dieser Artikel enthält Informationen zur Verwaltung von Thread verweisen mithilfe von Funktionen aus den shelllightweight-Hilfsprogrammfunktionen.


Situationen treten auf, wenn ein übergeordneter Thread für die Lebensdauer eines untergeordneten Threads aktiv gehalten werden muss. Wenn z. bWeise ein Component Object Model (com)-Objekt auf dem übergeordneten Thread erstellt und an den untergeordneten Thread gemarshallt wird, kann dieser übergeordnete Thread nicht vor dem untergeordneten Thread beendet werden. Um dies zu erreichen, stellt die Shell diese Funktionen bereit.

-   [**Shkreatethlesref**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadref)
-   [**Shsetthreadref**](/windows/desktop/api/Shlwapi/nf-shlwapi-shsetthreadref)
-   [**Shgetthreadref**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetthreadref)

Verwenden Sie diese Funktionen in ihrem übergeordneten Thread, wie hier beschrieben.

1.  Deklarieren Sie eine Anwendungs definierte Thread Prozedur nach der Form der [*Thread proc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) -Funktion.

    ``` syntax
    DWORD WINAPI ThreadProc(LPVOID lpParameter);
    ```

2.  Rufen Sie in [*Thread proc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) [**shaliatetheinref**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadref) auf, um einen Verweis auf den Thread zu erstellen. Dadurch wird ein Zeiger auf eine Instanz von [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)bereitstellt. Dieses **IUnknown** verwendet den Wert, auf den *pkref* zeigt, um einen Verweis Zähler beizubehalten. Solange diese Anzahl größer als 0 ist, bleibt der Thread aktiv.
3.  Wenn Sie diesen Zeiger auf [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)verwenden, wird [**shsetthreadref**](/windows/desktop/api/Shlwapi/nf-shlwapi-shsetthreadref) in [*Thread proc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85))aufgerufen. Dadurch wird der Verweis so festgelegt, dass nachfolgende Aufrufe von [**shgetthreadref**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetthreadref) etwas abrufen können.
4.  Wenn Ihr [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) einen anderen Thread erstellt, kann *Thread proc* von Thread proc [**shgetthreadref**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetthreadref) mit dem Zeiger auf [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) aufrufen, der von [**shkreatethumref**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadref)abgerufen wurde. Dadurch wird der Verweis Zähler erhöht, auf den der *pkref* -Parameter in **shkreatethread Ref** zeigt.
5.  Erstellen Sie den Thread. Dies erfolgt in der Regel durch Aufrufen von " [**shcreatethread**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread)", wobei ein Zeiger auf " [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) " im Parameter " *pfnthreadproc* " übergeben wird. Übergeben Sie außerdem das CTF- \_ Thread- \_ ref-Flag im *dwFlags* -Parameter. Der Thread ist aktiv, solange *ThreadProc* ausgeführt wird.
6.  Wenn ein untergeordneter Thread erstellt wird, übergeben Sie das CTF-Flag zum **\_ \_ zählen** von Verweisen im *dwFlags* -Parameter im Aufrufen an seinen [**shkreatethread**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread).
7.  Wenn untergeordnete Threads fertiggestellt und freigegeben werden, wird der Wert, auf den die *pkref* des übergeordneten Threads zeigt, verringert. Nachdem alle untergeordneten Threads abgeschlossen sind, kann der ursprüngliche [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) -Vorgang abgeschlossen werden und den endgültigen Thread Verweis freigeben, wodurch der Verweis Zähler auf 0 (null) gelöscht wird. An diesem Punkt wird der Verweis auf den ursprünglichen, von [**shkreatethread**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread) geöffneten Thread freigegeben, und der Thread ist abgeschlossen.

Eine weitere verwandte Funktion ist " [**shreleasethlesref**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreleasethreadref)". Diese Funktion wird von [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) aufgerufen, wenn der Thread mithilfe von [**shkreatethread**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread) mit dem **CTF- \_ Thread \_ ref** -Flag erstellt wurde. *Thread proc* ist jedoch nicht erforderlich. Der Aufruf von [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) auf dem Zeiger auf [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) , der über " [**shcreatethleref**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadref) " abgerufen wurde, muss nur durchgeführt werden.

 

 
