---
description: Sie können Konten entweder mithilfe der lokalen Sicherheitsrichtlinie Microsoft Management Console (MMC)-Snap-in (secpol. msc) oder durch Aufrufen der lsaaddaccounlenghts-Funktion zuweisen.
ms.assetid: F2DAB2E3-8B24-49A3-A2DD-E83B5181E9A2
title: Zuweisen von Berechtigungen zu einem Konto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0865a59b8bad75e687fd12f6bfc42c2cd39f664d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363624"
---
# <a name="assigning-privileges-to-an-account"></a><span data-ttu-id="cd2af-103">Zuweisen von Berechtigungen zu einem Konto</span><span class="sxs-lookup"><span data-stu-id="cd2af-103">Assigning Privileges to an Account</span></span>

<span data-ttu-id="cd2af-104">Sie können Konten entweder mithilfe der lokalen Sicherheitsrichtlinie Microsoft Management Console (MMC)-Snap-in (secpol. msc) oder durch Aufrufen der [**lsaaddaccounlenghts**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaaddaccountrights) -Funktion zuweisen.</span><span class="sxs-lookup"><span data-stu-id="cd2af-104">You can assign privileges to accounts either by using the Local Security Policy Microsoft Management Console (MMC) snap-in (Secpol.msc) or by calling the [**LsaAddAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaaddaccountrights) function.</span></span>

<span data-ttu-id="cd2af-105">Das Zuweisen einer Berechtigung zu einem Konto wirkt sich nicht auf vorhandene Benutzer Token aus.</span><span class="sxs-lookup"><span data-stu-id="cd2af-105">Assigning a privilege to an account does not affect existing user tokens.</span></span> <span data-ttu-id="cd2af-106">Ein Benutzer muss sich abmelden und dann wieder anmelden, um ein Zugriffs Token mit der neu zugewiesenen Berechtigung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="cd2af-106">A user must log off and then log back on to get an access token with the newly assigned privilege.</span></span>

<span data-ttu-id="cd2af-107">Wenn Sie mithilfe des MMC-Snap-Ins "lokale Sicherheitsrichtlinie" Berechtigungen zuweisen möchten, bearbeiten Sie die Liste der Benutzer für alle unter **Sicherheitseinstellungen/Lokale Richtlinien/Zuweisen von Benutzerrechten** aufgeführten Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="cd2af-107">To assign privileges by using the Local Security Policy MMC snap-in, edit the list of users for each privilege listed under **Security Settings/Local Policies/User Rights Assignment**.</span></span>

 

 
