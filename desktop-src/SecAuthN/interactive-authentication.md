---
description: Die Authentifizierung erfolgt interaktiv, wenn ein Benutzer zur Eingabe von Anmelde Informationen aufgefordert wird. Die lokale Sicherheits Autorität (Local Security Authority, LSA) führt eine interaktive Authentifizierung aus, wenn sich ein Benutzer über die Gina-Benutzeroberfläche anmeldet.
ms.assetid: 86a318fa-4d7c-4191-a309-d25b492dd915
title: Interaktive Authentifizierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afeb09044f4b34f28c02cd0f03b3358a8158af65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348059"
---
# <a name="interactive-authentication"></a><span data-ttu-id="aafef-104">Interaktive Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="aafef-104">Interactive Authentication</span></span>

<span data-ttu-id="aafef-105">Die Authentifizierung erfolgt interaktiv, wenn ein Benutzer zur Eingabe von Anmelde Informationen aufgefordert wird.</span><span class="sxs-lookup"><span data-stu-id="aafef-105">Authentication is interactive when a user is prompted to supply logon information.</span></span> <span data-ttu-id="aafef-106">Die [*Lokale Sicherheits Autorität (Local Security Authority*](../secgloss/l-gly.md) , LSA) führt eine interaktive Authentifizierung aus, wenn sich ein Benutzer über die [*Gina*](../secgloss/g-gly.md) -Benutzeroberfläche anmeldet.</span><span class="sxs-lookup"><span data-stu-id="aafef-106">The [*Local Security Authority*](../secgloss/l-gly.md) (LSA) performs an interactive authentication when a user logs on through the [*GINA*](../secgloss/g-gly.md) user interface.</span></span> <span data-ttu-id="aafef-107">Die folgende Abbildung zeigt die Teile einer typischen interaktiven Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="aafef-107">The following illustration shows the parts of a typical interactive authentication.</span></span>

![interaktive Authentifizierung](images/lsaint3.png)

<span data-ttu-id="aafef-109">Ein Benutzer signalisiert dem System, die Anmelde Sequenz zu starten, indem er die Tastenkombination STRG + ALT + ENTF ( [*Secure Attention Sequence*](../secgloss/s-gly.md) , SAS) eingibt.</span><span class="sxs-lookup"><span data-stu-id="aafef-109">A user signals the system to begin the logon sequence by typing the CTRL+ALT+DEL [*secure attention sequence*](../secgloss/s-gly.md) (SAS).</span></span> <span data-ttu-id="aafef-110">[*Winlogon*](../secgloss/w-gly.md) empfängt die SAS und ruft die Gina auf, um eine Benutzeroberfläche anzuzeigen und die Anmeldedaten des Benutzers zu erhalten, z. b. einen Benutzernamen und ein Kennwort.</span><span class="sxs-lookup"><span data-stu-id="aafef-110">[*Winlogon*](../secgloss/w-gly.md) receives the SAS and calls the GINA to display a user interface and obtain the user's logon data, such as a user name and password.</span></span>

<span data-ttu-id="aafef-111">Nachdem Sie die Anmeldedaten erhalten haben, ruft die Gina die [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) -Funktion auf, um den Benutzer zu authentifizieren. dabei wird angegeben, welches Authentifizierungs Paket zum Auswerten der Anmeldedaten verwendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="aafef-111">After obtaining the logon data, the GINA calls the [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) function to authenticate the user, specifying which authentication package must be used to evaluate the logon data.</span></span>

<span data-ttu-id="aafef-112">Der LSA Ruft das angegebene Authentifizierungs Paket auf und übergibt die Anmeldedaten an das Paket.</span><span class="sxs-lookup"><span data-stu-id="aafef-112">The LSA calls the specified authentication package and passes the logon data to it.</span></span> <span data-ttu-id="aafef-113">Das Authentifizierungs Paket überprüft die Daten und ermittelt, ob die Authentifizierung erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="aafef-113">The authentication package examines the data and determines whether the authentication is successful.</span></span> <span data-ttu-id="aafef-114">Das Authentifizierungs Ergebnis wird an die LSA und von der LSA an die Gina zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="aafef-114">The authentication result is returned to the LSA and from the LSA, to the GINA.</span></span>

<span data-ttu-id="aafef-115">Die Gina zeigt den Erfolg oder das Fehlschlagen der Authentifizierung für den Benutzer an und gibt das Ergebnis der Authentifizierung an Winlogon zurück.</span><span class="sxs-lookup"><span data-stu-id="aafef-115">The GINA displays the success or failure of the authentication to the user and returns the result of the authentication to Winlogon.</span></span> <span data-ttu-id="aafef-116">Wenn die Authentifizierung erfolgreich ist, beginnt die Anmelde Sitzung des Benutzers, und es wird ein Satz [*von Anmelde Informationen*](../secgloss/c-gly.md) für die spätere Referenz gespeichert.</span><span class="sxs-lookup"><span data-stu-id="aafef-116">If the authentication succeeds, the user's logon session begins and a set of logon [*credentials*](../secgloss/c-gly.md) are saved for future reference.</span></span>

> [!Note]  
> <span data-ttu-id="aafef-117">Im Allgemeinen müssen Entwickler, die eine benutzerdefinierte Gina schreiben, um spezialisierte Anmeldedaten zu akzeptieren, z. b. eine [*Smartcard*](../secgloss/s-gly.md) oder Daten zur Datenverarbeitung, auch ein Authentifizierungs Paketschreiben, das für die Verarbeitung dieser Daten und die Bestimmung der Echtheit zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="aafef-117">In general, a developer who writes a custom GINA to accept specialized logon data, such as a [*smart card*](../secgloss/s-gly.md) or retinal-scan data, must also write an authentication package responsible for processing that data and determining its authenticity.</span></span>

 

<span data-ttu-id="aafef-118">Weitere Informationen zu Winlogon und Ginas finden Sie unter [Winlogon und Gina](winlogon-and-gina.md).</span><span class="sxs-lookup"><span data-stu-id="aafef-118">For more information about Winlogon and GINAs, see [Winlogon and GINA](winlogon-and-gina.md).</span></span> <span data-ttu-id="aafef-119">Weitere Informationen zu Authentifizierungs Paketen finden Sie unter [Erstellen benutzerdefinierter Sicherheitspakete](creating-custom-security-packages.md).</span><span class="sxs-lookup"><span data-stu-id="aafef-119">For more information about authentication packages, see [Creating Custom Security Packages](creating-custom-security-packages.md).</span></span>

 

 
