---
title: Verweis Nachverfolgung
description: Verweis Nachverfolgung
ms.assetid: 1e2cf555-3b96-42d5-a0bb-abb720c93520
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f45607a495e973ec33acde6d97cb1f83259a27c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474309"
---
# <a name="reference-tracking"></a><span data-ttu-id="04c65-103">Verweis Nachverfolgung</span><span class="sxs-lookup"><span data-stu-id="04c65-103">Reference Tracking</span></span>

<span data-ttu-id="04c65-104">Die Verweis Nachverfolgung kann die unbeabsichtigte oder schädliche frühe Freigabe von Objekten verhindern.</span><span class="sxs-lookup"><span data-stu-id="04c65-104">Reference tracking can prevent the unintentional or malicious early release of objects.</span></span>

<span data-ttu-id="04c65-105">Wenn Sie die Verweis Verfolgung aktivieren, fordern Sie an, dass verteilte [**adressf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) -und [**releaseaufrufe**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) von com authentifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="04c65-105">When you enable reference tracking, you are requesting that distributed [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) and [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) calls be authenticated by COM.</span></span> <span data-ttu-id="04c65-106">Wenn die Verweis Verfolgung aktiviert ist, verfolgt com den Verweis Zähler pro Benutzer, damit ein Benutzer die **Freigabe** nur für Objekte aufrufen kann, die der Benutzer zuvor als " **adressf** " bezeichnet hat.</span><span class="sxs-lookup"><span data-stu-id="04c65-106">When reference tracking is enabled, COM keeps track of per-user reference counts so that a user can call **Release** only on objects that the user previously called **AddRef** on.</span></span> <span data-ttu-id="04c65-107">Obwohl bei der Verweis Nachverfolgung die Leistung beeinträchtigt werden kann, wird sichergestellt, dass unabhängig davon, wie oft ein bestimmter Benutzer die **Freigabe** aufruft, die Objekte und stubwerte weiterhin vorhanden sind, wenn ein anderer Benutzer einen Verweis darauf hat.</span><span class="sxs-lookup"><span data-stu-id="04c65-107">Although reference tracking can decrease performance, it ensures that no matter how many times a given user calls **Release**, the objects and stubs will still exist if someone else has a reference to them.</span></span>

<span data-ttu-id="04c65-108">Der Client kann die Verweis Nachverfolgung für einen Prozess festlegen, indem er \_ \_ in einem [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)-Rückruf das eoac Secure Refs-funktionsflag übergibt.</span><span class="sxs-lookup"><span data-stu-id="04c65-108">The client can set reference tracking for a process by passing the EOAC\_SECURE\_REFS capability flag in a call to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="04c65-109">Mithilfe Dcomcnfg.exe können Sie auch die Verweis Nachverfolgung für alle Anwendungen auf einem Computer aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="04c65-109">You can also enable or disable reference tracking for all applications on a computer by using Dcomcnfg.exe.</span></span>

<span data-ttu-id="04c65-110">Wenn die Verweis Nachverfolgung aktiviert ist, verwendet [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) immer Standard Sicherheitseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="04c65-110">If reference tracking is enabled, [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) always uses default security settings.</span></span> <span data-ttu-id="04c65-111">In diesem Fall tritt bei Aufrufen von [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) bei **IUnknown** ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="04c65-111">In this case, calls to [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) on **IUnknown** will fail.</span></span>

 

 