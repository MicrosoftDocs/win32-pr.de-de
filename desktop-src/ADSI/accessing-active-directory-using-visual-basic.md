---
title: Zugreifen auf Active Directory mithilfe Visual Basic
description: Eines der leistungsfähigsten Features, das mit dem Betriebssystem Microsoft Windows 2000 verfügbar wurde, ist der Microsoft Active Directory Directory-Dienst.
ms.assetid: b5021e38-92a2-43d2-b3cb-15ff5c74c1d8
ms.tgt_platform: multiple
keywords:
- Zugreifen auf Active Directory mithilfe von Visual Basic ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bbc469de112c37c1c2ea5865d88252c4bd98466
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036331"
---
# <a name="accessing-active-directory-using-visual-basic"></a><span data-ttu-id="9af86-104">Zugreifen auf Active Directory mithilfe Visual Basic</span><span class="sxs-lookup"><span data-stu-id="9af86-104">Accessing Active Directory Using Visual Basic</span></span>

<span data-ttu-id="9af86-105">Eines der leistungsfähigsten Features, das mit dem Betriebssystem Microsoft Windows 2000 verfügbar wurde, ist der Microsoft Active Directory Directory-Dienst.</span><span class="sxs-lookup"><span data-stu-id="9af86-105">One of the most powerful features that became available with the Microsoft Windows 2000 operating system is the Microsoft Active Directory directory service.</span></span> <span data-ttu-id="9af86-106">Wenn Sie sich bei einer Windows 2000-Domäne anmelden, wird Active Directory in Aktion eingefügt. Wenn Sie in Ihrem Gebäude nach dem nächstgelegenen Farbdrucker suchen möchten, können Sie Active Directory verwenden.</span><span class="sxs-lookup"><span data-stu-id="9af86-106">When you log on to a Windows 2000 domain, Active Directory is put into action; to search for the closest color printer in your building, you can use Active Directory.</span></span> <span data-ttu-id="9af86-107">Sie kann für eine Adressbuchsuche oder eine Suche nach Benutzern verwendet werden, die in Gebäude 40 arbeiten.</span><span class="sxs-lookup"><span data-stu-id="9af86-107">It can be used for an address book lookup or a search for users who work in building 40.</span></span> <span data-ttu-id="9af86-108">Mit Active Directory können Sie eine Smartcard für die Anmeldung bei einer Windows 2000-Domäne verwenden.</span><span class="sxs-lookup"><span data-stu-id="9af86-108">With Active Directory, you can use a smart card to log on to a Windows 2000 domain.</span></span> <span data-ttu-id="9af86-109">Sie können sogar Daten aus Microsoft SQL Server Datenbanksoftware und Active Directory verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="9af86-109">You can even join data from Microsoft SQL Server database software and Active Directory.</span></span>

<span data-ttu-id="9af86-110">Viele andere Microsoft-Technologien, wie z. b. Microsoft Message Queue Server (MSMQ), com (Klassen Speicher), IPSec (Internet Protocol Security), Gruppenrichtlinie Objekte (GPOs) und Exchange sind in Active Directory integriert.</span><span class="sxs-lookup"><span data-stu-id="9af86-110">Many other Microsoft technologies, such as Microsoft Message Queue Server (MSMQ), COM (Class Store), Internet Protocol security (IPsec), Group Policy Objects (GPOs), and Exchange are integrated with Active Directory.</span></span>

<span data-ttu-id="9af86-111">In diesem Abschnitt wird erläutert, wie Sie den Active Directory Service Interfaces (ADSI) verwenden, um auf Active Directory zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="9af86-111">This section discusses how to use the Active Directory Service Interfaces (ADSI) to access Active Directory.</span></span> <span data-ttu-id="9af86-112">Verwenden eines Szenarios für ein fiktives Unternehmen – Fabrikam Corporation – Sie erfahren, wie Sie einige grundlegende administrative Aufgaben durchführen.</span><span class="sxs-lookup"><span data-stu-id="9af86-112">Using a scenario for a fictitious company — the Fabrikam Corporation — you will learn how to perform some basic administrative tasks.</span></span>

<span data-ttu-id="9af86-113">Wenn Sie dieses Szenario durchlaufen, werden die Codebeispiele in den einzelnen Abschnitten auf sich selbst erstellt.</span><span class="sxs-lookup"><span data-stu-id="9af86-113">As you progress through this scenario, the code examples in each section build upon themselves.</span></span>

<span data-ttu-id="9af86-114">Aus Gründen der Kürze werden alle Codebeispiele mit dem Microsoft Visual Basic-Entwicklungssystem geschrieben.</span><span class="sxs-lookup"><span data-stu-id="9af86-114">For brevity, all code examples are written with the Microsoft Visual Basic development system.</span></span> <span data-ttu-id="9af86-115">Weitere Informationen zur C++-Konvertierung finden [Sie unter Mapping ADSI Visual Basic Code to C++ Code](mapping-adsi-visual-basic-code-to-c-code.md).</span><span class="sxs-lookup"><span data-stu-id="9af86-115">For more information about C++ conversion, see [Mapping ADSI Visual Basic Code to C++ Code](mapping-adsi-visual-basic-code-to-c-code.md).</span></span>

 

 




