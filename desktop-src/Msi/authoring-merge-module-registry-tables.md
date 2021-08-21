---
description: Verwenden Sie Mergemodulregistrierungstabellen entsprechend dem Typ der Registrierungsinformationen.
ms.assetid: 091429ff-a8f4-4e1b-929f-1559cd173c3d
title: Erstellen von Registrierungstabellen für Mergemodule
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03726481905d4efee2405d0b383f53833d840090fea74e2d41fc6ae67a8e5bd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066150"
---
# <a name="authoring-merge-module-registry-tables"></a>Erstellen von Registrierungstabellen für Mergemodule

Verwenden Sie Mergemodulregistrierungstabellen entsprechend dem Typ der Registrierungsinformationen.

## <a name="typelib-class-appid-progid-extension-verb-or-mime-tables"></a>TypeLib-, Klassen-, AppId-, ProgId-, Erweiterungs-, Verb- oder MIME-Tabellen

Erstellen Sie für Typbibliotheken, Klassen, Erweiterungen und Verben Registrierungsinformationen in den [TypeLib-,](typelib-table.md) [](extension-table.md) [Klassen-,](class-table.md) [AppId-,](appid-table.md) [ProgId-,](progid-table.md)Erweiterungs-, [Verb-](verb-table.md)oder MIME-Tabellen des [Mergemoduls.](mime-table.md) Wenn Sie diese Informationen [mithilfe](registry-table.md) der Tabelle Registrierung hinzufügen, kann Windows 2000 keine systemweite Ankündigung für diese Komponenten bereitstellen.

Mergemodulautoren können sich aus den folgenden Gründen gegen die Registrierung mithilfe der Tabelle Class entscheiden:

-   Um von der Class-Tabelle registriert zu werden, muss die Datei der KeyPath der Komponente sein. Dies kann eine inakzeptable Änderung der Organisation von Komponenten erfordern.
-   Ein COM-Aufruf kann einen Installationsversuch auslösen, um eine angekündigte Klasse neu zu installieren. Autoren können entscheiden, eine Klasse nicht mithilfe der Tabelle Class zu registrieren, um zu vermeiden, dass eine Neuinstallation ausgelöst wird, wenn der Clientcomputer keine Benutzeroberfläche unterstützt.

## <a name="registry-table"></a>Registrierungstabelle

Verwenden Sie die Tabelle Registrierung, um Registrierungsinformationen hinzuzufügen, die nicht in die Tabellen TypeLib, Class, AppId, ProgId, Extension, Verb oder MIME erstellt werden können. Windows 2000 kann keine systemweite Ankündigung für Komponenten bereitstellen, die die Registry-Tabelle verwenden.

Wenn Sie die Registrierungstabelle erstellen, verweisen Sie auf Dateipfade mithilfe der \[ \# Datei oder \] \[ ! Dateiformat \] und nicht als \[ \] Verzeichnisdateiname. Das zweite Format unterstützt keine Installation vom Quellcode aus. Das frühere Format erleichtert auch die Erkennung fehlender Dateien und fehlerhafter Komponenten.

Bei der Verwendung von formatiertem Text in der Spalte Schlüssel der Tabelle Registrierung ist Vorsicht erforderlich. Da Windows Installer bereits installierte Komponenten nicht neu installiert, kann die Verwendung von formatiertem Text in diesem Feld dazu führen, dass Registrierungsschlüssel beim Entfernen der Anwendung zurückgelassen werden.

## <a name="selfreg-table"></a>SelfReg-Tabelle

Die Verwendung der SelfReg-Tabelle wird nicht empfohlen. Eine Liste der Gründe, warum die Selbstregistrierung nicht verwendet wird, finden Sie in der [SelfReg-Tabelle](selfreg-table.md). Sie sollten nach Möglichkeit die Tabellen TypeLib, Class, AppId, ProgId, Extension, Verb und MIME sowie in allen anderen Fällen die Registry-Tabelle verwenden.

 

 



