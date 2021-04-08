---
title: Informationen zum Neustart-Manager
description: Der primäre Grund für die Installation und Aktualisierung von Software erfordert einen Systemneustart, da einige der Dateien, die aktualisiert werden, zurzeit von einer ausgelaufenden Anwendung oder einem Dienst verwendet werden.
ms.assetid: 9a1166d7-a0e1-4948-9077-278c84afccac
keywords:
- Neustart-Manager neu starten, Info
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec1cfd300d554e311ab43cc0a9413514b6b60081
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729576"
---
# <a name="about-restart-manager"></a>Informationen zum Neustart-Manager

Der primäre Grund für die Installation und Aktualisierung von Software erfordert einen Systemneustart, da einige der Dateien, die aktualisiert werden, zurzeit von einer ausgelaufenden Anwendung oder einem Dienst verwendet werden. Mit dem Neustart-Manager können alle außer wichtigen Anwendungen und Dienste heruntergefahren und neu gestartet werden. Dadurch werden die verwendeten Dateien freigegeben, und die Installations Vorgänge können ausgeführt werden. Außerdem kann die Anzahl der Systemneustarts, die zum Durchführen einer Installation oder eines Updates erforderlich sind, beseitigt oder reduziert werden.

Der Neustart-Manager stoppt Anwendungen in der folgenden Reihenfolge und startet Anwendungen, die für den Neustart in umgekehrter Reihenfolge registriert wurden, nach der Aktualisierung der Anwendungen neu.

1.  GUI-Anwendungen
2.  Konsolenanwendungen
3.  Windows-Dienste
4.  Windows-Explorer

Durch den Neustart-Manager werden Anwendungen oder Dienste nur dann heruntergefahren, wenn der Aufrufer über die entsprechende Berechtigung verfügt. Beachten Sie, dass das Sitzungs übergreifende Herunterfahren nicht unterstützt wird.

Anwendungen, die die [Windows Installer](/windows/desktop/Msi/windows-installer-portal) Version 4,0 für die Installation und Wartung verwenden, verwenden automatisch den Neustart-Manager, um die Systemneustarts zu verringern. Benutzerdefinierte Installationsprogramme können auch so entworfen werden, dass Sie die Restart Manager-API zum Herunterfahren und Neustarten von Anwendungen und Diensten aufruft. In Fällen, in denen ein Systemneustart unvermeidlich ist, können Installer die Neustart-Manager-API verwenden, um Neustarts so zu planen, dass die Unterbrechung des Arbeits Flusses des Benutzers minimiert wird.

Informationen zur Verwendung der Neustart-Manager-API während der Installation und Updates finden Sie unter [Verwenden des Neustart-Managers](using-restart-manager.md).

Kritische Systemdienste können vom Neustart-Manager ohne Systemneustart nicht beendet und neu gestartet werden. Weitere Informationen zum Identifizieren kritischer Systemdienste finden Sie unter [wichtige Systemdienste](critical-system-services.md).

Ihre Anwendungen und Dienste sollten so vorbereitet sein, dass Sie vom Neustart-Manager heruntergefahren werden und Benutzerdaten und Zustandsinformationen speichern, die für einen sauberen Neustart erforderlich sind. Weitere Informationen zum Vorbereiten von Anwendungen und Diensten für die Zusammenarbeit mit dem Neustart-Manager finden Sie unter [Richtlinien für Anwendungen und Dienste](guidelines-for-applications-and-services.md).

Referenzinformationen zu den Enumerationen, Strukturen und Funktionen der Neustart-Manager-API finden Sie im Abschnitt " [Neustart-Manager-Referenz](restart-manager-reference.md) ".

 

 