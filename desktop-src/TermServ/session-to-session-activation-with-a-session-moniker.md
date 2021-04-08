---
title: Sitzungs-zu-Sitzung-Aktivierung mit einem sitzungsmoniker
description: Die Sitzungs-zu-Sitzung-Aktivierung (auch Sitzungs übergreifende Aktivierung genannt) ermöglicht einem Client Prozess das Starten (aktivieren) eines lokalen Server Prozesses für eine bestimmte Sitzung.
ms.assetid: d405c276-040b-4cde-aeb2-482a25e2867f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2714f3dbe7b23c8b7f04d4271018891960b87f76
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729617"
---
# <a name="session-to-session-activation-with-a-session-moniker"></a><span data-ttu-id="2070a-103">Sitzungs-zu-Sitzung-Aktivierung mit einem sitzungsmoniker</span><span class="sxs-lookup"><span data-stu-id="2070a-103">Session-to-Session Activation with a Session Moniker</span></span>

<span data-ttu-id="2070a-104">Die Sitzungs-zu-Sitzung-Aktivierung (auch Sitzungs übergreifende Aktivierung genannt) ermöglicht einem Client Prozess das Starten (aktivieren) eines lokalen Server Prozesses für eine bestimmte Sitzung.</span><span class="sxs-lookup"><span data-stu-id="2070a-104">Session-to-session activation (also called cross-session activation) allows a client process to start (activate) a local server process on a specified session.</span></span> <span data-ttu-id="2070a-105">Diese Funktion ist für Anwendungen verfügbar, die so konfiguriert sind, dass Sie im Sicherheitskontext des interaktiven Benutzers ausgeführt werden, der auch als "runas Interactive User"-Objekt Aktivierungs Modus bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="2070a-105">This feature is available for applications that are configured to run in the security context of the interactive user, also known as the "RunAs Interactive User" object activation mode.</span></span> <span data-ttu-id="2070a-106">Weitere Informationen zu Sicherheits Kontexten finden Sie [im Sicherheitskontext des Clients](/windows/desktop/SecAuthZ/the-client-security-context).</span><span class="sxs-lookup"><span data-stu-id="2070a-106">For more information about security contexts, see [The Client's Security Context](/windows/desktop/SecAuthZ/the-client-security-context).</span></span>

<span data-ttu-id="2070a-107">Verteiltes com (DCOM) ermöglicht die Objekt Aktivierung pro Sitzung mithilfe eines vom System bereitgestellten [sitzungsmonikers](session-monikers.md).</span><span class="sxs-lookup"><span data-stu-id="2070a-107">Distributed COM (DCOM) enables object activation on a per-session basis by using a system-supplied [Session Moniker](session-monikers.md).</span></span> <span data-ttu-id="2070a-108">Andere vom System bereitgestellte Moniker sind [dateimoniker](../com/file-monikers.md), [elementmoniker](../com/item-monikers.md), generische zusammen [gesetzte Moniker](../com/composite-monikers.md), [Anti-Moniker](../com/anti-monikers.md), [zeigermoniker](../com/pointer-monikers.md)und [URL-Moniker](../com/url-monikers.md).</span><span class="sxs-lookup"><span data-stu-id="2070a-108">Other system-supplied monikers include [file monikers](../com/file-monikers.md), [item monikers](../com/item-monikers.md), generic [composite monikers](../com/composite-monikers.md), [anti-monikers](../com/anti-monikers.md), [pointer monikers](../com/pointer-monikers.md), and [URL monikers](../com/url-monikers.md).</span></span>

<span data-ttu-id="2070a-109">Damit der sitzungsmoniker verwendet werden kann, muss die DCOM-Anwendung so festgelegt werden, dass Sie als interaktiver Benutzer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2070a-109">To be able to use the session moniker, the DCOM application must be set to run as the interactive user.</span></span> <span data-ttu-id="2070a-110">Dies kann mithilfe des Verwaltungs Tools Komponenten Dienste, Anzeigen der Eigenschaften der DCOM-Anwendung und auswählen **des interaktiven Benutzers** auf der Registerkarte **Identität** festgelegt werden. Weitere Informationen zu den möglichen Sicherheitsrisiken im Zusammenhang mit der Festlegung einer DCOM-Anwendung für die Verwendung als interaktiver Benutzer in einer Remotedesktopdienste Umgebung finden Sie im Abschnitt "Anwendungs Identität (com)" der com-Dokumentation im Platform Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="2070a-110">This can be set by using the Component Services Administrative tool, viewing the Properties of the DCOM application, and selecting **The interactive user** on the **Identity** tab. For more information about the possible security risks associated with setting a DCOM application to run as the interactive user in a Remote Desktop Services environment, see the "Application Identity (COM)" section of the COM documentation in the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="2070a-111">Wenn ein anderer Benutzertyp ausgewählt ist, um die Anwendung auszuführen, wird der sitzungsmoniker von der Anwendung ignoriert.</span><span class="sxs-lookup"><span data-stu-id="2070a-111">If any other type of user is selected to run the application, the session moniker will be ignored by the application.</span></span> <span data-ttu-id="2070a-112">Der sitzungsmoniker wird auch von com+-Server Anwendungen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="2070a-112">The session moniker is also ignored by COM+ server applications.</span></span> <span data-ttu-id="2070a-113">Weitere Informationen zu anderen Methoden zum Auswählen des Benutzer Typs zum Ausführen der Anwendung finden Sie in der com-Dokumentation im Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="2070a-113">For more information about other methods for selecting the type of user to run the application, see the COM documentation in the Platform SDK.</span></span>

<span data-ttu-id="2070a-114">Um einen sitzungsmoniker zu erstellen, müssen Sie die Sitzungs-ID der Remotedesktopdienste Sitzung mit einem klassenmoniker verfassen, der die Klassen-ID des Prozess Servers angibt.</span><span class="sxs-lookup"><span data-stu-id="2070a-114">To create a session moniker, you must compose the session ID of the Remote Desktop Services session with a class moniker that specifies the process server's class ID.</span></span>

<span data-ttu-id="2070a-115">**So erstellen Sie einen sitzungsmoniker**</span><span class="sxs-lookup"><span data-stu-id="2070a-115">**To create a session moniker**</span></span>

1.  <span data-ttu-id="2070a-116">Legen Sie den anzeigen amen des klassenmonikers mit dem anzeigen amen des sitzungsmonikers mit der folgenden Syntax als Präfix:</span><span class="sxs-lookup"><span data-stu-id="2070a-116">Prefix the display name of the class moniker with the display name of the session moniker by using the following syntax:</span></span>

    ``` syntax
    "Session:[digits]!clsid:[class id]"
    ```

    <span data-ttu-id="2070a-117">, wobei *Ziffern* die Sitzungs-ID der Sitzung darstellt, für die der Server Prozess gestartet wird, und WHERE *Class ID* die Klassen-ID des Servers darstellt.</span><span class="sxs-lookup"><span data-stu-id="2070a-117">where *digits* represents the session ID of the session on which the server process will be started, and where *class id* represents the class ID of the server.</span></span> <span data-ttu-id="2070a-118">Beachten Sie, dass die Sitzungs-ID eine Basis-10-Nummer ist.</span><span class="sxs-lookup"><span data-stu-id="2070a-118">Note that the session ID is a base-10 number.</span></span>

    <span data-ttu-id="2070a-119">Bei Computern, auf denen Windows XP oder höher ausgeführt wird, führt die Verwendung der folgenden Syntax dazu, dass com die Aktivierung an die derzeit aktive physische Konsolen Sitzung sendet, je nachdem, wie die Sitzungs-ID lautet:</span><span class="sxs-lookup"><span data-stu-id="2070a-119">For computers that are running Windows XP or later, using the following syntax will result in COM sending the activation to the currently active physical console session, whatever its session ID is:</span></span>

    ``` syntax
    "Session:Console!clsid:[class id]"
    ```

2.  <span data-ttu-id="2070a-120">Nachdem Sie den sitzungsmoniker erstellt haben, können Sie das Ergebnis entweder an die Funktion " [**mkparamesedisplayname**](/windows/desktop/api/objbase/nf-objbase-mkparsedisplayname) " oder an die Funktion " [mkzisedisplaynameex](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) " übergeben.</span><span class="sxs-lookup"><span data-stu-id="2070a-120">After you have created the session moniker, you can pass the result to either the [**MkParseDisplayName**](/windows/desktop/api/objbase/nf-objbase-mkparsedisplayname) function or the [MkParseDisplayNameEx](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) function.</span></span>

<span data-ttu-id="2070a-121">Sie können einen sitzungsmoniker auf die gleiche Weise verwenden wie einen beliebigen anderen Moniker.</span><span class="sxs-lookup"><span data-stu-id="2070a-121">You can use a session moniker in the same way as you would use any other moniker.</span></span>

<span data-ttu-id="2070a-122">Ein Codebeispiel, in dem veranschaulicht wird, wie Sie einen lokalen Server Prozess für eine bestimmte Sitzung aktivieren, finden [Sie unter using an Session Moniker](using-a-session-moniker.md).</span><span class="sxs-lookup"><span data-stu-id="2070a-122">For a code sample that demonstrates how to activate a local server process on a specified session, see [Using a Session Moniker](using-a-session-moniker.md).</span></span>

<span data-ttu-id="2070a-123">Weitere Informationen zur Objekt Aktivierung, vom System bereitgestellte Moniker und klassenmoniker finden Sie in der com-Dokumentation im Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="2070a-123">For more information about object activation, system-supplied monikers and class monikers, see the COM documentation in the Platform SDK.</span></span>

> [!Note]  
> <span data-ttu-id="2070a-124">Prozesse, die Sitzungs übergreifend erstellt werden, weisen eine Obergrenze für die Größe des Umgebungs Blocks auf.</span><span class="sxs-lookup"><span data-stu-id="2070a-124">Processes that are created across sessions have an upper limit on the size of the environment block.</span></span> <span data-ttu-id="2070a-125">Dieser Grenzwert beträgt ca. 4 KB, kann jedoch je nach den anderen zum Erstellen des Prozesses benötigten Informationen (z. b. Dateinamen, Verzeichnisse und Parameter für den neuen Prozess) größer oder kleiner sein.</span><span class="sxs-lookup"><span data-stu-id="2070a-125">This limit is around 4 KB, but it can be larger or smaller depending on what other information is needed to create the process (for example file names, directories, and parameters for the new process).</span></span>

 

 

 