---
description: Es gibt einige Überlegungen, die für Remote verwaltete Systeme eindeutig sind.
ms.assetid: bfdf121e-9b4e-4323-82ec-9bd32531caad
title: Überlegungen zur WFP-Remote Verwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57bb40776f6b727abb49d7e0685bb12b087ed2bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366085"
---
# <a name="wfp-remote-administration-considerations"></a>Überlegungen zur WFP-Remote Verwaltung

Es gibt einige Überlegungen, die für Remote verwaltete Systeme eindeutig sind. Zuerst werden bei der Remote Bereitstellung der Software Installation (mit SMS oder MSI) WFP-Fehler Dialogfelder auf dem Bildschirm eines lokal angemeldeten Administrators (sofern vorhanden) und nicht des Installations Diensts angezeigt. Zweitens: Wenn ein Administrator sich Remote bei einem Terminal Server anmeldet und eine Anwendung installiert, die Geschützte Systemdateien ersetzt, werden die WFP-Fehler Dialogfelder nur in der Hauptkonsole angezeigt, nicht im Remote Fenster des Administrators.

Aus diesen Gründen unterdrückt WFP die Fehler Dialogfelder, bis sich ein Administrator lokal anmeldet. Remote Administratoren können Datei Ersetzungs Fehler im System Ereignisprotokoll finden.

**Windows Vista und Windows Server 2008:** Die WFP-Remote Verwaltung wird nicht unterstützt.

 

 



