---
description: SID-Komponenten
ms.assetid: 528412e7-c2b6-4ddd-86de-999252972421
title: SID-Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbd44d0534cc56c6ef998c150810f14b3eda289d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041831"
---
# <a name="sid-components"></a><span data-ttu-id="8920d-103">SID-Komponenten</span><span class="sxs-lookup"><span data-stu-id="8920d-103">SID Components</span></span>

<span data-ttu-id="8920d-104">Ein SID-Wert enthält Komponenten, die Informationen über die [**sid**](/windows/desktop/api/Winnt/ns-winnt-sid) -Struktur und die Komponenten bereitstellen, die einen Vertrauens nehmer eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8920d-104">A SID value includes components that provide information about the [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid) structure and components that uniquely identify a trustee.</span></span> <span data-ttu-id="8920d-105">Eine SID besteht aus den folgenden Komponenten:</span><span class="sxs-lookup"><span data-stu-id="8920d-105">A SID consists of the following components:</span></span>

-   <span data-ttu-id="8920d-106">Die Revisions Ebene der [**sid**](/windows/desktop/api/Winnt/ns-winnt-sid) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="8920d-106">The revision level of the [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid) structure</span></span>
-   <span data-ttu-id="8920d-107">Ein 48-Bit-bezeichnerautoritäts Wert, der die Autorität identifiziert, die die SID ausgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="8920d-107">A 48-bit identifier authority value that identifies the authority that issued the SID</span></span>
-   <span data-ttu-id="8920d-108">Eine Variable Anzahl von untergeordneten or-Rid-Werten ( [*relative Identifier*](/windows/desktop/SecGloss/r-gly) ), die den Vertrauens nehmer relativ zur Zertifizierungsstelle eindeutig identifizieren, die die SID ausgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="8920d-108">A variable number of subauthority or [*relative identifier*](/windows/desktop/SecGloss/r-gly) (RID) values that uniquely identify the trustee relative to the authority that issued the SID</span></span>

<span data-ttu-id="8920d-109">Durch die Kombination aus dem Wert der bezeichnerbehörde und den Werten der untergeordneten Instanz wird sichergestellt, dass keine zwei SIDs identisch sind, auch wenn zwei verschiedene sid-ausstellende Autoritäten die gleiche Kombination von RID-Werten ausgeben.</span><span class="sxs-lookup"><span data-stu-id="8920d-109">The combination of the identifier authority value and the subauthority values ensures that no two SIDs will be the same, even if two different SID-issuing authorities issue the same combination of RID values.</span></span> <span data-ttu-id="8920d-110">Jede sid-ausstellende Behörde gibt eine bestimmte Rid nur einmal aus.</span><span class="sxs-lookup"><span data-stu-id="8920d-110">Each SID-issuing authority issues a given RID only once.</span></span>

<span data-ttu-id="8920d-111">SIDs werden im Binärformat in einer [**sid**](/windows/desktop/api/Winnt/ns-winnt-sid) -Struktur gespeichert.</span><span class="sxs-lookup"><span data-stu-id="8920d-111">SIDs are stored in binary format in a [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid) structure.</span></span> <span data-ttu-id="8920d-112">Um eine SID anzuzeigen, können Sie die [**ConvertSidToStringSid**](/windows/desktop/api/Sddl/nf-sddl-convertsidtostringsida) -Funktion aufrufen, um eine binäre SID in ein Zeichen folgen Format zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="8920d-112">To display a SID, you can call the [**ConvertSidToStringSid**](/windows/desktop/api/Sddl/nf-sddl-convertsidtostringsida) function to convert a binary SID to string format.</span></span> <span data-ttu-id="8920d-113">Wenn Sie eine SID-Zeichenfolge zurück in eine gültige, funktionale sid konvertieren möchten, müssen Sie die [**convertstringsidto sid**](/windows/desktop/api/Sddl/nf-sddl-convertstringsidtosida) -Funktion abrufen.</span><span class="sxs-lookup"><span data-stu-id="8920d-113">To convert a SID string back to a valid, functional SID, call the [**ConvertStringSidToSid**](/windows/desktop/api/Sddl/nf-sddl-convertstringsidtosida) function.</span></span>

