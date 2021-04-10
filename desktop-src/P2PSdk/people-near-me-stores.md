---
description: Personen in meiner Umgebung speichern
ms.assetid: 3f2aa9bd-49ca-4fa6-b718-7cbeeef857c7
title: Personen in meiner Umgebung speichern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d18bf60e43aba278862fbd19f3c8909e344bc67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866695"
---
# <a name="people-near-me-stores"></a><span data-ttu-id="76cf4-103">Personen in meiner Umgebung speichern</span><span class="sxs-lookup"><span data-stu-id="76cf4-103">People Near Me Stores</span></span>

<span data-ttu-id="76cf4-104">Anwendungen, die [Personen in meiner](about-people-near-me.md) Umgebung (PNM) unterstützen, können die folgenden Datenspeicher verwenden:</span><span class="sxs-lookup"><span data-stu-id="76cf4-104">Applications capable of [People Near Me](about-people-near-me.md) (PNM) can use the following data stores:</span></span>

### <a name="windows-address-book"></a><span data-ttu-id="76cf4-105">Windows-Adressbuch</span><span class="sxs-lookup"><span data-stu-id="76cf4-105">Windows Address Book</span></span>

<span data-ttu-id="76cf4-106">Das Windows-Adressbuch speichert Informationen zu Kontakten und Ihren digitalen Zertifikaten.</span><span class="sxs-lookup"><span data-stu-id="76cf4-106">The Windows Address Book stores information on contacts and their digital certificates.</span></span> <span data-ttu-id="76cf4-107">Der Kontakt "**Me**", der den derzeit angemeldeten Benutzer darstellt, wird ebenfalls im Windows-Adressbuch gespeichert.</span><span class="sxs-lookup"><span data-stu-id="76cf4-107">The '**Me**' contact, representing the currently logged in user, is also stored in the Windows Address Book.</span></span>

### <a name="certificate-store"></a><span data-ttu-id="76cf4-108">Zertifikatspeicher</span><span class="sxs-lookup"><span data-stu-id="76cf4-108">Certificate Store</span></span>

<span data-ttu-id="76cf4-109">Der Zertifikat Speicher enthält das selbst signierte Zertifikat für den "**Me**"-Kontakt.</span><span class="sxs-lookup"><span data-stu-id="76cf4-109">The Certificate Store contains the self-signed certificate for the '**Me**' contact.</span></span>

### <a name="application-store"></a><span data-ttu-id="76cf4-110">Anwendungsstore</span><span class="sxs-lookup"><span data-stu-id="76cf4-110">Application Store</span></span>

<span data-ttu-id="76cf4-111">Ein Anwendungsinstallations Programm registriert eine Anwendung bei PNM während des Installationsvorgangs.</span><span class="sxs-lookup"><span data-stu-id="76cf4-111">An application installer registers an application with PNM during the installation process.</span></span> <span data-ttu-id="76cf4-112">Dabei handelt es sich um Objekte, die von anderen Benutzern durchsucht werden können, wenn versucht wird, eine Verbindung mit einem Benutzer mit einer allgemeinen Anwendung herzustellen, z. b. einem Computerspiel.</span><span class="sxs-lookup"><span data-stu-id="76cf4-112">These are the objects that can be searched for by other users when attempting to connect to a user with a common application, such as a computer game.</span></span> <span data-ttu-id="76cf4-113">Der Anwendungs Speicher enthält für jede Anwendung den Namen der Anwendung, eine Globally Unique Identifier (GUID), einen Bereich der Anwendung, eine Beschreibung und einen Pfad zur ausführbaren Datei des Programms.</span><span class="sxs-lookup"><span data-stu-id="76cf4-113">For each application, the Application Store contains the name of the application, a globally unique identifier (GUID), a scope of the application, a description, and a path to the executable file of the program.</span></span> <span data-ttu-id="76cf4-114">Der Geltungsbereich einer Anwendung kann auf keine (nicht angekündigt), Personen in der Nähe (angekündigt im lokalen Subnetz), Kontakte (angekündigt nur für Kontakte) oder alle (angekündigt im lokalen Subnetz und für Kontakte) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="76cf4-114">The scope of an application can be set to None (not advertised), People Near Me (advertised on the local subnet), Contacts (advertised just for contacts), or All (advertised on the local subnet and for contacts).</span></span> <span data-ttu-id="76cf4-115">Der Anwendungs Speicher befindet sich in der Windows Vista-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="76cf4-115">The Application Store is located in the Windows Vista registry.</span></span>

 

 



