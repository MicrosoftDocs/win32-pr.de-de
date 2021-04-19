---
description: Der Windows Installer kann die Verfügbarkeit einer Anwendung für Benutzer oder andere Anwendungen ankündigen, ohne die Anwendung tatsächlich zu installieren.
ms.assetid: 67170daa-448a-4a20-b38a-2dd36c95440f
title: Werbung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0bb31f14fb4cd6f589e94939afdd5575df52c43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362426"
---
# <a name="advertisement"></a>Werbung

Der Windows Installer kann die Verfügbarkeit einer Anwendung für Benutzer oder andere Anwendungen ankündigen, ohne die Anwendung tatsächlich zu installieren. Wenn eine Anwendung angekündigt wird, werden dem Benutzer oder anderen Anwendungen nur die Schnittstellen angezeigt, die zum Laden und Starten der Anwendung erforderlich sind. Wenn ein Benutzer oder eine Anwendung eine angekündigte Oberfläche aktiviert, fährt der Installer mit der Installation der erforderlichen Komponenten fort, wie unter [Installation nach Bedarf](installation-on-demand.md)beschrieben.

Die beiden Arten der Werbung sind das zuweisen und veröffentlichen. Eine Anwendung wird für einen Benutzer installiert, wenn die Anwendung dem Benutzer zugewiesen wird. Das **Startmenü** enthält die entsprechenden Tastenkombinationen, Symbole werden angezeigt, Dateien sind der Anwendung zugeordnet, und Registrierungseinträge spiegeln die Installation der Anwendung wider. Wenn der Benutzer versucht, eine zugewiesene Anwendung zu öffnen, wird er nach Bedarf installiert.

Das Installationsprogramm unterstützt die Ankündigung von Anwendungen und Features entsprechend dem Betriebssystem. Der Installer registriert com-Klassen Informationen für zugewiesene Anwendungen ab Windows XP. Dadurch kann das Installationsprogramm die Anwendung bei der Erstellung einer Instanz einer angekündigten Klasse installieren. Weitere Informationen finden Sie unter [Platt Form Unterstützung für Werbung](platform-support-of-advertisement.md).

Sie können eine Anwendung auf dem Server ab Windows Server 2003 veröffentlichen. Die veröffentlichte Anwendung wird dann über die Datei Zuordnung oder den MIME-Typ (Mehrzweck-Internet Mail Erweiterung) installiert. Bei der Veröffentlichung wird die Benutzeroberfläche nicht mit den Symbolen der Anwendung aufgefüllt. Das Client Betriebssystem kann eine veröffentlichte Anwendung ab Windows XP installieren.

 

 



