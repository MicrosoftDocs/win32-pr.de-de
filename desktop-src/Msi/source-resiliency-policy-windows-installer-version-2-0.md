---
description: Windows Installer Version 2,0 beginnt mit der Suche nach einer Quelle, indem Sie den zuletzt verwendeten Quell Speicherort in der Quell Liste und dann die Liste der Netzwerk Quellen, anschließend die Medienquellen und schließlich URL-Quellen überprüft.
ms.assetid: 21b1a31e-efe3-4d45-b1c5-fe6ed9b19fed
title: Resilienzrichtlinie für Quelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 605c420198234405c23cb9672ca25c621b76390e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960151"
---
# <a name="source-resiliency-policy"></a>Resilienzrichtlinie für Quelle

Das Installationsprogramm beginnt mit der Suche nach einer Quelle, indem Sie den zuletzt verwendeten Quell Speicherort in der Quell Liste und dann die Liste der Netzwerk Quellen, anschließend die Medienquellen und schließlich URL-Quellen überprüfen. Weitere Informationen finden Sie unter [Quellen Resilienz](source-resiliency.md). Wenn die Suche fehlschlägt, stellt das Installationsprogramm möglicherweise ein Dialog Feld zum [Durchsuchen](browse-dialog.md) dar, in dem der Benutzer manuell nach der Quelle suchen kann Das Dialogfeld durchsuchen kann nicht angezeigt werden, wenn die [Benutzeroberflächen Ebenen](user-interface-levels.md) auf keine festgelegt sind. Ein Administrator steuert die Anzeige des Dialog Felds durchsuchen für Benutzer durch Festlegen der System Richtlinie.

Mit Windows Installer können nicht Administratoren standardmäßig das Dialogfeld Durchsuchen nicht verwenden, um verwaltete Anwendungs Quellen auf Medien zu suchen. verwaltete Anwendungen können nicht installiert werden. Ein Administrator ermöglicht einem nicht Administrator, mithilfe der Richtlinien [AllowLockdownBrowse](allowlockdownbrowse.md) und [AllowLockdownMedia](allowlockdownmedia.md) verwaltete Anwendungen von Medien zu durchsuchen oder zu installieren. Ein Administrator deaktiviert die Funktion zum Durchsuchen oder Installieren von Anwendungen von Medien mithilfe der Richtlinien " [disablebrowse](disablebrowse.md) " und " [disablemedia](disablemedia.md) ".

In der folgenden Tabelle wird die Verwendung dieser Systemrichtlinien in Windows Installer zusammengefasst.



| Systemrichtlinie                                  | Nicht-Administrator Benutzer, nicht verwaltete Anwendung                                                                                                             | Nicht Administrator Benutzer verwaltete Anwendung                                                                                                                 | Nicht verwaltete Anwendung für Administrator verwaltete Anwendungen                                                                                               |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AllowLockdownBrowse](allowlockdownbrowse.md) | Benutzer können nicht verwaltete Anwendungen mithilfe von Quellen auf Medien installieren. Benutzer können Medien nach den Quellen nicht verwalteter Anwendungen durchsuchen.<br/>    | Benutzer können verwaltete Anwendungen nicht mithilfe von Quellen auf Medien installieren. Benutzer können Medien nach den Quellen verwalteter Anwendungen durchsuchen.<br/>      | Administratoren können Anwendungen mithilfe von Quellen auf Medien installieren. Administratoren können Medien für die Anwendungs Quellen durchsuchen.<br/>    |
| [AllowLockdownMedia](allowlockdownmedia.md)   | Benutzer können nicht verwaltete Anwendungen mithilfe von Quellen auf Medien installieren. Benutzer können Medien nach den Quellen nicht verwalteter Anwendungen durchsuchen.<br/>    | Benutzer können verwaltete Anwendungen mithilfe von Quellen auf Medien installieren. Benutzer können keine Medien nach den Quellen verwalteter Anwendungen durchsuchen.<br/>      | Administratoren können Anwendungen mithilfe von Quellen auf Medien installieren. Administratoren können Medien für die Anwendungs Quellen durchsuchen.<br/>    |
| *Standard*                                      | Benutzer können nicht verwaltete Anwendungen mithilfe von Quellen auf Medien installieren. Benutzer können Medien nach den Quellen nicht verwalteter Anwendungen durchsuchen.<br/>    | Benutzer können verwaltete Anwendungen nicht mithilfe von Quellen auf Medien installieren. Benutzer können keine Medien nach den Quellen verwalteter Anwendungen durchsuchen.<br/>   | Administratoren können Anwendungen mithilfe von Quellen auf Medien installieren. Administratoren können Medien für die Anwendungs Quellen durchsuchen.<br/>    |
| [Disablebrowse](disablebrowse.md)             | Benutzer können nicht verwaltete Anwendungen mithilfe von Quellen auf Medien installieren. Benutzer können keine Medien für die Quellen nicht verwalteter Anwendungen durchsuchen.<br/> | Benutzer können verwaltete Anwendungen nicht mithilfe von Quellen auf Medien installieren. Benutzer können keine Medien nach den Quellen verwalteter Anwendungen durchsuchen. .<br/> | Administratoren können Anwendungen mithilfe von Quellen auf Medien installieren. Administratoren können keine Medien für die Anwendungs Quellen durchsuchen.<br/> |
| [Disablemedia](disablemedia.md)               | Benutzer können nicht verwaltete Anwendungen nicht mithilfe von Quellen auf Medien installieren. Benutzer können Medien nach den Quellen nicht verwalteter Anwendungen durchsuchen.<br/> | Benutzer können verwaltete Anwendungen nicht mithilfe von Quellen auf Medien installieren. Benutzer können keine Medien nach den Quellen verwalteter Anwendungen durchsuchen.<br/>   | Administratoren können keine Anwendungen mithilfe von Quellen auf Medien installieren. Administratoren können Medien für die Anwendungs Quellen durchsuchen.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Quellen Resilienz](source-resiliency.md)
</dt> </dl>

 

 




