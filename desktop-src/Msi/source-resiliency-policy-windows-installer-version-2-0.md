---
description: Windows Installer Version 2.0 beginnt mit der Suche nach einer Quelle, indem der zuletzt verwendete Quellspeicherort in der Quellliste, dann die Liste der Netzwerkquellen, medienquellen und schließlich URL-Quellen überprüft wird.
ms.assetid: 21b1a31e-efe3-4d45-b1c5-fe6ed9b19fed
title: Quellresilienzrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4951c1183da8998986863fe5dae744fc58c23387306c91153b50ab63e38e0a3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039710"
---
# <a name="source-resiliency-policy"></a>Quellresilienzrichtlinie

Das Installationsprogramm beginnt mit der Suche nach einer Quelle, indem es den zuletzt verwendeten Quellspeicherort in der Quellliste, dann die Liste der Netzwerkquellen, medienquellen und schließlich URL-Quellen überprüft. Weitere Informationen finden Sie unter [Quellresilienz.](source-resiliency.md) Wenn bei der Suche ein Fehler auftritt, kann das Installationsprogramm ein [Dialogfeld](browse-dialog.md) zum Durchsuchen öffnen, mit dem der Benutzer manuell nach der Quelle suchen kann. Das Dialogfeld zum Durchsuchen kann nicht angezeigt werden, wenn [die Benutzeroberflächenebenen](user-interface-levels.md) auf Keine festgelegt sind. Ein Administrator steuert die Anzeige des Dialogfelds "Durchsuchen" für Benutzer durch Festlegen der Systemrichtlinie.

Mit Windows Installer können Nichtadministratoren standardmäßig nicht das Dialogfeld zum Durchsuchen verwenden, um verwaltete Anwendungsquellen auf Medien zu suchen, und verwaltete Anwendungen können nicht installiert werden. Ein Administrator ermöglicht es einem Nichtadministrator, verwaltete Anwendungen mithilfe der Richtlinien [AllowLockdownBrowse](allowlockdownbrowse.md) und [AllowLockdownMedia](allowlockdownmedia.md) auf Medien zu durchsuchen oder zu installieren. Ein Administrator deaktiviert die Funktion zum Durchsuchen oder Installieren von Anwendungen von Medien mithilfe der [Richtlinien DisAbleBrowse](disablebrowse.md) und [DisAbleMedia.](disablemedia.md)

In der folgenden Tabelle wird die Verwendung dieser Systemrichtlinien im Windows zusammengefasst.



| Systemrichtlinie                                  | Nicht verwaltete Anwendung des Benutzers "NonAdministrator"                                                                                                             | Vom Benutzer nicht verwaltete Anwendung ohne Administrator                                                                                                                 | Nicht verwaltete Anwendung mit Administratorverwaltung                                                                                               |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AllowLockdownBrowse](allowlockdownbrowse.md) | Benutzer können nicht verwaltete Anwendungen mithilfe von Quellen installieren, die sich auf Medien befinden. Benutzer können Medien nach den Quellen nicht verwalteter Anwendungen durchsuchen.<br/>    | Benutzer können verwaltete Anwendungen nicht mithilfe von Quellen installieren, die sich auf Medien befinden. Benutzer können Medien nach den Quellen verwalteter Anwendungen durchsuchen.<br/>      | Administratoren können Anwendungen mithilfe von Quellen installieren, die sich auf Medien befinden. Administratoren können Medien nach den Quellen von Anwendungen durchsuchen.<br/>    |
| [AllowLockdownMedia](allowlockdownmedia.md)   | Benutzer können nicht verwaltete Anwendungen mithilfe von Quellen installieren, die sich auf Medien befinden. Benutzer können Medien nach den Quellen nicht verwalteter Anwendungen durchsuchen.<br/>    | Benutzer können verwaltete Anwendungen mithilfe von Quellen installieren, die sich auf Medien befinden. Benutzer können keine Medien nach den Quellen verwalteter Anwendungen durchsuchen.<br/>      | Administratoren können Anwendungen mithilfe von Quellen installieren, die sich auf Medien befinden. Administratoren können Medien nach den Quellen von Anwendungen durchsuchen.<br/>    |
| *Standard*                                      | Benutzer können nicht verwaltete Anwendungen mithilfe von Quellen installieren, die sich auf Medien befinden. Benutzer können Medien nach den Quellen nicht verwalteter Anwendungen durchsuchen.<br/>    | Benutzer können verwaltete Anwendungen nicht mithilfe von Quellen installieren, die sich auf Medien befinden. Benutzer können keine Medien nach den Quellen verwalteter Anwendungen durchsuchen.<br/>   | Administratoren können Anwendungen mithilfe von Quellen installieren, die sich auf Medien befinden. Administratoren können Medien nach den Quellen von Anwendungen durchsuchen.<br/>    |
| [DisAbleBrowse](disablebrowse.md)             | Benutzer können nicht verwaltete Anwendungen mithilfe von Quellen installieren, die sich auf Medien befinden. Benutzer können keine Medien nach den Quellen nicht verwalteter Anwendungen durchsuchen.<br/> | Benutzer können verwaltete Anwendungen nicht mithilfe von Quellen installieren, die sich auf Medien befinden. Benutzer können keine Medien nach den Quellen verwalteter Anwendungen durchsuchen. .<br/> | Administratoren können Anwendungen mithilfe von Quellen installieren, die sich auf Medien befinden. Administratoren können keine Medien nach den Quellen von Anwendungen durchsuchen.<br/> |
| [DisAbleMedia](disablemedia.md)               | Benutzer können nicht verwaltete Anwendungen nicht mithilfe von Quellen installieren, die sich auf Medien befinden. Benutzer können Medien nach den Quellen nicht verwalteter Anwendungen durchsuchen.<br/> | Benutzer können verwaltete Anwendungen nicht mithilfe von Quellen installieren, die sich auf Medien befinden. Benutzer können keine Medien nach den Quellen verwalteter Anwendungen durchsuchen.<br/>   | Administratoren können keine Anwendungen mithilfe von Quellen installieren, die sich auf Medien befinden. Administratoren können Medien nach den Quellen von Anwendungen durchsuchen.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Quellresilienz](source-resiliency.md)
</dt> </dl>

 

 




