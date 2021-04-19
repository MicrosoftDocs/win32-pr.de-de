---
description: Eine Anlage-Engine ist eine DLL, die Dienst spezifische Konfigurations-und Analyseanforderungen verarbeitet. Dies bedeutet, dass die Verarbeitung verarbeitet wird, die nicht vom standardmäßigen Sicherheitskonfigurations-Toolset verarbeitet werden kann.
ms.assetid: c04779f4-f1e9-40b0-9f00-0176afb1b839
title: Erstellen einer Anlage-Engine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96b16e768956e61fe76406777da2bce9affbfa2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351814"
---
# <a name="creating-an-attachment-engine"></a>Erstellen einer Anlage-Engine

Eine Anlage-Engine ist eine DLL, die Dienst spezifische Konfigurations-und Analyseanforderungen verarbeitet. Dies bedeutet, dass die Verarbeitung verarbeitet wird, die nicht vom standardmäßigen Sicherheitskonfigurations-Toolset verarbeitet werden kann.

Zum Erstellen einer Anlage-Engine müssen Sie die folgenden drei Funktionen implementieren:

-   [**Scesvstreamtachmentanalysis**](scesvcattachmentanalyze.md): berechnet den Unterschied zwischen der Konfiguration des Diensts und der Konfiguration, die in der Sicherheitsdatenbank gespeichert ist. Diese Unterschiede werden in die Sicherheitsdatenbank geschrieben. Weitere Informationen finden Sie unter [Implementieren von scesvsintachmentanalysis](implementing-scesvcattachmentanalyze.md).
-   [**Scesvtortachmentconfig**](scesvcattachmentconfig.md): Hiermit wird der Dienst entsprechend der Angabe in der Snap-in-Benutzeroberfläche konfiguriert. Weitere Informationen finden Sie unter [Implementieren von scesvsintachmentconfig](implementing-scesvcattachmentconfig.md).
-   [**Scesvsintachmentupdate**](scesvcattachmentupdate.md), das die Basiskonfiguration und Konfigurations Analyse für den Dienst in der Sicherheitsdatenbank aktualisiert. Weitere Informationen finden Sie unter [Implementieren von scesvsintachmentupdate](implementing-scesvcattachmentupdate.md).

Das Sicherheitskonfigurations-Toolset implementiert eine Reihe von Unterstützungsfunktionen, die von der Anwendung aufgerufen werden können, um Informationen in der Sicherheitsdatenbank abzufragen und festzulegen. Weitere Informationen finden Sie unter [Anlage Rückruf Funktionen](management-functions.md).

Nachdem Sie eine Anlagen-Engine-dll erstellt haben, müssen Sie Sie beim Sicherheitskonfigurations-Toolset registrieren. Dieser Vorgang wird unter [Registrieren einer Anlage-Engine](registering-an-attachment-engine.md)beschrieben.

Zusätzlich zum Erstellen einer Anlagen-Engine müssen Sie auch eine Erweiterung für das Erweiterungs-Snap-in erstellen. Die Snap-in-Erweiterung bietet eine Benutzeroberfläche für Dienst spezifische Aufgaben. Wenn der Benutzer eine neue Konfiguration mit einer Snap-in-Erweiterung angibt, wird die Anforderung an die entsprechende Anlage-Engine übermittelt. Die Engine stellt dann eine Verbindung mit dem Dienst her und ändert seine Konfiguration. Wenn Sie keine Snap-in-Erweiterung implementieren, haben Benutzer keine Möglichkeit, die Dienst Konfiguration oder-Analyse zu ändern. Weitere Informationen zum Erstellen einer Erweiterungs-Snap-in-Erweiterung finden Sie unter [Creating a Attachment Snap-in Extension](creating-an-attachment-snap-in-extension.md).

 

 



