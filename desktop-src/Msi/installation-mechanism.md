---
description: 'Es gibt zwei Phasen für einen erfolgreichen Installationsprozess: Erwerb und Ausführung. Wenn die Installation nicht erfolgreich ist, kann eine Rollbackphase auftreten.'
ms.assetid: e9cda321-6978-4f9f-aff4-ccf609c88667
title: Installationsmechanismus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bce4396701ab5cddb43a67dddbafd1e8310092d04d779af04ad7876681cc3bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118634218"
---
# <a name="installation-mechanism"></a>Installationsmechanismus

Es gibt zwei Phasen für einen erfolgreichen Installationsprozess: Erwerb und Ausführung. Wenn die Installation nicht erfolgreich ist, kann eine Rollbackphase auftreten.

## <a name="acquisition"></a>Erwerb

Zu Beginn der Erwerbsphase weist eine Anwendung oder ein Benutzer das Installationsprogramm an, ein Feature oder eine Anwendung zu installieren. Das Installationsprogramm durchschreitet dann die aktionen, die in den Sequenztabellen der Installationsdatenbank angegeben sind. Diese Aktionen fragen die Installationsdatenbank ab und generieren ein Skript, das eine schrittweise Vorgehensweise zum Ausführen der Installation enthält.

## <a name="execution"></a>Ausführung

Während der Ausführungsphase übergibt das Installationsprogramm die Informationen an einen Prozess mit erhöhten Rechten und führt das Skript aus.

## <a name="rollback"></a>Rollback

Wenn eine Installation nicht erfolgreich ist, stellt das Installationsprogramm den ursprünglichen Zustand des Computers wieder her. Wenn das Installationsprogramm das Installationsskript verarbeitet, wird gleichzeitig ein Rollbackskript generiert. Zusätzlich zum Rollbackskript speichert das Installationsprogramm eine Kopie jeder Datei, die während der Installation gelöscht wird. Diese Dateien werden in einem ausgeblendeten Systemverzeichnis gespeichert. Nach Abschluss der Installation werden das Rollbackskript und die gespeicherten Dateien gelöscht. Weitere Informationen finden Sie unter [Rollbackinstallation.](rollback-installation.md)

 

 



