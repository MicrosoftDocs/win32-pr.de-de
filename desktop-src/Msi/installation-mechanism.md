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
# <a name="installation-mechanism"></a>Installationsmechanismus

Ein erfolgreicher Installationsvorgang besteht aus zwei Phasen: dem Erwerb und der Ausführung. Wenn die Installation nicht erfolgreich ist, kann eine Rollback Phase ausgeführt werden.

## <a name="acquisition"></a>Erwerb

Zu Beginn der Erwerbsphase weist eine Anwendung oder ein Benutzer das Installationsprogramm an, ein Feature oder eine Anwendung zu installieren. Der Installer durchläuft dann die Aktionen, die in den Sequenz Tabellen der-Installations Datenbank angegeben sind. Diese Aktionen Fragen die Installations Datenbank ab und generieren ein Skript, das ein schrittweises Verfahren zum Ausführen der Installation ermöglicht.

## <a name="execution"></a>Ausführung

Während der Ausführungsphase übergibt das Installationsprogramm die Informationen an einen Prozess mit erhöhten Rechten und führt das Skript aus.

## <a name="rollback"></a>Rollback

Wenn eine Installation nicht erfolgreich ist, stellt das Installationsprogramm den ursprünglichen Zustand des Computers wieder her. Wenn das Installationsprogramm das Installationsskript verarbeitet, generiert es gleichzeitig ein Rollback-Skript. Zusätzlich zum Rollback-Skript speichert das Installationsprogramm eine Kopie jeder Datei, die während der Installation gelöscht wird. Diese Dateien werden in einem verborgenen System Verzeichnis gespeichert. Nach Abschluss der Installation werden das Rollback-Skript und die gespeicherten Dateien gelöscht. Weitere Informationen finden Sie unter [Rollback-Installation](rollback-installation.md).

 

 



