---
description: Ein zweistufiger Prozess erweitert das Transaktionsmodell des Windows Installer auf Produkte, die Common Language Runtime Assemblys enthalten. Dadurch kann das Installationsprogramm nicht erfolgreiche Installationen und Entfernungen von Assemblys zurücksetzen.
ms.assetid: 065a380c-4eb5-48a5-ab0a-7f1229b77898
title: Rollback von Assemblys im globalen Assemblycache
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c84bc3107355cb50c17043ee571edff708ba3f6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751120"
---
# <a name="rollback-of-assemblies-in-the-global-assembly-cache"></a>Rollback von Assemblys im globalen Assemblycache

Ein zweistufiger Prozess erweitert das Transaktionsmodell des Windows Installer auf Produkte, die Common Language Runtime Assemblys enthalten. Dadurch kann das Installationsprogramm nicht erfolgreiche Installationen und Entfernungen von Assemblys zurücksetzen.

Im ersten Schritt verwendet die Windows Installer das Microsoft .NET Framework, um eine Schnittstelle für jede Assembly zu erstellen. Die Windows Installer verwendet so viele Schnittstellen, wie Assemblys installiert werden. Das Ausführen eines Commits für eine Assembly über eine dieser Schnittstellen bedeutet lediglich, dass die Assembly bereit ist, vorhandene Assemblys mit demselben Namen zu ersetzen, Sie wird jedoch noch nicht ersetzt. Wenn der Benutzer die Installation abbricht oder ein schwerwiegender Installationsfehler vorliegt, kann die Windows Installer weiterhin die Assembly auf den vorherigen Zustand zurücksetzen, indem Sie diese Schnittstellen freigeben.

Nachdem der Windows Installer die Installation aller Assemblys und Windows Installer Komponenten abgeschlossen hat, kann das Installationsprogramm den zweiten Schritt der Installation einleiten. Im zweiten Schritt wird eine separate Funktion verwendet, um den endgültigen Commit aller neuen Common Language Runtime Assemblys durchzuführen. Dadurch werden alle vorhandenen Assemblys mit demselben Namen ersetzt.

 

 



