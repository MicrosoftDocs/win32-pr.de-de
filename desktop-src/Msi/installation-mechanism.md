---
description: 'Ein erfolgreicher Installationsvorgang besteht aus zwei Phasen: dem Erwerb und der Ausführung. Wenn die Installation nicht erfolgreich ist, kann eine Rollback Phase ausgeführt werden.'
ms.assetid: e9cda321-6978-4f9f-aff4-ccf609c88667
title: Installationsmechanismus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78455cb26e7672614266453e82f1a44c44e6b14d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348482"
---
# <a name="installation-mechanism"></a><span data-ttu-id="72fe9-104">Installationsmechanismus</span><span class="sxs-lookup"><span data-stu-id="72fe9-104">Installation Mechanism</span></span>

<span data-ttu-id="72fe9-105">Ein erfolgreicher Installationsvorgang besteht aus zwei Phasen: dem Erwerb und der Ausführung.</span><span class="sxs-lookup"><span data-stu-id="72fe9-105">There are two phases to a successful installation process: acquisition and execution.</span></span> <span data-ttu-id="72fe9-106">Wenn die Installation nicht erfolgreich ist, kann eine Rollback Phase ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="72fe9-106">If the installation is unsuccessful, a rollback phase may occur.</span></span>

## <a name="acquisition"></a><span data-ttu-id="72fe9-107">Erwerb</span><span class="sxs-lookup"><span data-stu-id="72fe9-107">Acquisition</span></span>

<span data-ttu-id="72fe9-108">Zu Beginn der Erwerbsphase weist eine Anwendung oder ein Benutzer das Installationsprogramm an, ein Feature oder eine Anwendung zu installieren.</span><span class="sxs-lookup"><span data-stu-id="72fe9-108">At the beginning of the acquisition phase, an application or a user instructs the installer to install a feature or an application.</span></span> <span data-ttu-id="72fe9-109">Der Installer durchläuft dann die Aktionen, die in den Sequenz Tabellen der-Installations Datenbank angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="72fe9-109">The installer then progresses through the actions specified in the sequence tables of the installation database.</span></span> <span data-ttu-id="72fe9-110">Diese Aktionen Fragen die Installations Datenbank ab und generieren ein Skript, das ein schrittweises Verfahren zum Ausführen der Installation ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="72fe9-110">These actions query the installation database and generate a script that gives a step-by-step procedure for performing the installation.</span></span>

## <a name="execution"></a><span data-ttu-id="72fe9-111">Ausführung</span><span class="sxs-lookup"><span data-stu-id="72fe9-111">Execution</span></span>

<span data-ttu-id="72fe9-112">Während der Ausführungsphase übergibt das Installationsprogramm die Informationen an einen Prozess mit erhöhten Rechten und führt das Skript aus.</span><span class="sxs-lookup"><span data-stu-id="72fe9-112">During the execution phase, the installer passes the information to a process with elevated privileges and runs the script.</span></span>

## <a name="rollback"></a><span data-ttu-id="72fe9-113">Rollback</span><span class="sxs-lookup"><span data-stu-id="72fe9-113">Rollback</span></span>

<span data-ttu-id="72fe9-114">Wenn eine Installation nicht erfolgreich ist, stellt das Installationsprogramm den ursprünglichen Zustand des Computers wieder her.</span><span class="sxs-lookup"><span data-stu-id="72fe9-114">If an installation is unsuccessful, the installer restores the original state of the computer.</span></span> <span data-ttu-id="72fe9-115">Wenn das Installationsprogramm das Installationsskript verarbeitet, generiert es gleichzeitig ein Rollback-Skript.</span><span class="sxs-lookup"><span data-stu-id="72fe9-115">When the installer processes the installation script it simultaneously generates a rollback script.</span></span> <span data-ttu-id="72fe9-116">Zusätzlich zum Rollback-Skript speichert das Installationsprogramm eine Kopie jeder Datei, die während der Installation gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="72fe9-116">In addition to the rollback script, the installer saves a copy of every file it deletes during the installation.</span></span> <span data-ttu-id="72fe9-117">Diese Dateien werden in einem verborgenen System Verzeichnis gespeichert.</span><span class="sxs-lookup"><span data-stu-id="72fe9-117">These files are kept in a hidden, system directory.</span></span> <span data-ttu-id="72fe9-118">Nach Abschluss der Installation werden das Rollback-Skript und die gespeicherten Dateien gelöscht.</span><span class="sxs-lookup"><span data-stu-id="72fe9-118">Once the installation is complete, the rollback script and the saved files are deleted.</span></span> <span data-ttu-id="72fe9-119">Weitere Informationen finden Sie unter [Rollback-Installation](rollback-installation.md).</span><span class="sxs-lookup"><span data-stu-id="72fe9-119">For more information, see [Rollback Installation](rollback-installation.md).</span></span>

 

 



