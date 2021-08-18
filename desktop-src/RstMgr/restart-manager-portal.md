---
title: Neustart-Manager
description: Schreiben Sie benutzerdefinierte Installationsprogramme, um Systemneustarts zu vermeiden, die zum Abschließen der Aktualisierung einer datei in Gebrauch sind. Fahren Sie alle systemkritischen Systemdienste von Programmen herunter, und starten Sie sie neu.
ms.assetid: 44b7975a-0093-4c8f-9a14-2a6bfd7a68a5
keywords:
- Restart Manager Restart Mgr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d67910428fb781a5ddf8e2c719d30f2f0488e11d6b07daad1770788e8ad5f5ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010098"
---
# <a name="restart-manager"></a>Neustart-Manager

## <a name="purpose"></a>Zweck

Die Restart Manager-API kann die Anzahl von Systemneustarts, die zum Abschließen einer Installation oder eines Updates erforderlich sind, beseitigen oder verringern. Der Hauptgrund dafür, dass Softwareupdates während einer Installation oder eines Updates einen Systemneustart erfordern, ist, dass einige der dateien, die aktualisiert werden, derzeit von einer ausgeführten Anwendung oder einem ausgeführten Dienst verwendet werden. Mit dem Neustart-Manager können alle wichtigen [Systemdienste](critical-system-services.md) heruntergefahren und neu gestartet werden. Dadurch werden dateien frei, die verwendet werden, und installationsvorgänge können abgeschlossen werden.

## <a name="where-applicable"></a>Anwendungsbereich

Die Neustart-Manager-DLL exportiert eine öffentliche C-Schnittstelle, die von Standardinstallationsprogrammen oder benutzerdefinierten Installationsprogrammen geladen werden kann. Das Installationsprogramm kann den Neustart-Manager verwenden, um Dateien zu registrieren, die während der Installation einer Anwendung oder eines Updates ersetzt werden sollen. Während einer nachfolgenden Aktualisierung oder Installation kann das Installationsprogramm dann den Neustart-Manager verwenden, um zu bestimmen, welche Dateien nicht aktualisiert werden können, da sie derzeit verwendet werden. Der Neustart-Manager kann die nicht kritischen Dienste oder Anwendungen, die diese Dateien derzeit verwenden, herunterfahren und neu starten. Installationsprogramme können den Neustart-Manager an das Herunterfahren und Neustarten von Anwendungen oder Diensten basierend auf der in Gebrauchenen Datei, der Prozess-ID (PID) oder dem Kurznamen eines dienstbasierten Windows.

Der Neustart-Manager ist für die Entwicklung von Desktopanwendungen vorgesehen.

## <a name="developer-audience"></a>Entwicklergruppe

Diese Dokumentation richtet sich an Entwickler von Installationsanwendungen, die die Installerfunktionen in Windows Vista oder Windows Server 2008 nutzen möchten. Anwendungen, die den [Windows Installer](/windows/desktop/Msi/windows-installer-portal) Version 4.0 für die Installation und Wartung verwenden, verwenden den Neustart-Manager automatisch, um Systemneustarts zu reduzieren. Benutzerdefinierte Installationsprogramme können auch so entworfen werden, dass sie die Restart Manager-API aufrufen, um Anwendungen und Dienste herunter- und neu zu starten. In Fällen, in denen ein Systemneustart nicht möglich ist, können Installationsprogramme die Restart Manager-API verwenden, um Neustarts so zu planen, dass die Unterbrechung des Benutzerarbeitsablaufs minimiert wird.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Die Neustart-Manager-API ist ab Windows Vista und Windows Server 2008 verfügbar. Restart Manager besteht aus einer einzelnen DLL, die Anwendungen laden können, um auf die Restart Manager-API zuzugreifen.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                 | BESCHREIBUNG                                                     |
|-----------------------------------------------------------------------|-----------------------------------------------------------------|
| [Informationen zum Neustart-Manager](about-restart-manager.md)<br/>         | Übersichtsthemen, in denen der Neustart-Manager beschrieben wird.<br/>   |
| [Verwenden des Neustart-Managers](using-restart-manager.md)<br/>         | Übersichtsthemen zur Verwendung der Restart Manager-API.<br/> |
| [Referenz zum Neustart-Manager](restart-manager-reference.md)<br/> | Referenzthemen für die Neustart-Manager-API.<br/>        |



 

 

