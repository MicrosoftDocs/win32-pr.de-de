---
description: Sie können Konten Berechtigungen zuweisen, indem Sie entweder das MMC-Snap-In (Local Security Policy Microsoft Management Console) (Secpol.msc) verwenden oder die LsaAddAccountRights-Funktion aufrufen.
ms.assetid: F2DAB2E3-8B24-49A3-A2DD-E83B5181E9A2
title: Zuweisen von Berechtigungen zu einem Konto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a4ba4fb5266a66aac67b17c70fc6bbcaa1a397a8593534144c688daaee5a0b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119623010"
---
# <a name="assigning-privileges-to-an-account"></a>Zuweisen von Berechtigungen zu einem Konto

Sie können Konten Berechtigungen zuweisen, indem Sie entweder das MMC-Snap-In (Local Security Policy Microsoft Management Console) (Secpol.msc) verwenden oder die [**LsaAddAccountRights-Funktion**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaaddaccountrights) aufrufen.

Das Zuweisen einer Berechtigung zu einem Konto wirkt sich nicht auf vorhandene Benutzertoken aus. Ein Benutzer muss sich abmelden und dann wieder anmelden, um ein Zugriffstoken mit der neu zugewiesenen Berechtigung zu erhalten.

Um Berechtigungen mithilfe des MMC-Snap-Ins für lokale Sicherheitsrichtlinien zuzuweisen, bearbeiten Sie die Liste der Benutzer für jede Berechtigung, die unter **Sicherheit Einstellungen/Lokale Richtlinien/Zuweisen von Benutzerrechten** aufgeführt ist.

 

 
