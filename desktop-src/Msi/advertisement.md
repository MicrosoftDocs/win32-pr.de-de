---
description: Der Windows Installer kann die Verfügbarkeit einer Anwendung für Benutzer oder andere Anwendungen ankündigen, ohne die Anwendung tatsächlich zu installieren.
ms.assetid: 67170daa-448a-4a20-b38a-2dd36c95440f
title: Werbung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71f9d60eb1d709f0b956719593e2d7158ba8ef2bc17994945302474a02b695a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066370"
---
# <a name="advertisement"></a>Werbung

Der Windows Installer kann die Verfügbarkeit einer Anwendung für Benutzer oder andere Anwendungen ankündigen, ohne die Anwendung tatsächlich zu installieren. Wenn eine Anwendung angekündigt wird, werden dem Benutzer oder anderen Anwendungen nur die Schnittstellen angezeigt, die zum Laden und Starten der Anwendung erforderlich sind. Wenn ein Benutzer oder eine Anwendung eine angekündigte Schnittstelle aktiviert, wird das Installationsprogramm mit der Installation der erforderlichen Komponenten fortgesetzt, wie unter [Installation bei Bedarf](installation-on-demand.md)beschrieben.

Die beiden Arten von Werbung sind das Zuweisen und Veröffentlichen. Eine Anwendung wird einem Benutzer installiert angezeigt, wenn diese Anwendung dem Benutzer zugewiesen wird. Das **Startmenü** enthält die entsprechenden Tastenkombinationen, Symbole werden angezeigt, Dateien werden der Anwendung zugeordnet, und Registrierungseinträge spiegeln die Installation der Anwendung wider. Wenn der Benutzer versucht, eine zugewiesene Anwendung zu öffnen, wird sie bei Bedarf installiert.

Das Installationsprogramm unterstützt die Ankündigung von Anwendungen und Features gemäß dem Betriebssystem. Das Installationsprogramm registriert COM-Klasseninformationen für zugewiesene Anwendungen, beginnend mit Windows XP. Dadurch kann das Installationsprogramm die Anwendung beim Erstellen einer Instanz einer angekündigten Klasse installieren. Weitere Informationen finden Sie unter [Plattformunterstützung für Ankündigungen.](platform-support-of-advertisement.md)

Sie können eine Anwendung ab Windows Server 2003 auf dem Server veröffentlichen. Die veröffentlichte Anwendung wird dann über ihre Dateizuordnung oder den MIME-Typ (Multipurpose Internet Mail Extension) installiert. Bei der Veröffentlichung wird die Benutzeroberfläche nicht mit den Symbolen der Anwendung aufgefüllt. Das Clientbetriebssystem kann eine veröffentlichte Anwendung installieren, die mit Windows XP beginnt.

 

 