<span data-ttu-id="8920d-114">Diese Funktionen verwenden die folgende standardisierte Zeichen folgen Notation für SIDs, wodurch die Visualisierung Ihrer Komponenten vereinfacht wird:</span><span class="sxs-lookup"><span data-stu-id="8920d-114">These functions use the following standardized string notation for SIDs, which makes it simpler to visualize their components:</span></span>

<span data-ttu-id="8920d-115">s-*R* - *I* - *s*...</span><span class="sxs-lookup"><span data-stu-id="8920d-115">S-*R*-*I*-*S*…</span></span>

<span data-ttu-id="8920d-116">In dieser Notation identifiziert das Literalzeichen "S" die Reihen der Ziffern als sid, *R* die Revisions Ebene, *Ich bin* der Wert der Bezeichnerautorität und *S*...</span><span class="sxs-lookup"><span data-stu-id="8920d-116">In this notation, the literal character "S" identifies the series of digits as a SID, *R* is the revision level, *I* is the identifier-authority value, and *S*…</span></span> <span data-ttu-id="8920d-117">ist ein oder mehrere subauthority-Werte.</span><span class="sxs-lookup"><span data-stu-id="8920d-117">is one or more subauthority values.</span></span>

<span data-ttu-id="8920d-118">Im folgenden Beispiel wird diese Notation verwendet, um die bekannte Domänen relative SID der lokalen Administrator Gruppe anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="8920d-118">The following example uses this notation to display the well-known domain-relative SID of the local Administrators group:</span></span>

<span data-ttu-id="8920d-119">S-1-5-32-544</span><span class="sxs-lookup"><span data-stu-id="8920d-119">S-1-5-32-544</span></span>

<span data-ttu-id="8920d-120">In diesem Beispiel verfügt die SID über die folgenden Komponenten.</span><span class="sxs-lookup"><span data-stu-id="8920d-120">In this example, the SID has the following components.</span></span> <span data-ttu-id="8920d-121">Die Konstanten in Klammern sind bekannte Bezeichnerautorität und [*RID*](/windows/desktop/SecGloss/r-gly) -Werte, die in "Winnt. h" definiert sind:</span><span class="sxs-lookup"><span data-stu-id="8920d-121">The constants in parentheses are well-known identifier authority and [*RID*](/windows/desktop/SecGloss/r-gly) values defined in Winnt.h:</span></span>

-   <span data-ttu-id="8920d-122">Eine Revisions Ebene von 1</span><span class="sxs-lookup"><span data-stu-id="8920d-122">A revision level of 1</span></span>
-   <span data-ttu-id="8920d-123">Ein bezeichnerautoritäts Wert von 5 (Sicherheits- \_ NT- \_ Autorität)</span><span class="sxs-lookup"><span data-stu-id="8920d-123">An identifier-authority value of 5 (SECURITY\_NT\_AUTHORITY)</span></span>
-   <span data-ttu-id="8920d-124">Der erste subauthority-Wert 32 ( \_ sicherheitsbuiltin \_ Domäne \_ RID)</span><span class="sxs-lookup"><span data-stu-id="8920d-124">A first subauthority value of 32 (SECURITY\_BUILTIN\_DOMAIN\_RID)</span></span>
-   <span data-ttu-id="8920d-125">Eine zweite untergeordnete Instanz von 544 (Domänenalias- \_ \_ \_ Admins)</span><span class="sxs-lookup"><span data-stu-id="8920d-125">A second subauthority value of 544 (DOMAIN\_ALIAS\_RID\_ADMINS)</span></span>

 

 
