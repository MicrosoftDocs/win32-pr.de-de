---
description: Implementieren von Eigenschaftenblatterweiterungen
ms.assetid: 5d1f9d91-e8a1-4cbb-b1de-4262a61e3cb7
title: Implementieren von Eigenschaftenblatterweiterungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23b4f74559176ecc0c411f75e7ca630db152a51109f09ecdca47a62d0113e70c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590280"
---
# <a name="implementing-property-sheet-extensions"></a>Implementieren von Eigenschaftenblatterweiterungen

Die WPD-Namespaceerweiterung unterstützt erweiterbare Eigenschaftenblätter. Dies sind die Eigenschaftendialogfelder, die angezeigt werden, wenn ein Benutzer mit der rechten Maustaste auf ein Objekt klickt, z. B. eine Datei oder einen Ordner, und **Eigenschaften auswählt.** Einige WPD-Anwendungen nutzen diese erweiterbaren Eigenschaftenblätter, um Eigenschaften für geräteseitige Inhalte (oder Objekte, die sich auf dem Gerät befinden) anzuzeigen.

Erweiterbare Eigenschaftenblätter werden von den in der folgenden Tabelle beschriebenen Schnittstellen unterstützt. Weitere Informationen zu diesen Schnittstellen finden Sie im Windows SDK.



| Schnittstelle           | BESCHREIBUNG                                                                  |
|---------------------|------------------------------------------------------------------------------|
| Idataobject         | Wird verwendet, um das PIDL-Array des Kontextmenüs an den Kontextmenühandler zu übergeben.      |
| IPropertySetStorage | Diese Schnittstelle wird verwendet, um WPD-Eigenschaften für das gegebene Objekt abzurufen.      |
| IPropertyStorage    | Diese Schnittstelle wird auch verwendet, um WPD-Eigenschaften für das gegebene Objekt abzurufen. |
| IShellExtInit       | Initialisiert die Windows Vista-Shellerweiterungen für das Kontextmenü.         |
| IShellPropSheetExt  | Unterstützt das Hinzustellen von Eigenschaftenblatterweiterungen.                              |



 

Eigenschaftenblätter für WPD werden wie jedes andere Eigenschaftenblatt in Windows Vista implementiert. Wenn Sie bereits einen Eigenschaftenblatthandler implementiert haben, können Sie Den vorhandenen Code so ändern, dass er geräteseitigen Inhalt unterstützt. Wenn Sie noch nie einen Kontextmenühandler erstellt haben, lesen Sie das Thema Creating Property Sheet Handlers (Erstellen von Eigenschaftenblatthandlern) im Windows SDK.

Die beiden Punkte, an denen sich ein WPD-Eigenschaftenblatthandler von jedem anderen Handler unterscheidet, sind die Handlerregistrierung und die Unterstützung geräteseitiger Inhalte.

 

 



