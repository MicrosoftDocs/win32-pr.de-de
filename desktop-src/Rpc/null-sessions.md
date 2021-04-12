---
title: Null-Sitzungen
description: Manchmal kann ein in der NULL-Sitzung eintreffenden Rückruf wie ein authentifizierter-Rückruf erscheinen.
ms.assetid: 5d113d20-c7af-4fb3-ba17-d0715671f290
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68fe0542d86dd2e6b903a08834293d6cc2f09828
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471660"
---
# <a name="null-sessions"></a><span data-ttu-id="7162f-103">Null-Sitzungen</span><span class="sxs-lookup"><span data-stu-id="7162f-103">Null Sessions</span></span>

<span data-ttu-id="7162f-104">Manchmal kann ein in der NULL-Sitzung eintreffenden Rückruf wie ein authentifizierter-Rückruf erscheinen.</span><span class="sxs-lookup"><span data-stu-id="7162f-104">Sometimes a call arriving on the null session can appear like an authenticated call.</span></span> <span data-ttu-id="7162f-105">Der Aufruf der [**rpcbindinginqauthclient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) -Funktion gibt insbesondere die Authentifizierungs Ebene und den Sicherheitsanbieter zurück, die für den Aufruf verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7162f-105">Specifically, calling the [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) function returns the authentication level and security provider used for the call.</span></span> <span data-ttu-id="7162f-106">Dieser Vorgang bedeutet nicht, dass der-Befehl nicht für eine NULL-Sitzung verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="7162f-106">This operation does not mean the call was not on a null session.</span></span> <span data-ttu-id="7162f-107">Die beiden Probleme sind orthogonal.</span><span class="sxs-lookup"><span data-stu-id="7162f-107">The two issues are orthogonal.</span></span> <span data-ttu-id="7162f-108">Bei Microsoft Windows 2000 kann ein Remote Prozedur Aufruf versuchen, die Identität eines Aufrufers anzunehmen und die Berechtigungen nach dem Identitätswechsel zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="7162f-108">On Microsoft Windows 2000, a remote procedure call can attempt to impersonate a caller and check the permissions after impersonation.</span></span> <span data-ttu-id="7162f-109">Unter Microsoft Windows XP ist es schneller, die [**rpcserverinqcallattribute**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) -Funktion aufzurufen und das **nullsession** -Flag zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="7162f-109">On Microsoft Windows XP, it is faster to call the [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) function and check for the **NullSession** flag.</span></span>

<span data-ttu-id="7162f-110">Ein weiterer relevanter Unterschied besteht zwischen Windows 2000 und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7162f-110">Another relevant difference exists between Windows 2000 and Windows XP.</span></span> <span data-ttu-id="7162f-111">Wenn nur das \_ Flag RPC if \_ Allow \_ Secure \_ only angegeben ist, werden Aufrufe in der NULL-Sitzung in Windows 2000 durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="7162f-111">If only the RPC\_IF\_ALLOW\_SECURE\_ONLY flag is specified, calls on the null session go through in Windows 2000.</span></span> <span data-ttu-id="7162f-112">In Windows XP werden bei der allgemeinen Verschärfung der Standard Sicherheitseinstellungen, wenn dieses Flag angegeben ist, Aufrufe der NULL-Sitzung mit "Zugriff verweigert" abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="7162f-112">In Windows XP, with the general tightening of default security settings, when this flag is specified, calls on the null session are rejected with access denied.</span></span> <span data-ttu-id="7162f-113">Allerdings \_ \_ \_ \_ garantiert RPC nicht die Berechtigungsebene des aufrufenden Benutzers, auch wenn der RPC-Flag "Secure Secure only" verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7162f-113">However, even with the RPC\_IF\_ALLOW\_SECURE\_ONLY flag, RPC does not guarantee the privilege level of the calling user.</span></span> <span data-ttu-id="7162f-114">Alle RPC-Überprüfungen sind, dass der Benutzer über gültige Anmelde Informationen verfügt.</span><span class="sxs-lookup"><span data-stu-id="7162f-114">All RPC checks is that the user has valid credentials.</span></span> <span data-ttu-id="7162f-115">Es ist möglich, dass der aufrufenden Benutzer das Gastkonto oder andere Konten mit niedrigen Berechtigungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="7162f-115">It is possible that the calling user is using the guest account or other low privileged accounts.</span></span> <span data-ttu-id="7162f-116">Stellen Sie sicher, dass der Server nicht über eine hohe Berechtigung verfügt, \_ Wenn RPC \_ \_ nur zulassen \_ verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7162f-116">Make sure the server does not assume high privilege once RPC\_IF\_ALLOW\_SECURE\_ONLY is used.</span></span>

 

 




