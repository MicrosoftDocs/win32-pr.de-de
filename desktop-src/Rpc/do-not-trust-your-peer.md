---
title: Ihren Peer nicht als vertrauenswürdig einstufen
description: '\ 0034; dem Peer nicht Vertrauen \ 0034; ist eine grundlegende Sicherheitsregel, die jedoch oft übersehen wird.'
ms.assetid: 776c1c99-feb1-415c-9a18-e9bf581bc3ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4c5c7ba3760e14a66fb4765000c7a6698599b50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709965"
---
# <a name="do-not-trust-your-peer"></a><span data-ttu-id="c3960-103">Ihren Peer nicht als vertrauenswürdig einstufen</span><span class="sxs-lookup"><span data-stu-id="c3960-103">Do Not Trust Your Peer</span></span>

<span data-ttu-id="c3960-104">"Ihr Peer nicht als vertrauenswürdig einstufen" ist eine grundlegende Sicherheitsregel, die jedoch oft übersehen wird.</span><span class="sxs-lookup"><span data-stu-id="c3960-104">"Do not trust your peer" is a basic security rule, but it is often overlooked.</span></span> <span data-ttu-id="c3960-105">Gehen Sie nicht davon aus, dass sich die andere Partei in einer Kommunikation ordnungsgemäß verhält, und gehen Sie nicht davon aus, dass Ihr Peer die erwarteten Daten übergibt.</span><span class="sxs-lookup"><span data-stu-id="c3960-105">Do not assume the other party in a communication will behave properly, and do not assume your peer will pass the data you expect.</span></span> <span data-ttu-id="c3960-106">In der Mitte und in RPC werden in Ihrem Namen einige Überprüfungen durchgeführt, aber nicht alle Prüfungen.</span><span class="sxs-lookup"><span data-stu-id="c3960-106">MIDL and RPC perform some checks on your behalf, but not all checks.</span></span>

<span data-ttu-id="c3960-107">Stellen Sie fest, welcher Aspekt der Parameter von "Mittel l" oder "RPC" überprüft wird und welche Aspekte Sie selbst überprüfen müssen.</span><span class="sxs-lookup"><span data-stu-id="c3960-107">Know which aspect of the parameters are verified by MIDL or RPC, and which aspects you must verify yourself.</span></span> <span data-ttu-id="c3960-108">Beispielsweise prüft RPC bei in/out-Kontext Handles, ob das Kontext Handle kein Ungültiger Wert ungleich NULL ist.</span><span class="sxs-lookup"><span data-stu-id="c3960-108">For example, for in/out context handles, RPC verifies the context handle is not an invalid non-null value.</span></span> <span data-ttu-id="c3960-109">Sie lässt NULL-Werte und gültige Werte zu, aber viele Entwickler sind nicht darauf aufmerksam, dass NULL-Werte durchgelassen werden.</span><span class="sxs-lookup"><span data-stu-id="c3960-109">It allows null values and valid values, but many developers are not aware that null values are let through.</span></span> <span data-ttu-id="c3960-110">Dies soll überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="c3960-110">This is something to check for.</span></span>

<span data-ttu-id="c3960-111">Selbst wenn Sie Ihrem Peer im allgemeinen Vertrauen, stellen Sie sicher, dass keine neuen Pfade eingeführt werden, mit denen ein kompromittiertes Computer-oder Prinzipal Konto andere Computer angreifen kann.</span><span class="sxs-lookup"><span data-stu-id="c3960-111">Even if you generally trust your peer, be sure not to introduce new paths by which a compromised machine or principal account can attack other machines.</span></span> <span data-ttu-id="c3960-112">Angenommen, ein Benutzer wählt seinen Geburtstag als Kennwort aus, und er wird von einem Angreifer erraten.</span><span class="sxs-lookup"><span data-stu-id="c3960-112">Imagine that a user chooses his birthday as his password, and it is guessed by an attacker.</span></span> <span data-ttu-id="c3960-113">Auch nachdem Anforderungen des Benutzers authentifiziert wurden und der Zugriff auf seine Daten zulässig ist, stellen Sie sicher, dass keine ausnutzbaren Sicherheitsrisiken vorhanden sind. diese Stapel Überläufe können einem Angreifer ermöglichen, die Kontrolle über den Server zu übernehmen und die Sicherheitsverletzung zu verlängern.</span><span class="sxs-lookup"><span data-stu-id="c3960-113">Even after requests from the user are authenticated and access to his data is allowed, make sure exploitable vulnerabilities do not exist, such stack overruns that may allow an attacker to take control of your server and extend the security breach.</span></span>

 

 




