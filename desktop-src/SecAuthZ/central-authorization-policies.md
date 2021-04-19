---
description: Eine zentrale Autorisierungs Richtlinie (Cap) sammelt die spezifischen Autorisierungs Regeln (caprs) in einer einzelnen Richtlinie.
ms.assetid: E3E43D9F-6826-468A-86E9-AC8F9A381FD4
title: Zentrale Autorisierungs Richtlinien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b890236b0dae0f8f8d51254def4e1607cc35894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347025"
---
# <a name="central-authorization-policies"></a><span data-ttu-id="c19d9-103">Zentrale Autorisierungs Richtlinien</span><span class="sxs-lookup"><span data-stu-id="c19d9-103">Central Authorization Policies</span></span>

<span data-ttu-id="c19d9-104">Eine zentrale Autorisierungs Richtlinie (Cap) sammelt die spezifischen Autorisierungs Regeln (caprs) in einer einzelnen Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="c19d9-104">A Central Authorization Policy (CAP) collects the specific authorization rules (CAPRs) into a single policy.</span></span> <span data-ttu-id="c19d9-105">Damit die spezifischen Autorisierungs Regeln (caprs) in der ganzheitlichen Autorisierungs Richtlinie der Organisation zusammengefasst werden können, kann auf caprs zusammen verwiesen und auf einen Satz von Ressourcen angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="c19d9-105">To allow the specific authorization rules (CAPRs) to be combined into the holistic authorization policy of the organization, CAPRs can be referenced together and applied to a set of resources.</span></span> <span data-ttu-id="c19d9-106">Dies erfolgt durch das Erfassen mehrerer (als Verweis) in eine Obergrenze.</span><span class="sxs-lookup"><span data-stu-id="c19d9-106">This is done by collecting multiple (by reference) into a CAP.</span></span> <span data-ttu-id="c19d9-107">Sobald eine Obergrenze definiert ist, kann Sie von Ressourcen-Managern genutzt werden, um die Autorisierungs Richtlinie für Organisationen auf Ressourcen anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="c19d9-107">Once a CAP is defined it can be distributed consumed by resource managers to apply the organizations authorization policy to resources.</span></span>

<span data-ttu-id="c19d9-108">Eine Obergrenze hat die folgenden Attribute:</span><span class="sxs-lookup"><span data-stu-id="c19d9-108">A CAP has the following attributes:</span></span>

-   <span data-ttu-id="c19d9-109">Sammlung von caprs – eine Liste mit Verweisen auf vorhandene Capr-Objekte</span><span class="sxs-lookup"><span data-stu-id="c19d9-109">Collection of CAPRs – a list of references to existing CAPR objects</span></span>
-   <span data-ttu-id="c19d9-110">Ein Bezeichner (SID)</span><span class="sxs-lookup"><span data-stu-id="c19d9-110">An identifier (Sid)</span></span>
-   <span data-ttu-id="c19d9-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c19d9-111">Description</span></span>
-   <span data-ttu-id="c19d9-112">Name</span><span class="sxs-lookup"><span data-stu-id="c19d9-112">Name</span></span>

<span data-ttu-id="c19d9-113">Eine Obergrenze wird während der Zugriffs Auswertung für Dateien und Ordner ausgewertet, in denen Sie von einem Administrator aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="c19d9-113">A CAP is evaluated during access evaluation for files and folders on which an administrator enables it.</span></span> <span data-ttu-id="c19d9-114">Während eines [**Access Check**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) -Aufrufes wird die Cap-Prüfung logisch mit der Überprüfung der freigegebenen Zugriffs Steuerungs Liste kombiniert. Dies bedeutet, dass ein Benutzer für den Zugriff auf eine Datei, auf die das Cap angewendet wird, über Zugriff verfügen muss, und zwar gemäß der Obergrenze (zugeordneten caprs) und der freigegebenen ACL für die Datei.</span><span class="sxs-lookup"><span data-stu-id="c19d9-114">During an [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) call, the CAP check is logically combined with the discretionary ACL check; this means that in order to obtain access to a file to which the CAP applies, a user needs to have access both according to the CAP (its associated CAPRs) and the discretionary ACL on the file.</span></span>

<span data-ttu-id="c19d9-115">Beispiel Obergrenze:</span><span class="sxs-lookup"><span data-stu-id="c19d9-115">Example CAP:</span></span>

``` syntax
CORPORATE-FINANCE-CAP]
CAPID=S-1-5-3-4-56-45-67-123
Policies=HBI-CAPE;RETENTION-CAPR
```

## <a name="cap-definition"></a><span data-ttu-id="c19d9-116">Cap-Definition</span><span class="sxs-lookup"><span data-stu-id="c19d9-116">CAP Definition</span></span>

<span data-ttu-id="c19d9-117">Eine Obergrenze wird in Active Directory mithilfe einer neuen Benutzeroberfläche in ADAC (oder PowerShell) erstellt und bearbeitet, die es dem Administrator ermöglicht, eine Obergrenze zu erstellen und einen Satz von caprs anzugeben, die die Obergrenze bilden.</span><span class="sxs-lookup"><span data-stu-id="c19d9-117">A CAP is created and edited in Active Directory using a new UX in ADAC (or PowerShell) that allows the administrator to create a CAP and specify a set of CAPRs that make up the CAP.</span></span>

 

 
