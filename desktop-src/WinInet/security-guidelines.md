---
title: Sicherheitsrichtlinie
description: Es ist wichtig, den Benutzer über mögliche Sicherheitsprobleme auf dem Laufenden zu halten.
ms.assetid: f0c041fd-3cc5-491e-b088-6c93fcd61def
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3d4214ba4582394ed555bafd58551e8b047493
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102110"
---
# <a name="security-guideline"></a><span data-ttu-id="58b91-103">Sicherheitsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="58b91-103">Security Guideline</span></span>

<span data-ttu-id="58b91-104">Es ist wichtig, den Benutzer über mögliche Sicherheitsprobleme auf dem Laufenden zu halten.</span><span class="sxs-lookup"><span data-stu-id="58b91-104">It is important to keep the user informed about possible security issues.</span></span>

## <a name="notify-the-user-of-security-related-events"></a><span data-ttu-id="58b91-105">Benachrichtigen des Benutzers über Security-Related-Ereignisse</span><span class="sxs-lookup"><span data-stu-id="58b91-105">Notify the User of Security-Related Events</span></span>

<span data-ttu-id="58b91-106">Benachrichtigen Sie den Benutzer stets über jegliche Änderung der Sicherheit, ob es sich um einen sicherheitsbezogenen Fehler wie einen Zertifikat Fehler oder eine Änderung der Sicherheit des zugrunde liegenden Protokolls handelt, z. b. eine Änderung von einer HTTPS-Site zu einer HTTP-Site.</span><span class="sxs-lookup"><span data-stu-id="58b91-106">Always notify the user of any change in security, whether it is a security-related error such as a certificate failure, or a change in the security of the underlying protocol, such as change from an HTTPS site to an HTTP site.</span></span>

## <a name="notify-the-user-of-security-related-errors"></a><span data-ttu-id="58b91-107">Benachrichtigen des Benutzers über Security-Related Fehler</span><span class="sxs-lookup"><span data-stu-id="58b91-107">Notify the User of Security-Related Errors</span></span>

<span data-ttu-id="58b91-108">Wenn Ihre Anwendung eine Fehlermeldung empfängt, die möglicherweise auf ein Sicherheitsproblem hinweist, stellt die **internetterrordlg** -Funktion eine standardmäßige, vertraute Schnittstelle zum Benachrichtigen des Benutzers in den meisten Fällen bereit.</span><span class="sxs-lookup"><span data-stu-id="58b91-108">When your application receives an error message that may indicate a security problem, the **InternetErrorDlg** function provides a standard, familiar interface for notifying the user in most cases.</span></span>

<span data-ttu-id="58b91-109">Zu den Fehlern, die in diese Kategorie fallen, zählen die folgenden:</span><span class="sxs-lookup"><span data-stu-id="58b91-109">Among the errors that fall in this category are:</span></span>

<span data-ttu-id="58b91-110">**Fehler " \_ Internet \_ http \_ zu https" \_ \_ beim \_ redir**</span><span class="sxs-lookup"><span data-stu-id="58b91-110">**ERROR\_INTERNET\_HTTP\_TO\_HTTPS\_ON\_REDIR**</span></span>

<span data-ttu-id="58b91-111">**Fehler beim \_ Internet \_ ungültige Zertifizierungsstelle \_**</span><span class="sxs-lookup"><span data-stu-id="58b91-111">**ERROR\_INTERNET\_INVALID\_CA**</span></span>

<span data-ttu-id="58b91-112">**Fehler " \_ Internet \_ Post" \_ ist \_ nicht \_ sicher.**</span><span class="sxs-lookup"><span data-stu-id="58b91-112">**ERROR\_INTERNET\_POST\_IS\_NON\_SECURE**</span></span>

<span data-ttu-id="58b91-113">**Fehler \_ Internet \_ Sek. \_ CERT- \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="58b91-113">**ERROR\_INTERNET\_SEC\_CERT\_ERRORS**</span></span>

<span data-ttu-id="58b91-114">**Fehler \_ Internet \_ sec \_ CERT \_ CN ist \_ ungültig.**</span><span class="sxs-lookup"><span data-stu-id="58b91-114">**ERROR\_INTERNET\_SEC\_CERT\_CN\_INVALID**</span></span>

<span data-ttu-id="58b91-115">**Fehler \_ Internet \_ Sek. \_ CERT- \_ Datum \_ ungültig**</span><span class="sxs-lookup"><span data-stu-id="58b91-115">**ERROR\_INTERNET\_SEC\_CERT\_DATE\_INVALID**</span></span>

<span data-ttu-id="58b91-116">Ein Fehler bei der Benachrichtigung des Benutzers über Fehler, wie z. b. diese, kann den Benutzer für verschiedene Arten von Sicherheitsverletzungen verfügbar machen, einschließlich Spoofing-Angriffe oder unfreiwilligen Offenlegung von Informationen.</span><span class="sxs-lookup"><span data-stu-id="58b91-116">A failure to notify the user of errors such as these can expose the user to various sorts of security breaches, including spoofing attacks or involuntary information disclosure.</span></span>

## <a name="notify-the-user-when-connection-security-changes"></a><span data-ttu-id="58b91-117">Benutzer benachrichtigen, wenn sich die Verbindungssicherheit ändert</span><span class="sxs-lookup"><span data-stu-id="58b91-117">Notify the User When Connection Security Changes</span></span>

<span data-ttu-id="58b91-118">Benachrichtigen Sie den Benutzer immer, wenn die Sicherheit der Verbindung geändert wird, z. b. von HTTPS zu http.</span><span class="sxs-lookup"><span data-stu-id="58b91-118">Always notify the user when the security of the connection changes, for example from HTTPS to HTTP.</span></span> <span data-ttu-id="58b91-119">Andernfalls verbergen Sie die Risiken der Offenlegung unfreiwilliger Informationen, es sei denn, der Benutzer hat explizit entschieden, nicht über solche Änderungen benachrichtigt zu werden.</span><span class="sxs-lookup"><span data-stu-id="58b91-119">Otherwise, unless the user has explicitly chosen not to be notified of such changes, you are concealing the risks of involuntary information disclosure.</span></span>

<span data-ttu-id="58b91-120">Zu den Funktionen, die eine solche Änderung der Verbindungssicherheit melden, gehören die **Internetstatus Callback** -Rückruffunktion und die **internetconfirmzonecrossing** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="58b91-120">Among the functions that report such a change in connection security are the **InternetStatusCallback** callback function and the **InternetConfirmZoneCrossing** function.</span></span>

> [!Note]  
> <span data-ttu-id="58b91-121">WinInet unterstützt keine Server Implementierungen.</span><span class="sxs-lookup"><span data-stu-id="58b91-121">WinINet does not support server implementations.</span></span> <span data-ttu-id="58b91-122">Außerdem sollte Sie nicht von einem Dienst verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="58b91-122">In addition, it should not be used from a service.</span></span> <span data-ttu-id="58b91-123">Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="58b91-123">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 