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
# <a name="assigning-privileges-to-an-account"></a>Zuweisen von Berechtigungen zu einem Konto

Sie können Konten entweder mithilfe der lokalen Sicherheitsrichtlinie Microsoft Management Console (MMC)-Snap-in (secpol. msc) oder durch Aufrufen der [**lsaaddaccounlenghts**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaaddaccountrights) -Funktion zuweisen.

Das Zuweisen einer Berechtigung zu einem Konto wirkt sich nicht auf vorhandene Benutzer Token aus. Ein Benutzer muss sich abmelden und dann wieder anmelden, um ein Zugriffs Token mit der neu zugewiesenen Berechtigung zu erhalten.

Wenn Sie mithilfe des MMC-Snap-Ins "lokale Sicherheitsrichtlinie" Berechtigungen zuweisen möchten, bearbeiten Sie die Liste der Benutzer für alle unter **Sicherheitseinstellungen/Lokale Richtlinien/Zuweisen von Benutzerrechten** aufgeführten Berechtigungen.

 

 
