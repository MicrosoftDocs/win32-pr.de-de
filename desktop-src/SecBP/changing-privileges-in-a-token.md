---
description: Erläutert das Ändern von Berechtigungen in einem Token mithilfe der Funktionen "" "" "" "" "" "" "" "" "" ""
ms.assetid: b8e47d04-07c1-4d57-8209-6b0c397476e5
title: Ändern von Berechtigungen in einem Token
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8b77d966acf90db101269b77a767550bcae3ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366167"
---
# <a name="changing-privileges-in-a-token"></a><span data-ttu-id="26713-103">Ändern von Berechtigungen in einem Token</span><span class="sxs-lookup"><span data-stu-id="26713-103">Changing Privileges in a Token</span></span>

<span data-ttu-id="26713-104">Sie können die Berechtigungen entweder in einem primären oder einem Identitätswechsel Token auf zwei Arten ändern:</span><span class="sxs-lookup"><span data-stu-id="26713-104">You can change the privileges in either a primary or an impersonation token in two ways:</span></span>

-   <span data-ttu-id="26713-105">Aktivieren oder deaktivieren Sie Berechtigungen mithilfe der Funktion "- [**tokenprivilegien**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) ".</span><span class="sxs-lookup"><span data-stu-id="26713-105">Enable or disable privileges by using the [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) function.</span></span>
-   <span data-ttu-id="26713-106">Einschränken oder Entfernen von Berechtigungen mithilfe der [**Funktion "**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) " von "".</span><span class="sxs-lookup"><span data-stu-id="26713-106">Restrict or remove privileges by using the [**CreateRestrictedToken**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) function.</span></span>

<span data-ttu-id="26713-107">[](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) "" "" "" "" "" "" "" "" "".</span><span class="sxs-lookup"><span data-stu-id="26713-107">[**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) cannot add or remove privileges from the token.</span></span> <span data-ttu-id="26713-108">Es können nur vorhandene Berechtigungen aktiviert werden, die zurzeit deaktiviert sind, oder vorhandene Berechtigungen deaktivieren, die derzeit aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="26713-108">It can only enable existing privileges that are currently disabled or disable existing privileges that are currently enabled.</span></span> <span data-ttu-id="26713-109">Beispiele finden Sie unter [aktivieren und Deaktivieren von Berechtigungen in C++](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--).</span><span class="sxs-lookup"><span data-stu-id="26713-109">For examples, see [Enabling and Disabling Privileges in C++](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--).</span></span>

<span data-ttu-id="26713-110">Informationen zum Zuweisen von Berechtigungen zu einem Benutzerkonto finden Sie unter [Zuweisen von Berechtigungen zu einem Konto](assigning-privileges-to-an-account.md).</span><span class="sxs-lookup"><span data-stu-id="26713-110">To assign privileges to a user account, see [Assigning Privileges to an Account](assigning-privileges-to-an-account.md).</span></span>

<span data-ttu-id="26713-111">" [**Kreaterestrictedtoken**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) " verfügt über umfangreichere Funktionen wie folgt:</span><span class="sxs-lookup"><span data-stu-id="26713-111">[**CreateRestrictedToken**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) has more extensive capabilities as follows:</span></span>

-   <span data-ttu-id="26713-112">Entfernen einer Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="26713-112">Removing a privilege.</span></span> <span data-ttu-id="26713-113">Beachten Sie, dass das Entfernen einer Berechtigung nicht mit der Deaktivierung einer Berechtigung identisch ist.</span><span class="sxs-lookup"><span data-stu-id="26713-113">Note that removing a privilege is not the same as disabling one.</span></span> <span data-ttu-id="26713-114">Nachdem eine Berechtigung aus einem Token entfernt wurde, kann Sie nicht wieder zurückgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="26713-114">After a privilege is removed from a token, it cannot be put back.</span></span>
-   <span data-ttu-id="26713-115">Das Deny-only-Attribut wird an SIDs im Token angefügt.</span><span class="sxs-lookup"><span data-stu-id="26713-115">Attaching the deny-only attribute to SIDs in the token.</span></span> <span data-ttu-id="26713-116">Dies hat den Effekt, dass bestimmte Gruppen oder Konten nicht zulässig sind, z. b. wenn die Gruppe "jeder" den Lösch Zugriff auf eine bestimmte Datei verweigert.</span><span class="sxs-lookup"><span data-stu-id="26713-116">This has the effect of disallowing specific groups or accounts, for example, denying the Everyone group delete access to a particular file.</span></span> <span data-ttu-id="26713-117">Weitere Informationen zum Einschränken von SIDs finden Sie unter [SID-Attribute in einem Zugriffs Token](/windows/desktop/SecAuthZ/sid-attributes-in-an-access-token).</span><span class="sxs-lookup"><span data-stu-id="26713-117">For more information on restricting SIDs, see [SID Attributes in an Access Token](/windows/desktop/SecAuthZ/sid-attributes-in-an-access-token).</span></span>
-   <span data-ttu-id="26713-118">Angeben einer Liste mit einschränkenden SIDs im Token.</span><span class="sxs-lookup"><span data-stu-id="26713-118">Specifying a list of restricting SIDs in the token.</span></span> <span data-ttu-id="26713-119">Informationen zum Einschränken von SIDs finden Sie unter [Eingeschränkte Token](/windows/desktop/SecAuthZ/restricted-tokens).</span><span class="sxs-lookup"><span data-stu-id="26713-119">For information about restricting SIDs, see [Restricted Tokens](/windows/desktop/SecAuthZ/restricted-tokens).</span></span>

 

 
