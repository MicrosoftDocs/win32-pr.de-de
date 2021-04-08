---
title: Öffnen und Schließen einer WinSNMP-Sitzung
description: Um eine Sitzung zu öffnen, ruft eine Anwendung die snmpkreatesession-Funktion auf.
ms.assetid: 76650231-509b-45be-b156-09752b817854
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e006ffb81f6c2508b3505678b28c3ace8e60c85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037286"
---
# <a name="opening-and-closing-a-winsnmp-session"></a><span data-ttu-id="d156c-103">Öffnen und Schließen einer WinSNMP-Sitzung</span><span class="sxs-lookup"><span data-stu-id="d156c-103">Opening and Closing a WinSNMP Session</span></span>

<span data-ttu-id="d156c-104">Um eine Sitzung zu öffnen, ruft eine Anwendung die [**snmpkreatesession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="d156c-104">To open a session, an application calls the [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) function.</span></span> <span data-ttu-id="d156c-105">Wenn die Funktion erfolgreich abgeschlossen wird, wird von der Microsoft WinSNMP-Implementierung eine Sitzung geöffnet, und die Funktion gibt einen Sitzungs Bezeichner in Form eines **hsnmp- \_ Sitzungs** Handles zurück.</span><span class="sxs-lookup"><span data-stu-id="d156c-105">If the function completes successfully, the Microsoft WinSNMP implementation opens a session, and the function returns a session identifier in the form of an **HSNMP\_SESSION** handle.</span></span> <span data-ttu-id="d156c-106">Alle WinSNMP-Funktionen, die Handle-Variablen zurückgeben, enthalten den Sitzungs Bezeichner als Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="d156c-106">All WinSNMP functions that return handle variables include the session identifier as an input parameter.</span></span> <span data-ttu-id="d156c-107">Dadurch kann die Implementierung das Handle verwenden, um Ressourcen auf Sitzungs Ebene effizient zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="d156c-107">This enables the implementation to use the handle to efficiently manage resources at the session level.</span></span>

<span data-ttu-id="d156c-108">In einer Anwendung können mehrere Sitzungen gleichzeitig geöffnet sein.</span><span class="sxs-lookup"><span data-stu-id="d156c-108">An application can have multiple sessions open at one time.</span></span> <span data-ttu-id="d156c-109">Mehrere Sitzungen in einer Anwendung können Handle-Variablen freigeben.</span><span class="sxs-lookup"><span data-stu-id="d156c-109">Multiple sessions within an application can share handle variables.</span></span>

<span data-ttu-id="d156c-110">Wenn die Implementierung eine Sitzung aufgrund von Ressourceneinschränkungen nicht öffnen kann, wird ein Snmpapi-Fehler zurückgegeben, \_ Wenn die Anwendung [**snmpkreatesession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession)aufruft.</span><span class="sxs-lookup"><span data-stu-id="d156c-110">If the implementation cannot open a session because of resource limitations, it returns SNMPAPI\_FAILURE when the application calls [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession).</span></span> <span data-ttu-id="d156c-111">Wenn die Anwendung dann die [**snmpgetlasterror**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) -Funktion aufruft, gibt Sie den Fehler "Snmpapi-Zuweisung" zurück \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d156c-111">If the application then calls the [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) function, it returns SNMPAPI\_ALLOC\_ERROR.</span></span>

<span data-ttu-id="d156c-112">Ein Aufrufe der [**snmpclose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) -Funktion ermöglicht der Implementierung, alle verbleibenden Ressourcen freizugeben und die Sitzung zu schließen.</span><span class="sxs-lookup"><span data-stu-id="d156c-112">A call to the [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) function enables the implementation to free any remaining resources and to close the session.</span></span>

<span data-ttu-id="d156c-113">Weitere Informationen finden Sie unter [resource handle-Objekte](resource-handle-objects.md) und [WinSNMP-Sitzungen](winsnmp-sessions.md).</span><span class="sxs-lookup"><span data-stu-id="d156c-113">For more information, see [Resource Handle Objects](resource-handle-objects.md) and [WinSNMP Sessions](winsnmp-sessions.md).</span></span>

 

 




