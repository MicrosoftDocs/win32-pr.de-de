---
description: Das setreg-Tool legt den Wert der Registrierungsschlüssel fest, die das Verhalten der Authenticode-Zertifikat Überprüfung steuern.
ms.assetid: c34c00fe-da99-4c2e-9e9a-0ef6406ae5ae
title: Verwenden von "abtreg"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 706463f86d38a03bc3416713be7427df55424d09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130237"
---
# <a name="using-setreg"></a><span data-ttu-id="dd5d5-103">Verwenden von "abtreg"</span><span class="sxs-lookup"><span data-stu-id="dd5d5-103">Using SetReg</span></span>

<span data-ttu-id="dd5d5-104">Das setreg-Tool legt den Wert der Registrierungsschlüssel fest, die das Verhalten der Authenticode-Zertifikat Überprüfung steuern.</span><span class="sxs-lookup"><span data-stu-id="dd5d5-104">The SetReg tool sets the value of the registry keys controlling the behavior of the Authenticode certificate verification process.</span></span> <span data-ttu-id="dd5d5-105">Diese Schlüssel, die als Software Publishing State Keys bezeichnet werden, Steuern, ob Sie einem Test Stamm Vertrauen, die Offline Genehmigung von Zertifikaten zulassen, Ablaufdaten für das Zertifikat testen und Sperr Überprüfungen durchführen.</span><span class="sxs-lookup"><span data-stu-id="dd5d5-105">These keys, called the Software Publishing State Keys, control whether to trust a test root, allow offline approval of certificates, test certificate expiration dates, and perform revocation checks.</span></span>

<span data-ttu-id="dd5d5-106">Der folgende Befehl listet die Syntax und die Optionen für die Verwendung von "\*" auf.</span><span class="sxs-lookup"><span data-stu-id="dd5d5-106">The following command lists the syntax and options for using SetReg.</span></span>

<span data-ttu-id="dd5d5-107">**-?**</span><span class="sxs-lookup"><span data-stu-id="dd5d5-107">**setreg -?**</span></span>

<span data-ttu-id="dd5d5-108">Mit dem folgenden Befehl wird ein Test Stamm als vertrauenswürdig eingestuft.</span><span class="sxs-lookup"><span data-stu-id="dd5d5-108">The following command makes a test root trusted.</span></span> <span data-ttu-id="dd5d5-109">Standardmäßig ist ein Test Stamm nicht vertrauenswürdig.</span><span class="sxs-lookup"><span data-stu-id="dd5d5-109">By default, a test root is not trusted.</span></span> <span data-ttu-id="dd5d5-110">Nachdem alle Änderungen an den Schlüsselwerten vorgenommen wurden, wird eine Liste mit dem aktuellen Wert aller Schlüsselwerte angezeigt.</span><span class="sxs-lookup"><span data-stu-id="dd5d5-110">After any changes in the key values are made, a list of the current value of all of the key values is displayed.</span></span> <span data-ttu-id="dd5d5-111">Wenn die Option **-q** verwendet wird, werden die Schlüsselwerte nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="dd5d5-111">If the **-q** option is used, the key values are not displayed.</span></span>

<span data-ttu-id="dd5d5-112">**Eing 1 true**</span><span class="sxs-lookup"><span data-stu-id="dd5d5-112">**setreg 1 TRUE**</span></span>

<span data-ttu-id="dd5d5-113">Der folgende Befehl erstellt einen Test Stamm als nicht vertrauenswürdig und bewirkt, dass die Überprüfung auf die Sperrung überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="dd5d5-113">The following command makes a test root untrusted and causes all verification to check for revocation.</span></span> <span data-ttu-id="dd5d5-114">Die Option " **-q** " wird verwendet, sodass die Liste der Schlüsselwerte nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="dd5d5-114">The **-q** option is used so that the list of key values is not displayed</span></span>

<span data-ttu-id="dd5d5-115">**Protokoll-q 1 false 3 true**</span><span class="sxs-lookup"><span data-stu-id="dd5d5-115">**setreg -q 1 FALSE 3 TRUE**</span></span>

> [!Note]  
> <span data-ttu-id="dd5d5-116">Bei Befehlen, Optionen und Argumenten wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="dd5d5-116">Commands, options, and arguments are not case sensitive.</span></span>

 

 

 



