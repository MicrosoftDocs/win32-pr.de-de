---
description: Ein zweistufiger Prozess erweitert das transaktionsbasierte Windows installer auf Produkte, die Common Language Runtime-Assemblys enthalten. Dadurch kann das Installationsprogramm ein Rollback für nicht erfolgreiche Installationen und Entfernungen von Assemblys ausführen.
ms.assetid: 065a380c-4eb5-48a5-ab0a-7f1229b77898
title: Rollback von Assemblys im globalen Assemblycache
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef1379d8132e4a0789108bae4b26fc02c492f5ccb9a0ec7699bba3d9d4de04d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625825"
---
# <a name="rollback-of-assemblies-in-the-global-assembly-cache"></a>Rollback von Assemblys im globalen Assemblycache

Ein zweistufiger Prozess erweitert das transaktionsbasierte Windows installer auf Produkte, die Common Language Runtime-Assemblys enthalten. Dadurch kann das Installationsprogramm ein Rollback für nicht erfolgreiche Installationen und Entfernungen von Assemblys ausführen.

Im ersten Schritt verwendet der Windows Installer die Microsoft .NET Framework, um eine Schnittstelle für jede Assembly zu erstellen. Der Windows Installer verwendet so viele Schnittstellen, wie Assemblys installiert werden. Das Committen einer Assembly mithilfe einer dieser Schnittstellen bedeutet nur, dass die Assembly bereit ist, alle vorhandenen Assemblys mit demselben Namen zu ersetzen. Sie ersetzt sie noch nicht. Wenn der Benutzer die Installation abbricht oder ein schwerwiegender Installationsfehler auftritt, kann der Windows Installer die Assembly weiterhin in den vorherigen Zustand zurücksetzen, indem diese Schnittstellen veröffentlicht werden.

Nachdem der Windows Installer die Installation aller Assemblys und Windows Installer-Komponenten abgeschlossen hat, kann das Installationsprogramm den zweiten Schritt der Installation initiieren. Im zweiten Schritt wird eine separate Funktion verwendet, um den endgültigen Commit aller neuen Common Language Runtime-Assemblys zu erstellen. Dadurch werden alle vorhandenen Assemblys mit dem gleichen Namen ersetzt.

 

 



