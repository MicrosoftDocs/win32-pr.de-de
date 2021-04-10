---
title: Cleanup des virtuellen Verzeichnisses
description: Bits erweitert virtuelle IIS-Verzeichnisse für die Unterstützung von Uploads.
ms.assetid: 8214904e-8a95-4c4b-a1c5-91e84031587f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83fb689bb3c797a311ec7c2ef8134eb51ffd6f1a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948909"
---
# <a name="virtual-directory-cleanup"></a>Cleanup des virtuellen Verzeichnisses

Bits erweitert virtuelle IIS-Verzeichnisse für die Unterstützung von Uploads. Jedes virtuelle Verzeichnis verfügt über eine Sitzungs Timeout-Eigenschaft (die IIS-Eigenschaft " [bitssessiontimeout](bits-iis-extension-properties.md) Metabase"), die den Zeitraum angibt, in dem der BITS-Client beim Hochladen der Datei Fortschritte ausführen muss. Wenn während dieses Zeitraums kein Fortschritt erfolgt (der Zeitgeber wird zurückgesetzt, wenn der Fortschritt erfolgt), schließt Bits die Sitzung. Der standardmäßige Sitzungs Timeout beträgt 14 Tage.

Mit Bits wird der [Taskplaner](/windows/desktop/TaskSchd/task-scheduler-start-page) für jedes virtuelle Verzeichnis, das Sie erstellen und aktivieren, ein Arbeits Element hinzugefügt. Mit dem Arbeits Element werden Ressourcen gelöscht, die den geschlossenen Sitzungen zugeordnet sind. Standardmäßig erfolgt die Bereinigung alle 12 Stunden. Wenn zwei virtuelle Verzeichnisse auf dasselbe physische Verzeichnis verweisen, löscht der Bereinigungs Prozess, der von einem der Verzeichnisse initiiert wurde, die Ressourcen, die allen geschlossenen Sitzungen im physischen Verzeichnis zugeordnet sind.

Verwenden Sie die Registerkarte Bits-Erweiterung oder die [Taskplaner](/windows/desktop/TaskSchd/task-scheduler-start-page) Schnittstellen, um den Bereinigungs Zeitplan entsprechend Ihrer Anwendung zu ändern. Sie können auch die [**ibitsextensionsetup:: getcleanuptask**](/windows/desktop/api/Bitscfg/nf-bitscfg-ibitsextensionsetup-getcleanuptask) -Methode aufrufen, um einen Schnittstellen Zeiger auf den Cleanuptask abzurufen, der dem virtuellen Verzeichnis zugeordnet ist.

> [!Note]  
> Wenn die Taskplaner nach dem Aktivieren des virtuellen Verzeichnisses deaktiviert ist, funktioniert der Cleanupprozess des virtuellen Verzeichnisses nicht.

 

 

 