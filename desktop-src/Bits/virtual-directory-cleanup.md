---
title: Bereinigung virtueller Verzeichnisse
description: BITS erweitert virtuelle IIS-Verzeichnisse, um Uploads zu unterstützen.
ms.assetid: 8214904e-8a95-4c4b-a1c5-91e84031587f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ce883bbd9f1af31bc7cafb10a2484f3a56ecbcffa7917a5a0e491a38da4701b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118422191"
---
# <a name="virtual-directory-cleanup"></a>Bereinigung virtueller Verzeichnisse

BITS erweitert virtuelle IIS-Verzeichnisse, um Uploads zu unterstützen. Jedes virtuelle Verzeichnis verfügt über eine Sitzungstimeouteigenschaft (die IIS [BITSSessionTimeout-Metabasiseigenschaft),](bits-iis-extension-properties.md) die den Zeitraum angibt, in dem der BITS-Client beim Hochladen der Datei Fortschritte machen muss. Wenn während dieses Zeitraums kein Fortschritt erfolgt (der Timer wird zurückgesetzt, wenn der Fortschritt erfolgt), schließt BITS die Sitzung. Das Standardsitzungs-Time out beträgt 14 Tage.

BITS fügt dem Virtuellen Verzeichnis ein [Arbeitselement](/windows/desktop/TaskSchd/task-scheduler-start-page) Taskplaner für jedes virtuelle Verzeichnis hinzu, das Sie erstellen und aktivieren. Das Arbeitselement löscht Ressourcen, die den geschlossenen Sitzungen zugeordnet sind. Standardmäßig erfolgt die Bereinigung alle 12 Stunden. Wenn zwei virtuelle Verzeichnisse auf dasselbe physische Verzeichnis verweisen, löscht der von einem der Verzeichnisse initiierte Bereinigungsprozess die Ressourcen, die allen geschlossenen Sitzungen im physischen Verzeichnis zugeordnet sind.

Verwenden Sie die Registerkarte BITS-Erweiterung oder [Taskplaner](/windows/desktop/TaskSchd/task-scheduler-start-page) Schnittstellen, um den Bereinigungszeitplan entsprechend Ihrer Anwendung zu ändern. Sie können auch die [**IBITSExtensionSetup::GetCleanupTask-Methode**](/windows/desktop/api/Bitscfg/nf-bitscfg-ibitsextensionsetup-getcleanuptask) aufrufen, um einen Schnittstellenzeiger auf den Cleanuptask abzurufen, der dem virtuellen Verzeichnis zugeordnet ist.

> [!Note]  
> Wenn die Taskplaner nach der Aktivierung des virtuellen Verzeichnisses deaktiviert ist, funktioniert der Bereinigungsprozess für virtuelle Verzeichnisse nicht.

 

 

 