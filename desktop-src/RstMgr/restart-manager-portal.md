---
title: Neustart-Manager
description: Schreiben Sie benutzerdefinierte Installationsprogramme, um Systemneustarts zu vermeiden, die erforderlich sind, um das Aktualisieren einer verwendeten Datei abzuschließen. Herunterfahren und Neustarten aller außer wichtigen Systemdienste von Programmen
ms.assetid: 44b7975a-0093-4c8f-9a14-2a6bfd7a68a5
keywords:
- Neustart-Manager neu starten Mgr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1244cff7bc22fd2e7b6d2540051bd0984596086
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039327"
---
# <a name="restart-manager"></a>Neustart-Manager

## <a name="purpose"></a>Zweck

Mit der API für den Neustart-Manager können Sie die Anzahl der Systemneustarts, die zum Durchführen einer Installation oder eines Updates erforderlich sind, eliminieren oder verringern. Der primäre Grund für Software Updates ist ein Systemneustart während einer Installation oder eines Updates erforderlich, da einige der Dateien, die aktualisiert werden, zurzeit von einer ausgelaufenden Anwendung oder einem Dienst verwendet werden. Mit dem Neustart-Manager können alle außer den [kritischen System Diensten](critical-system-services.md) heruntergefahren und neu gestartet werden. Dadurch werden Dateien freigegeben, die verwendet werden, und es können Installations Vorgänge ausgeführt werden.

## <a name="where-applicable"></a>Anwendungsbereich

Die Neustart-Manager-DLL exportiert eine öffentliche C-Schnittstelle, die von standardmäßigen oder benutzerdefinierten Installationsprogrammen geladen werden kann. Das Installationsprogramm kann den Neustart-Manager zum Registrieren von Dateien verwenden, die während der Installation einer Anwendung oder eines Updates ersetzt werden sollen. Während einer nachfolgenden Aktualisierung oder Installation kann das Installationsprogramm den Neustart-Manager verwenden, um zu bestimmen, welche Dateien nicht aktualisiert werden können, weil Sie zurzeit verwendet werden. Der Neustart-Manager kann die nicht wichtigen Dienste oder Anwendungen, die diese Dateien zurzeit verwenden, Herunterfahren und neu starten. Installationsprogramme können den Neustart-Manager anweisen, Anwendungen oder Dienste basierend auf der verwendeten Datei, der Prozess-ID (PID) oder dem Kurznamen eines Windows-Diensts herunterzufahren und neu zu starten.

Der Neustart-Manager ist für die Entwicklung von Anwendungen im Desktop Stil vorgesehen.

## <a name="developer-audience"></a>Entwicklergruppe

Diese Dokumentation ist für Entwickler von Installationsanwendungen gedacht, die die Installationsfunktionen von Windows Vista oder Windows Server 2008 nutzen möchten. Anwendungen, die die [Windows Installer](/windows/desktop/Msi/windows-installer-portal) Version 4,0 für die Installation und Wartung verwenden, verwenden automatisch den Neustart-Manager, um die Systemneustarts zu verringern. Benutzerdefinierte Installationsprogramme können auch so entworfen werden, dass Sie die Restart Manager-API zum Herunterfahren und Neustarten von Anwendungen und Diensten aufruft. In Fällen, in denen ein Systemneustart unvermeidlich ist, können Installer die Neustart-Manager-API verwenden, um Neustarts so zu planen, dass die Unterbrechung des Arbeits Flusses des Benutzers minimiert wird.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Die API für den Neustart-Manager ist ab Windows Vista und Windows Server 2008 verfügbar. Der Neustart-Manager besteht aus einer einzelnen dll, die Anwendungen für den Zugriff auf die Neustart-Manager-API laden können.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                 | BESCHREIBUNG                                                     |
|-----------------------------------------------------------------------|-----------------------------------------------------------------|
| [Informationen zum Neustart-Manager](about-restart-manager.md)<br/>         | Übersichts Themen, in denen der Neustart-Manager beschrieben wird.<br/>   |
| [Verwenden des Neustart-Managers](using-restart-manager.md)<br/>         | Übersichts Themen zur Verwendung der Neustart-Manager-API.<br/> |
| [Neustart-Manager-Verweis](restart-manager-reference.md)<br/> | Referenz Themen für die Neustart-Manager-API.<br/>        |



 

 

